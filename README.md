# NIST-password-policy-audit
"A security audit project assessing web application password policies against NIST SP 800-63B Digital Identity Guidelines."

# Password Policy Audit (NIST SP 800-63B)

This project demonstrates a **Password Policy Audit** of a sample web application login system against **NIST SP 800-63B (Digital Identity Guidelines)**.

## Objectives
- Assess the application’s password policy
- Identify gaps against NIST recommendations
- Provide actionable security recommendations

## Methodology
1. Tested minimum and maximum password length
2. Checked for complexity rules
3. Verified breach password checks
4. Reviewed password expiration policies
5. Tested copy-paste in password fields
6. Checked for MFA availability

## Findings
| Test | NIST Requirement | System Behavior | Result |
|------|-----------------|-----------------|--------|
| Minimum Length | ≥ 8 | Allowed 6 | ❌ Fail |
| Maximum Length | ≥ 64 | Capped at 16 | ❌ Fail |
| Complexity Rules | Not enforced | Forced complexity | ❌ Fail |
| Breached Password Check | Required | Not implemented | ❌ Fail |
| Password Expiration | Not required | Forced 90-day reset | ❌ Fail |
| Copy-Paste | Allowed | Blocked | ❌ Fail |
| MFA | Recommended | Not available | ❌ Fail |

## Recommendations
- Increase maximum password length (≥ 64)
- Remove complexity rules, allow passphrases
- Implement breached password check
- Remove forced expiration policies
- Allow copy-paste (support password managers)
- Implement MFA

## Files Included
- `Password_Policy_Audit_Report.pdf` – Report (PDF version)
- `Password_Policy_Audit_Report.docx` - Report (Word)
- `NIST_Password_Audit_Checklist.xlsx` – Audit checklist
- `BLOG.md` – Blog draft for Medium

## Blog
I also wrote a blog explaining this project in detail: https://medium.com/@aswinstanly03/auditing-password-policies-with-nist-sp-800-63b-a-practical-project-b0f0eeac3adc

---

