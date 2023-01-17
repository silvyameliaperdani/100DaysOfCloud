
# Multi Factor Authentication - MFA. Course AWS Certified Cloud Practitioner on Udemy by Stephane Maarek

## Cloud Research
- Users have access to your account and can possibly change configurations or         delete resources in your AWS account
- You want to protect you Root Accounts and IAM users 
- MFA = password you know + security device you own 
- Main benefit of MFA :
  if a password is stolen or hacked, the account is not compromised
  
## MFA device options in AWS 
- Virtual MFA Device 
 - Google Authenticator ( phone only )
 - Aunty ( multi-device )
- Universal 2nd Factor (U2F) Security Key 
 - YubiKey by Yubico ( 3rd party )
- Hardware Key Fob MFA Device 
 - Provided by Gemalto ( 3rd party )
- Hardware Key Fob MFA Device for AWS GovCloud ( US )
 - Provided by SurePassID ( 3rd party )
 ## How can Users Access AWS ? 
  - AWS Management Console (Protected by password + MFA )
  - AWS Command Line Interface ( CLI ): Protected by access keys 
  - AWS Software Developer Kit ( SDK ) - For code:protected by access keys
 ##  IAM Roles For Service 
 - Some AWS service will need to perform actions on your behalf 
 - To do so, we will assign permissions to AWS services with IAM Roles 
 - Common Roles : 
  - EC2 Instance Roles 
  - Lambda Function Roles
  ## IAM Security Tools 
   - IAM Credentials Report ( account-level )
   - IAM Access Advisor ( user-level )
   
 ## Social Proof


[Twitter](https://twitter.com/silvyameliaa_/status/1614773214714134529)

 
