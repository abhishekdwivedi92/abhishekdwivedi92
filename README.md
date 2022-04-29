Amazon CloudFormation as infrastructure automation or Infrastructure-as-Code (IaC) tool provided by AWS which can automate the setup and deployment of various Infrastructure-as-a-Service (IaaS) offerings on the AWS CloudFormation supports virtually every service that runs in AWS. Through CloudFormation we can set up many AWS Services or configure various workloads like EC2 compute service, the S3 storage service, and the IAM service for configuring access control by using Cloudformation templates.CloudFormation is not the only way to configure and deploy services on AWS. We can handle these processes manually using the AWS command-line interface, API, or Web console.

Advantages of CloudFormation
CloudFormation provides us a range of benefits that make cloud service deployment and management faster and more efficient.

1. Deployment speed

2. Scaling up

3. Service integration

4. Consistency

5. Security

6. Easy updates

7. Auditing and change management

Terms and Concepts
Before we understand the set up of AWS EKS by Cloudformation template, we first know the CloudFormation Template Terms and Concepts, it helps us to understand core concepts around which CloudFormation templates structure resources, variables, and functions.

Stacks: stack is a term which refers to a collection of multiple AWS resources like EC2, S3 storage, and IAM access controls that we can manage together using a single template.
Template: CloudFormation template is simply a text file, which defines how AWS services or resources should be configured and deployed.
Parameters: In order to apply unique settings for each deployment, we can use parameters. Parameters define custom values for each deployment that CloudFormation will apply at runtime.
Change sets: If We want to update a deployment using CloudFormation, we can update the template we used to create the deployment. We can then create a change set, which summarizes the changes that the updated template will apply before making the change.
CloudFormation Template
There are two ways to create a template:

By using a pre-existing template as the foundation.
Writing entirely a new template from scratch.
We are here using a newly created cloudformation template in YAML, which consists of all the important resources required for EKS cluster like parameters, Networking part like VPC, Subnets,Internet Gateway, Worker Node group, etc as shown in the diagram below.

Prerequisite
1. AWS Account.

2. AWS CLI.

3. AWS Keypair

4. Cloudformation Template in yaml.

We can create EKS Cluster through Cloudformation template by two ways:

1. AWS CLI
2. AWS Console.

Steps to create AWS EKS Cluster by using AWS Cloudformation Template in AWS Console.

1. Get clone this repo and do some changes in template such as EKS cluster name, keypair name which you have created in the region, region id, AMI ID and and type of instance you want to as worker node.
2. Save the template.
3. Open AWS console and navigate to AWS Cloudformation
4. Click on create stack.
5. Choose template ready as we are using the created template and specify the location of the template file.
6. Specify stack details. 
7. Configure stack options like Tags, IAM roles for EKS cluster.
8. If we have created the IAM role for our EKS already then uncheck the IAM role confirmation and if not then check the radio to create IAM role for our EKS cluster and click create stack.

Now we can connect to our cluster through AWS CLI. Run command to configure and get access to the AWS account and provide Access-key, secret-key, region name and format for output or we can also create a profile for future use.


