
# Deploy a high-availability web app using CloudFormation

In this project, you’ll deploy web servers for a highly available web app using CloudFormation. You will write the code that creates and deploys the infrastructure and application for an Instagram-like app from the ground up. You will begin with deploying the networking components, followed by servers, security roles and software.  The procedure you follow here will become part of your portfolio of cloud projects. You’ll do it exactly as it’s done on the job - following best practices and scripting as much as possible. 

## Infrastructure Diagram

![Infra-diagram](https://github.com/user-attachments/assets/62555c18-3e33-41c7-9181-5baf2c45958f)


## Infrastructure Overview

This project uses CloudFormation to provision the following resources:
1. VPC with public and private subnets
2. NatGatways, InternetGatway, Routable
3. LB for HTTP/HTTPS traffic
4. IAM roles and policies
5. EC2 for Web Application
   
We have two stages for this deployment 

   1. Network configuration by network team
   2. Application setup by DevOps team

      
### Dependencies

1. AWS CLI installed and configured in your workspace using an AWS IAM role with Administrator permissions (as reviewed in the course).

2. Access to a diagram creator software of your choice.

3. Your favorite IDE or text editor ready to work.

### Infrastructure setup and application deployment 

infrastructure creation using the provided scripts, follow the steps below:

1. Make the script executable:
    chmod +x <scripts.sh>

2. ./create.sh StackName ParameterFile TemplateFile - run create.sh with three parameters(StackName, Parameter and Template files) to create new CF stack
3. This script creates a new stack with the provided parameters.
4. Update an existing stack if there are any changes in parameter file(./update.sh StackName ParameterFile TemplateFile)
5. Deploy a stack - ./deploy.sh StackName ParameterFile TemplateFile
   
The deploy.sh script checks if the stack already exists. If it does, the script will update the stack; if it doesn't, it will create a new stack. It very useful for automation like CI/CD pipeline


## Testing

We can access the Application through DNS url - http://udacit-webap-igb3jrkeujvh-1389014971.us-east-1.elb.amazonaws.com/


## Shoudown the infrastructure

Delete a stack:
./delete.sh StackName

Use the delete.sh script to delete a stack. The script only requires one parameter: the name of the stack you wish to delete.



