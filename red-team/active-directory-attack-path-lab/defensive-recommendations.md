# Defensive Recommendations — Active Directory Attack Path Lab

This document provides hardening recommendations for each vulnerability identified in the lab. The goal is to demonstrate not just offensive capability, but a thorough understanding of defensive countermeasures.

---

## 1. Kerberoasting Mitigation

**Finding:** Service accounts with SPNs set and weak passwords are vulnerable to offline password cracking via Kerberoasting.

**Recommendations:**
- Use long, complex, randomly generated passwords (25+ characters) for all service accounts
- Implement Group Managed Service Accounts (gMSA) — passwords are automatically managed and rotated by AD
- Enable AES encryption for Kerberos tickets (disables weaker RC4 encryption which is faster to crack)
- Monitor for high volumes of TGS requests from a single account (potential Kerberoasting activity)

**Detection:** Event ID 4769 — Kerberos Service Ticket Requested (filter for RC4 encryption type `0x17`)

---

## 2. AS-REP Roasting Mitigation

**Finding:** Accounts with Kerberos pre-authentication disabled can have their hashes captured and cracked offline.

**Recommendations:**
- Enable Kerberos pre-authentication on all accounts (this is the default — ensure it has not been manually disabled)
- Audit accounts with `DONT_REQUIRE_PREAUTH` flag set using: `Get-ADUser -Filter {DoesNotRequirePreAuth -eq $True}`
- Use strong passwords on any accounts that legitimately require pre-auth to be disabled

**Detection:** Event ID 4768 with `Pre-Authentication Type: 0`

---

## 3. ACL Misconfiguration Mitigation

**Finding:** Over-permissive ACLs (GenericAll, GenericWrite, WriteDACL) granted to non-privileged accounts allow privilege escalation.

**Recommendations:**
- Regularly audit AD ACLs using BloodHound or PingCastle
- Remove unnecessary permissions — apply the principle of least privilege
- Use tiered AD administration model (Tier 0 / Tier 1 / Tier 2) to prevent lateral movement between privilege levels
- Protect privileged groups using AdminSDHolder — ensure it is not misconfigured

**Detection:** Event ID 5136 — Directory Service Object Modified (monitor for ACL changes on sensitive objects)

---

## 4. Unconstrained Delegation Mitigation

**Finding:** Unconstrained delegation enabled on workstations allows an attacker with local admin access to extract TGTs for any user that authenticates to the machine.

**Recommendations:**
- Remove unconstrained delegation from all workstations and non-DC servers
- Use constrained delegation with protocol transition only where delegation is a genuine business requirement
- Enable the "Account is sensitive and cannot be delegated" flag on all privileged accounts
- Use Protected Users security group for highly privileged accounts — members cannot be delegated

**Detection:** Monitor for changes to the `msDS-AllowedToDelegateTo` attribute (Event ID 5136)

---

## 5. Local Admin Password Reuse Mitigation

**Finding:** Identical local administrator passwords across workstations allow an attacker to use a single compromised hash to gain local admin on all machines (Pass-the-Hash lateral movement).

**Recommendations:**
- Deploy **Microsoft LAPS (Local Administrator Password Solution)** to enforce unique, auto-rotating local admin passwords on all endpoints
- Disable the default local Administrator account where possible
- Use Windows Defender Credential Guard to protect credentials in memory

**Detection:** Event ID 4624 (Logon Type 3) from unexpected source machines; lateral movement patterns in SIEM

---

## 6. Credentials in SYSVOL / Group Policy Preferences

**Finding:** Group Policy Preferences XML files stored in SYSVOL may contain encrypted passwords, which can be decrypted using the publicly available AES key.

**Recommendations:**
- Immediately remove any passwords from GPP XML files in SYSVOL
- Apply Microsoft KB2962486 (patch released 2014) to prevent new GPP passwords being stored
- Audit SYSVOL for any `cpassword` fields: `findstr /S /I cpassword \\[domain]\sysvol\[domain]\policies\*.xml`
- Rotate any credentials that were exposed

**Detection:** File access to GPP XML files from non-administrative accounts (file system auditing)

---

## General AD Hardening Recommendations

1. **Tiered Administration Model** — Separate accounts for workstation admin, server admin, and domain admin tasks
2. **Privileged Access Workstations (PAWs)** — Use dedicated, hardened machines for privileged administration
3. **Regular AD Security Audits** — Run BloodHound or PingCastle quarterly to identify new privilege escalation paths
4. **Microsoft Defender for Identity** — Deploy for real-time detection of AD-based attacks
5. **Patch Management** — Ensure all DCs and workstations are patched promptly, particularly for Kerberos-related CVEs

---

## References

- Microsoft LAPS: https://learn.microsoft.com/en-us/windows-server/identity/laps/laps-overview
- BloodHound: https://github.com/BloodHoundAD/BloodHound
- PingCastle: https://www.pingcastle.com/
- MITRE ATT&CK — Active Directory techniques: https://attack.mitre.org/matrices/enterprise/windows/
- CIS Benchmark for Active Directory: https://www.cisecurity.org/benchmark/microsoft_windows_server
