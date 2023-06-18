# IAM (Identity and Access Management)

## IAM: Introduction
- IAM stands for Identity and Access Management.
- IAM is a global service provided by AWS for managing user identities and controlling their access to AWS resources.
- The root account is created by default during AWS account setup, but it is recommended not to use or share the root account for day-to-day activities.
- Users in IAM represent individuals within your organization and can be grouped together for easier management.
- Groups in IAM only contain users, not other groups. They help in organizing and applying permissions to multiple users simultaneously.
- Users do not belong to a specific group and can belong to multiple groups simultaneously.

## IAM: Permissions and Policies
- Users or groups in IAM can be assigned JSON documents called policies.
- Policies define permissions for actions that can be performed on AWS resources.
- The principle of least privilege should be followed, which means not granting more permissions than necessary for a user to perform their tasks.

## IAM: Policy Structure
- IAM policies consist of the following components:
  - Version: The policy language version. Always include "2012-10-17".
  - Id: An identifier for the policy (optional).
  - Statement: One or more individual statements (required).

- Statements consist of the following elements:
  - Sid: An identifier for the statement (optional).
  - Effect: Whether the statement allows or denies access (Allow or Deny) (required).
  - Principal: The AWS account/user/role to which this policy is applied (required).
  - Action: A list of actions that this policy allows or denies (required).
  - Resource: A list of resources to which the actions apply (required).
  - Condition: Conditions for when this policy is in effect (optional).

## IAM - Password Policy
- Strong passwords enhance the security of your AWS account.
- In AWS, you can set up a password policy to enforce certain requirements:
  - Set a minimum password length.
  - Require specific character types.
  - Allow all IAM users to change their own passwords.
  - Require users to change their passwords after a specific time period.
  - Prevent password reuse.

## Multi-Factor Authentication (MFA)
- Multi-Factor Authentication adds an extra layer of security by combining a password with a security device that the user owns.
- It provides an additional level of assurance for accessing AWS resources.

## AWS Access Keys, CLI, and SDK
- There are three options to access AWS resources:
  - AWS Management Console: Accessed through a web browser.
  - AWS Command Line Interface (CLI): Protected by access keys, allows for scripting and automation.
  - AWS Software Development Kit (SDK): Provides language-specific APIs for developing applications that interact with AWS services.

## AWS CLI (Command Line Interface)
- The AWS Command Line Interface (CLI) is a tool that enables you to interact with AWS services using commands in your command-line shell.
- It's an open-source tool that allows you to manage and configure AWS services.
- You can develop scripts to automate your AWS resource management tasks.
- The AWS CLI provides direct access to the public APIs of AWS services.

## AWS SDK (Software Development Kit)
- The AWS SDK (Software Development Kit) provides language-specific APIs for interacting with AWS services.
- It supports various programming languages such as JavaScript, PHP, Python, .NET, and more.
- With the AWS SDK, you can integrate AWS services into your applications and leverage their functionality.

## AWS CloudShell
- AWS CloudShell is a browser-based shell available within the AWS Management Console.
- It provides a command-line interface with pre-installed AWS CLI and SDK tools.
- AWS CloudShell allows you to manage and automate AWS resources directly from your browser.
- Please note that AWS CloudShell availability may vary across regions.

## IAM Roles
- IAM Roles allow you to assign permissions to AWS services instead of individual users.
- Roles are used to delegate access to AWS services securely.
- They help in maintaining security and access control by providing temporary credentials.

## IAM Security Tools
- IAM Credentials Report (account-level): Generates a report that lists all your account's users and the status of their various credentials.
- IAM Access Advisor (user-level): Shows the service permissions granted to a user and when those services were last accessed.

## IAM Guidelines & Best Practices
- Don't use the root account except for AWS account setup.
- Follow the one physical user = one AWS user principle.
- Assign users to groups and assign permissions to groups.
- Create a strong password policy for IAM users.
- Enable Multi-Factor Authentication (MFA) for added security.
- Use IAM Roles to grant permissions to AWS services.
- Use Access Keys for programmatic access (CLI/SDK) and avoid sharing them.
- Regularly audit permissions using IAM Credentials Report and IAM Access Advisor.
- Never share IAM users and access keys.

## Summary
- Users: Represent individuals within your organization.
- Groups: Organize and apply permissions to multiple users simultaneously.
- Policies: Define permissions for actions on AWS resources.
- Roles: Assign permissions to AWS services securely.
- Security: Enhance account security with strong passwords, MFA, and IAM best practices.
- AWS CLI: Command-line tool for managing AWS resources.
- AWS SDK: Language-specific APIs for integrating AWS services into applications.
- Access Keys: Provide programmatic access to AWS services.
- Audit: Regularly review and audit IAM permissions for better security.
