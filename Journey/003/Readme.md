
# IAM : Identity and Access Management - Course AWS Certified Cloud Practitioner on Udemy by Stephane Maarek

## Cloud Research

## IAM - Identity and Access Management 
AWS Identity and Access Management (IAM)allows you to control access to compute, storage, database, and application services in the AWS Cloud.IAM can be used to handle authentication, and to specify and enforce authorization policies so that you can specify which users can access which services. 
- IAM this is a global service
- Root Account : create by default, shouldn't be used or shared 
- Users : are people within your organization, and can be grouped
- Groups : only contain users, not other groups 
- Users don't have to belong to a group, and user can belong to multiple groups

## IAM Permissions 
- User or Groups can be assigned JSON documents called policies
- These policies define the permission of the users 
- In AWS you apply the least privilege principle, don't give more permissions than   a user needs 

## IAM Policy 
  is a document that defines permissions to determine what users can do in the AWS   account. A policy typically grants access to specific resources and specifies       what the user can do with those resources. Policies can also explicitly deny       access.
  Consists of 
  - Version, Policy language version, always include "2012-10-17"
  - Id, an identifier for the policy (optional)
  - Statement, one or more individual statements (required)
  Statements consists of 
  - Sid, an identifier for the statement (optional)
  - Effectwhether the statement allows or denies access (Allow, Deny)  
  - Principal: account/user/role to which this policy applied to 
  - Action: list of actions this policy allows or denies 
  - Resource: list of resources to which the actions applied to 
  - Condition: conditions for when this policy is in effect (optional

## IAM Password Policy 
 - Strong passwords = higher security for your account 
 - Setup a password policy :
  - set a minimum password legth
  - Require specific charater types :
   - including uppercase letters
   - lowercase letters 
   - numbers 
   - non-alphanumeric charcters 
 - Allow all IM users to change their own passwords 
 - Require users to change their password after some time (password expiration)
 - Prevent password re-use 
