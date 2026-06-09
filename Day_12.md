
************** (8 Jun 2026) ********************

**1**. Self Intro, Roles and Resposibilities, Day-to-Day activities  
2. Python experience - I have Training Only.  
3. What is the cmd to build the Python packages -> (python -m build)  
4. How to create virtual environment in python -> (python3 -m venv .venv) Note: (.venv) is the standard name for the environment folder, but you can replace it with any name you prefer.
5. Experence with - Flinx, spark, -No, I already informed about it.  
**6**. What is the use of Terraform state file.  
**7**. What is the difference b/w input and output variables. -> (The main difference between input and output variables is the direction of data flow: input variables act as parameters that you pass into your configuration, while output variables act as return values that expose information after the configuration has run.)  
**8**. Scenario: Lets say, you are creating 2 resources - security group and EC2 instance, you want to reference SG instance in the EC2 instance. How would you refrence.  
   By passing  [aws_security_group.web_sg.id] to VPC_id's of EC2 => web_sg is alias name of SG.  
**9**. While running "Terraform plan" It show - 2 to destroy, But you haven't done any change. How would you resolve it.
   When terraform plan shows "2 to destroy" despite no intended changes, it typically means there is a mismatch between your code (desired state) and your state file (last known reality).  
   There could be reasons like:  
   1) .tf file was moved / renamed or Deleted 2) Renamed a Blocked or moved to module 3) Manual change on cloud. 4) unnessesary changes -that can be ignored via life-cycle.  
   => Use moved block for moved files / blocks.  
   => (terraform apply -refresh-only) -> looks at what is actually running in your cloud right now and updates your Terraform records to match.  

10. What are the services you have experence with in AWS -> IAM, EC2, VPC, S3, EKS.  
11. How do you create cross account role in IAM  
    Cross-account IAM roles are used to grant secure, temporary access to AWS resources across different accounts without sharing permanent credentials.  
    Creating a cross-account IAM role involves two main steps:
    -> configuring a role in the Destination account (the one with the resources) and
    -> granting permission to an identity in the Source account (the one that needs access).  
12. What is web identity role.
    A web identity role (also known as a Web Identity Federation role) is an AWS IAM role that lets users authenticated by an external identity provider (IdP) securely access AWS resources without needing an AWS IAM user account. 
Instead of creating AWS credentials for everyone, the role trusts token signatures from public identity providers like Google, Facebook, or Amazon, as well as any OpenID Connect (OIDC) compatible service.

**13.** Let say, You have an IAM Role, it has both Allow and Deny for the same service and same user, which one will work -          (Deny).
14. In NACL - 101 -> allow ; 102 -> Deny ; which one will work.
    Rule 101 (Allow) will work: AWS Network Access Control Lists (NACLs) process rules in numerical order, starting from the lowest number. As soon as a packet matches a rule, the evaluation stops, and that rule is applied.  
    Best Practice TipAlways leave gaps between your rule numbers (e.g., 100, 110, 120). This allows you to easily insert new rules later if you need to override an existing rule.  
15. Is it possible to block the IP's in security groups. - Yes


Q) Is it possible to block the API's in security groups.  
   No, it is not possible to block specific APIs or API paths using Security Groups. But, you can use Security Groups to restrict access to the entire API server.
   Security Groups operate at Layer 4 (Transport Layer) of the OSI model. They only understand IP addresses, protocols (TCP/UDP), and ports. Because they cannot inspect the content of the data payload (Layer 7 - Application Layer), they cannot differentiate between a request to GET /users and a request to POST /admin/delete.  

**16.** What actions are allowed in Security Groups. Is it allow or Deny.?
    Only ALLOW actions are supported in Security Groups.Security Groups act as stateful firewalls that operate on an implicit deny-all basis. You cannot write a rule to explicitly "Deny" traffic.
    Note: If you absolutely need to explicitly block a specific IP address or port, you must use a Network Access Control List (NACL) or AWS Network Firewall instead of a Security Group. NACLs support both Allow and Deny actions.

**17.** what are fields you see on security group.?
18. What are the Other services, you have experence with in AWS - EC2, S3, VPC, EKS, Lambda.
19. How will you expose Lambda URL to public.
20. In EC2 what is use of User Data.
    EC2 User Data is used to automate bootstrap tasks when an instance launches for the first time.
21. How will you optimize a docker file.
22. In K8s, you are deploying new package - Application is not coming up, what will you do.
      1. Check the Pod Status -> "kubectl get pods -n (namespace)"
      2. Inspect the Pod Events -> "kubectl describe pod (pod-name) -n (namespace)"
      3. Check Application Logs -> "kubectl logs (pod-name) -n (namespace)
      4. Verify Health Probes

**23**. Commands to identify the logs and error message.
24. Difference b/w Nodeport, clusterIP and LoadBalancer.
25. Can you explain the Network, How the Master and worker Node are connected. How all these are communicating.
    Architecture - explained ->
26. Asked for Flow of Networking -> from Hitting a URL till pod reach.  
27. Lets say you have created a New EC2 instance / worker node , it has kublet running, but that kublet is not able to connect with the Master. How do you fix.
**28.** What service convert the Host Name to IP address.
      DNS - Route 53 service
29. In Route53 - which routing policy will convert.
    All routing policies in Amazon Route 53 will convert (resolve) a host name into an IP address or target resource. That is the primary function of any DNS policy.

30. Do you exp with ArgoCD - No exp.

##

Done

    
    


