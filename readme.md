<img src="./public/amazonaws.svg">

# AWS
Amazon Web Services offers reliable, scalable, and inexpensive cloud computing services. Free to join, pay only for what you use. This blog will help you understand different services and resources that aws provides. This is incomplete, currently contains content that I have learned so far, I will update this from time to time.

# IAM
Identity and access management is a we service of aws which helps us to manage aws resources and let us define who and upto what limit they can access or use allocated aws resource under the supervision of certain rules.

## IAM Components

**Users**<br/>
IAM provides us the capability of creating sub-users for accessing the same aws account and resources that you have, using this functionality you can create different users with different capabilities or permission for accomplishing different tasks. 

**Groups**<br/>
A collection of IAM users is an IAM Group. It used to define rules or permission which is common for multiple users. Any user added to this group will inherit all the permission defined for that particular group. This is just for reducing administrative load.
 
**Roles**<br/>
Roles are similar to users but in this case permission and credentials are alloted to resources or entities instead od users on aws. It is basically used to control the accessibilty of resources over other resources on aws.

**Policies**<br/>
These are the sets of rules and permission which is used to restrict users and roles. In aws we can define rules on json format or we can use UI provided by aws.

## How users can access AWS:
- **AWS management console** (protected by password/MFA)
- **AWS Command line interface** (protected by access key)
- **AWS Software developer kit** (sdk) for programmatic accessibilty

## IAM Security and auditing
It is very important for aws users to monitor and audit its users. In IAM this can be achieved by 
- **IAM credentials reports** (account-level): A report that list all your account users and status of their credentails.
- **IAM access advisor** (user-level): Access advisor shows the service permission granted to a user and when those were last accessed.

*IAM PASSWORD POLICY - strong password means higher security, so inorder to focus on this, IAM uses passwor policy it allows aws account user to define password creation rules for its user, It provides a set of rules that user can follow in order to update password*

## IAM Guidelines and best practices

- Don't use root account except for aws account setup, in other cases try to access aws resources using sub user account with restricted permission.
- Always assign users to group and then assign polices to it.
- Create strong password policy and try to enforce the use of MFA (mutli factor authentication).
- Use access key for programmatic access (sdk/cli).
- Always audit permissions of your account using [***IAM credentials report***](#iam-security-and-auditing) and [***IAM access advisor***](#iam-security-and-auditing).

![IAM](./public/diagrams/iam.svg)


