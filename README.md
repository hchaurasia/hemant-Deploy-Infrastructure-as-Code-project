
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
5. 
Use the create.sh script to create a new CloudFormation stack.
The script requires three parameters (such as StackName, ParameterFile, and TemplateFile). You will need to pass these parameters as per the instructions in the script.
./create.sh StackName ParameterFile TemplateFile

This script creates a new stack with the provided parameters. Make sure you include IAM capabilities


## Testing

No tests required for this project.

## Project Instructions

1. Design your solution diagram using a tool of your choice and export it into an image file.

2. Add all the CloudFormation networking resources and parameters to the `network.yml` and `network-parameters.json` files inside the `starter` folder of this repo.

3. Add all the CloudFormation application resources and parameters to the `udagram.yml` and `udagram-parameters.json` files inside the `starter` folder of this repo.

4. Create any required script files to automate spin up and tear down of the CloudFormation stacks.

5. Update the README.md file in the `starter` folder with creation and deletion instructions, as well as any useful information regarding your solution.
   
6.  Submit your solution as a GitHub link or a zipped file containing the diagram image, CloudFormation yml and json files, automation scripts and README file.

## License

[License](LICENSE.txt)
