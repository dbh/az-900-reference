- [Security](#security)
  - [MFA](#mfa)
  - [Azure AD MFA](#azure-ad-mfa)
  - [Conditional Access](#conditional-access)

# Security
## MFA
Requires additional security forident by req two or more elements to fully auth

Categories
* User knows
* User has 
  * ex temporal code via phone
* Something user is 
  * (Biometrics)

## Azure AD MFA
* MS Service for MFA
* Can use ex phone call or mobile app notificaiton
* can be enfoced for org based on security defaults on az tenant
* Can be used for Office 365 auth

## Conditional Access
* Uses Azure AD
* Identity Signals
  * who
  * where
  * device type
* Collects signals
* Makes Decisions
  * might demand another auth type
* Enforcement
* Can be setup for MFA 
  * to an app, certain users, user types, different networks
  * services through approved client apps
  * require users to access ap only from managed devices
  * Block access from untrusted sources
* What-if tool
* License
  * AD P1 or P2
  * MS 365 Business Premium