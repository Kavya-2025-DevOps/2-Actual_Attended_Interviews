******************** Date: 05 Jun ***************************
Role: Aws Admin 

Governance & Multi-Account Management (Control Tower & Config)

Scenario 1: You are tasked with onboarding a new business unit that requires three separate environments (Dev, Test, Prod). How would you use AWS Control Tower and Account Factory to ensure these accounts automatically adhere to corporate security guardrails from day one?
Scenario 2: A developer accidentally launches an unencrypted S3 bucket in a member account. Describe how you would use AWS Config and specialized Remediation Actions to automatically detect and fix this non-compliant resource without manual intervention.
Scenario 3: Your organization needs to ensure that no resources are ever created outside of the us-east-1 and eu-west-1 regions. How would you implement this restriction across the entire AWS Organization using Control Tower or Service Control Policies (SCPs)?
Infrastructure as Code (Terraform)

Scenario 1: You are managing a complex environment with Terraform. A team member manually changed a Security Group rule in the AWS Console. How do you identify this configuration drift, and what specific steps do you take to bring the real-world infrastructure back in sync with your code?
Scenario 2: You need to deploy the same VPC architecture across 10 different AWS accounts. How would you structure your Terraform modules and manage your backend state files to ensure the code is reusable and the state is stored securely and locked?
Scenario 3: During a terraform apply, the process crashes halfway through, leaving some resources created and others in a "tainted" state. How do you troubleshoot the state file to ensure the environment isn't left in a corrupted or unstable condition?
Identity, Security & Compliance (IAM & S3)

Scenario 1: A third-party security auditing tool needs read-only access to your AWS environment. How would you design a secure IAM Role with Cross-Account access using External IDs to provide this access without sharing long-term credentials?
Scenario 2: An S3 bucket containing sensitive logs must be protected against accidental deletion, even by an administrator. How would you configure S3 Versioning, MFA Delete, and Object Lock to meet this requirement?
Scenario 3: You notice unauthorized API calls being made in a sub-account. Walk through your process of using CloudTrail and IAM Access Analyzer to track down the source and tighten the permissions.
Monitoring & Network Analysis (CloudWatch & VPC Flow Logs)

Scenario 1: An application team reports that their EC2 instance cannot connect to an RDS database. How would you use VPC Flow Logs and CloudWatch Logs Insights to determine if the traffic is being rejected by a Security Group or a Network ACL?
Scenario 2: You need to create a dashboard that alerts the team if 4xx errors on an S3 bucket exceed a certain threshold. How would you set up the CloudWatch Metric Filter and Alarm to notify the team via Slack or Email?
CI/CD & DevOps Integration (GitHub & Azure TFS)

Scenario 1: You are migrating your automation scripts from Azure TFS to GitHub Enterprise. How would you redesign a manual deployment gate in TFS into a GitHub Actions workflow using "Environments" and "Required Reviewers"?
Scenario 2: Your Terraform pipeline in GitHub Actions needs access to AWS to deploy resources. Explain how you would use OIDC (OpenID Connect) instead of storing hardcoded AWS Access Keys in GitHub Secrets.
Containerization (EKS)

Scenario 1: You are asked to assist the dev team with an EKS cluster. A pod is stuck in ImagePullBackOff. How would you troubleshoot the worker node's IAM role or the ECR repository policy to resolve this?
