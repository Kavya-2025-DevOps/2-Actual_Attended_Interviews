
************** Tavan Technologies ********************

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
   1) .tf file was moved / renamed or Deleted. 2) Renamed a Blocked or moved to module 3) Manual change on cloud. 4) unnessesary changes -that can be ignored via life-cycle.  
   => Use moved block for moved files / blocks.  
   => (terraform apply -refresh-only) -> looks at what is actually running in your cloud right now and updates your Terraform records to match.  

10. What are the services you have experence with in AWS -> IAM, EC2, VPC, S3, EKS.
11. 
   
