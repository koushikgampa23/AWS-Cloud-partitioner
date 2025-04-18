# AWS-Cloud-partitioner
## Introduction
### What is server composed of?
    compute - cpu
    memory - ram
    Storage Data - files or 
    Data stored in structured way - database
    Network: router, switches, dns server
### IT terminologies
    Network - bunch of cables, routers and servers connected with each other
    Router - A networking device that forwards data packets between computer networks.They where to send your packets on internet.
    Switch - Takes a packages and sends it to the correct server/client on your network
    if we put all the things together
        Our client will send the data to the router, the switch will know to which computer in your to send data.
### Problems with traditional IT approach
    Pay for the rent for the data center
    Pay for power supply, cooling, maintanance
    Adding and replacing hardware takes time
    Scaling is limited
    Hire 24/7 team to monitor the infrastructure
    How to deal with disasters? (earthquake, powershutdown, fire..)
    We can eliminate all this difficulties by using cloud.
### What is cloud computing
    Cloud computing is the on demand delivery of compute power, database storage, applications and other IT resources.
    Through cloud service platform pay-as-you-go pricing.
    We can provision exactly type and size of computing resources as you need.
    you can access as many resources as you need almost instantly.
    Gives simple way to access servers, storage, databases and a set of application services.
    AWS owns and maintains the network connected hardware required for these application services, while you provision and use what you need via web application.
### Types of clouds
    Private cloud
        Cloud services used by single organization, not exposed to public
        Complete control
        Security for sensitivity application
        Meet specific Business needs
    Public Cloud
        AWS, Azure, Google cloud
        Cloud service owned and operated by a third party cloud service provider delivered over internet.
        Six advantages of cloud computing
    Hybrid Cloud
        keep some servers on premises and extend some capabilities to the cloud.
        Control over sensitive assests in your private infrastructure.
        Flexibility and cost effectiveness of the public cloud.
### Five Characterists of Cloud
    On demand self service
        Users can provision resources and use them without human interaction from the service provider
    Broad network access
        Resources avaliable over the internet and can be accessable by diverse client platforms
    Multitenancy and resource pooling
        Multiple customers can share the same infrastructure and application with security and privacy.
    Rapid elasticity and scalability
        Automatically and quickly acquire and dispose resources when needed.
        Quickly and easily scale based on demand
    Measured Service
        Usage is measured, users pay correctly what they have used.
### Six advantages of cloud computing
    Trade capital expense(CAPEX) for operation expense (OPEX)
        Pay on Demand dont own hardware
        Reduced total cost of ownership(TCO) and operational expense (OPEX)
    Benefits from massive economics of scale
        Prices are reduced as AWS is more efficient due to large scale
    Stop Guessing capacity
        Scale based on actual measured usage.
    Increase speed and agility
    Stop spending on running and maintaining data centers
    Go global in minutes: leverage the global infrastructure
#### Problems solved by cloud
    Flexibility: change resources types when needed
    Cost effectiveness: pay as you go, for what you use
    Scalabitliy: accomate larger loads by making hardware stronger or adding additional nodes.
    Elasticity: Ability to scale out and scale in when needed
    High avaliablity and fault tolarance: built around data centers
    Agility: Rapidly develop, test and lauch the software applications
## Types of cloud computing
    Infrastructure as a Service(IaaS)
        Provide building blocks for IT
        Provides networking, computers, data storage, space
        highest level of flexibility
        Easy with traditional on premises IT
    Platform as a Serivce(Paas)
        Removes the need for your organization to manage underlying infrastructure
        Focus on deployment and management of the application
    Software as a Service(Saas)
        Completed product that is run and managed by service providers
    Difference between this three
        On premises is the one managing operations like applications, data, runtime, middleware, os, virtualization, servers, storage, networking
        IaaS: Applications, data, run, middleware, os managed by you
              os, virtualization,servers, storage, networking - managed by others(AWS)
        PaaS: Applications, Data is manage by us
              Runtime, Middleware, OS, Virtualization, Servers, Storage, Networking - managed by others(AWS)
        SaaS: Everything is managed by AWS
    Example of cloud computing
        Iaas:
            Amazon EC2(on AWS)
            GCP, Azure, Rackspace, Digital Ocean, Linode
        Paas:
            Elastic BeanStack(on AWS)
            Heroku, Google App Engine (GCP), windows Azure(Microsoft)
        Saas:
            Many AWS services (ex: rekognition for machine learning)
            Google apps(Gmail), Drop Box, Zoom
### Pricing of the cloud - overview
    Aws has 3 pricing models, following pay-as-you-go model
        Compute: pay for the compute time
        Storage: pay for data stored in the cloud
        Data transfer OUT of the cloud: data transfer IN is free
        Solves the expensive issue of traditional IT
![tcsglobal udemy com_course_aws-certified-cloud-practitioner-new_learn_lecture_20054392](https://github.com/user-attachments/assets/9b2fae2e-fa47-4a53-8ce0-b1429f201490)
### AWS facts
    In 2023, AWS has $90 billion annual revenue
    10lakh active users
### AWS Cloud use cases
    Allows us to build sophisticated and scalable applications
    Applicable for diverse set of industries
    Use cases include
        Enterprise It, Backup and restore, Big data analytics
        Web hosting, mobile and social apps
        gaming
    Aws global infrastructure
        AWS Regions - has regions all around the world, Names can be us-east-1, eu-west-3, A region is cluster of data centers, Most AWS services are region scoped
        AWS avaliablity zones
        AWS Data Centers
        AWS Edge locations/points of presence
    How to choose an AWS region?
    If you want to lauch a application in which region will you lauch?
        Compliance with data governance and legal requirements: Data leaves a region without your explict permission
        Proximity to customers: reduced latency
            if the majority of your application users are from america, its better to deploy in america or near by areas that redues the latency
        Avaliable Services within a region: new services and new features are not available in all regions.
        Pricing: Pricing varies from region to region and is transparent in the service pricing page.
    Aws avaliablity zones:
        Each region has max availablity zones(min is 3, max is 6)
        Each avaliablity zone is one or more discrete data centers with redundent power, networking and connectivity.
        In simple terms a availibity zone can be a combination of 1 or more data centers that has constant power, networking and connectvity
        They are seperate from each other, so that they are isolated from each other.
        They are connected with high bandwidht, ultra-low latency networking.
    Aws points of presence
        Aws 400+ points of presence in 90+ cities across 40+ countries
        content is delivered to end user with low-latency
### Glimpse of AWS console
    AWS Global services
        Identity and access management(IAM)
        Route S3(DNS service)
        CloudFront(Content Delivery Network)
        WAF(Web application firewall)
    Most AWS services are region scoped
        Amazon EC2(Iaas)
        Elastic Bean(Paas)
        lambda(Faas) #function as a service
        Rekognition(Saas)
    There are some service like Route S3 this service region is global we cant modify region, where aws ec2 service we have option to select a region.
    To see detailed list of service that are offered in each region we can
        search aws global infrastructure -> click on regions and AZs tab -> navigate below and click on See detailed list of offerings at all AWS locations link -> click on region you want
## Shared Responsibility model
    Customer - you has the customer your are responsible for the security IN the cloud
               that includes how are configuring security, firewall, os and everything
    AWS - Responsible for the security OF the cloud
          All the infrastructure, hardware, software, there own internal security
    ![tcsglobal udemy com_course_aws-certified-cloud-practitioner-new_learn_lecture_20263094](https://github.com/user-attachments/assets/1118b306-a731-4522-a507-6596f0bb0a5a)

## Quiz
    1) Which Global Infrastructure identity is composed of one or more discrete data centers with redundant power, networking, and connectivity, and are used to deploy infrastructure?
        a) edge locations b) availibity zones c) Regions
        Ans: b
    2) Which of the following is NOT one of the Five Characteristics of Cloud Computing?
        a) rapid elasticity and scalability b) multi tenancy and resource pooling c) Dedicated agent support to help you deploy applications d) on demand self service
        Ans: C
    3) Which are the 3 pricing fundamentals of the AWS Cloud?
        a) compute, storage and data transfer inside the AWS cloud
        b) compute, networking and data transfer our of the aws cloud
        c) compute, storage and data transfer out of the aws cloud
        d) Storage, functions and data transfer in the aws cloud
        Ans: C
    4) Which of the following options is NOT a point of consideration when choosing an AWS Region?
        a) Compliance with data governance
        b) latency
        c) capacity avalibility
        d) Pricing
        Ans C
        Capacity is unlimited in the cloud, you do not need to worry about it. The 4 points of considerations when choosing an AWS Region are: compliance with data governance and legal requirements, proximity to customers, available services and features within a Region, and pricing.
    5) Which of the following is NOT an advantage of Cloud Computing?
        a) CAPX for operational expanse
        b) Train your employees less
        c) Go global in minutes
        d) stop spending money on running and maintaing data centers
        Ans: B
        You must train your employees more so they can use the cloud effectively.
    6) AWS Regions are composed of?
        a) one or more discrete data centers
        b) two or more edge locations
        c) Three or more availablity zones
        Ans: C
        avalibity zones are composed of one or more discrete data centers, and Aws regions is composed of three or more avaliability zones 
    7) which of the following services as global scope
        a) Ec2 b) IAM c) lamda d) rekognition
        Ans: B
    8) What is cloud computing?
        a) Rapidly develop, test and deploy applications
        b) Automatic and quick ability to acquire resource as you need them and release resources when no longer need them
        c) on deman avalibilty of computer system resources, espically data storage, and compute power, without direct active management by the user
        d) change resource types when needed
        Ans: C
    9) What defines the distribution of responsibilities for security in the AWS Cloud?
        Ans: The shared reponsibilty Model
    10) A company would like to benefit from the advantages of the Public Cloud but would like to keep sensitive assets in its own infrastructure. Which deployment model should the company use?
    Ans: Hybrid cloud
    11) What is NOT authorized to do on AWS according to the AWS Acceptable Use Policy?
    Ans: Run analytics on stolen data
## IAM - Identity and Access Management
    It is a Global service
    Root user is created by default, shouldnt be used or shared
    Users are people within your organization and can be grouped
    Groups contains only users not other groups
    Users doesnot have to belong a group and user can belong to muliple groups
    Example:
        suppose there is a company of six people alice, bob, charles, david, edward, fred
        since alice, bob, charles are developers we can group together as developers
        since david, edware work together in operations we can group them together as operations
        fred works individual doesnot belong to any group
        Suppose charles and david together they can be group as audit team
### IAM permissions
    Why do we need users and groups in aws?
        Because we want to allow them to use our aws account with least privileged access.
    To allow them to use we need to give permissions
    Users or Groups can be assigned JSON documents called policies
    These policies define the permissions of the users.
    In AWS you apply the least privilege principle: dont give more permission than user needed.
    policies
    ![tcsglobal udemy com_course_aws-certified-cloud-practitioner-new_learn_lecture_20054584](https://github.com/user-attachments/assets/b4e13352-87ac-4fa4-8d99-9825577281a4)
    Practical
        Aws console -> Iam -> User -> Create User
        on the top right if i see it is global no need to select the region, that means if you create a iam user he can be accesible across all regions
### Creating IAM User
    Navigate login to AWS console -> search IAM service -> Users -> Create User
    page1:
        username - koushik
        check the provide access to the aws management console
        Select i want to create Iam User
        auto generate password or custom password anything
        Users must create a new password at next signin check it
    Page2:
        click on create group button
        group name
        add permission policy to the group
        select Administrator access
        click next
        check box the group and create user
        copy the credentials 
    Login Iam user
        Go to IAM dashboard
        on the right side copy the signurl for iam users
        It is recommended to create a alias name to customize the url
        paste the url in the private window and enter the credentials
        Now iam able to login as Iam user
### IAM policy inheritance
    alice, bob, charlies - developers group
    David, edwin - testing group
    fred - individual
    charlies, David are also from operational group
    That means charlies will have polices from both developers group and operational groups
### IAM Policy Structure
    Version: Policy language verison, always include "2012-10-17"
    Id: Identifier for the policy (optional)
    Statement: One or more individual statement(required)
    Statement consists of:
        sid: an identifier for the statement(optional)
        Effect: whether the statement allows or denies the access(Allow, Deny)
        Principal: account/user/role to which this policy applied to
        Action: list of actions this policy allows or denies
        Resource: list of resources to which the actions applies to
        Condition: conditions for when this policy is in effect(optional)
![tcsglobal udemy com_course_aws-certified-cloud-practitioner-new_learn_lecture_26623452](https://github.com/user-attachments/assets/52b5b4ab-222d-4eca-8fed-96c1d49002d2)
### IAM policies handon Permission Add and delete(practical)
    Login as root user and IAM user, one in browser and one in private window.
    Remove administrative access of IAM user from root user account and refresh the IAM User account and try to access the IAM dashboard, we get an error you dont have enough permissions.
    Instead of adding user to admin group this time try adding attach policy directly option and select IAMReadOnlyAccess
    Now the IAM user cannot delete the user he only has read only access
#### Create policies
    Navigate polices -> create policy
    Page1:
        select service IAM
        use search or open dropdown options and add
        add listuser, getuser
        Resources - all
        create policy
    Page2:
        Policy Name BasicUser
    Now open user delete the previous polices, click on add permission -> choose add permission -> attach policies directly
    Search for BasicUser and add permission to the user
#### IAM Password policy
    Strong password = high security for the account
    In Aws you can setup password policy:
        set a minimum password length
        Require specific character types:
            including uppercase letters
            lowercase letters
            numbers
            non-alphanumeric characters
        Allow all IAM users to change their own passwords
        Requires users to change password after some time(password expiration)
        Password reuse
### Multi factor authentication - MFA
        Users have access to your accounts and can possibliy change or delete your resources in AWS account
        You want to protect your root users and IAM users
        MFA = password you know + security device you own
        Main benefit of MFA
            if a password is stolen or hacked, the account is not compromized.
    MFA devices options in AWS
        Virtual MFA device
            Google Authenticator (both apps support of  multiple tokens in a single device)
            Authy
        Universal 2nd Factor(U2F) Security Key
            Yubikey(looks like pendrive a physical machine)
            - support for multiple root and IAM users with a single security key
        Hardware key Fob MFA device
            -looks like a pacer and has password in it.
#### Hands on password policy
    Add password policy: Navigate IAM -> Account settings -> Edit password policy
    Add MFA to account: Click on user name -> click Security credentials -> Now you can assign MFA
### How to access your aws account?
    3 options available:
        AWS console management(protected by password+ MFA)
        AWS command line interface(CLI): protected by access key
        AWS software Developer kit(SDK): -for code protected by accesskey
    Access keys are generated through AWS console
    Users manage there own access keys
    Access keys are secret, just like password, dont share with any one.
    Access Key ID - username
    Secret Access Key - password
#### Whats the AWS cli?
    A tool that allows you to interact with the AWS using commands in comand line
    Direct access to the public API's of AWS services
    You can develop scripts to manage your resources
#### What is AWS SDK
    AWS Software Developement Toolkit(SDK)
    Language specific API(set of libraries)
    Enables you to access and manage AWS services programatically
    we are not using it in a terminal, but we are embedding within our application
    Supports - Javascript, Ruby, python, java, c++, Node js
        Mobile SDks(android, ios)
        Iot Devices(Embedded C, Arduino)
### AWS CLI setup
    Step1) Install AWS CLI
        Search for AWS CLI for windows and open a aws docs website and download msi version for windows
        Check using aws --version
    Step2) Generate access key
        navigate to create access key
        click on username -> click security crendentials -> scroll down -> click on generate accesskey
    Step3) Click on command line interface, check the i understand box
        Click on generate accesskey
        This is the only time where we can be able to access it, make sure to download
    Step4) use this cmd
        aws configure 
        enter credentials
    Step5) Verify it
        aws iam list-users
    Step6) Optional try removing Administrative access to the IAM user, try aws iam list-users it wont work it shows you dont have enough permissions to do this.
### AWS cloud shell
    It is an alternative for using AWS CLI instead of running on the computer we can open the cloud shell in the aws console portal
    Cloud shell is not available in all regions make sure to use the proper region if i want to use
    if i use ls it shows nothing
    we can use echo "test" > demo.txt(it will a file demo.txt with text test)
    even if i restart the cloud shell the files will stay there
    You can even download the files
    Click on actions -> click on download file -> enter file location, then we can download it
#### IAM Roles for services
    Some AWS services will need to perform actions on your behalf
    To do so, we will assign permissions to AWS services with IAM Roles
    Common Roles:
        EC2 instance roles
        lambda function roles
        Roles for CloudFormation
    In simple terms for EC2
        Allows Ec2 instance to perform AWS services on behalf of you
    HandsOn:
        navigate IAM -> Roles -> Create Roles -> Click AWS service -> Use Case -> EC2
        Page2: Add policy like AdministrativeAccess or IAMReadOnlyAccess
        Add role name and click on create role
### IAM Security Tools
    We can generate 
    IAM credentials Report(account-level)
        A report that lists all your accounts users and the status of their various credentials
    IAM Access Advisor(user-level)
        Access Advisor shows the service permissions granted to a user and when those services were last accessed.
        You can use this to revise the permissions
    Handson:
        IAM credentials Report: navigate IAM -> scroll down -> click on credentials report -> download credential report
        Access Advisor: navigate IAM -> Users -> Click on any user -> Last Accessed tab
### IAM Best practises
    Dont use root account except for aws account setup
    One physical user = one AWS account
    Assign users to groups and assign permissions to groups
    Create a strong password policy
    Use and enforce the use of MFA
    Create and use Roles for giving permissions to AWS services
    Use AccessKeys for programmatic Access(CLI/SDK)
    Audit permissions of your account using IAM Credentials Report and IAM Access Advisory
    Never share IAM users and accesskeys
### Shared Responsibility Model for IAM
    Aws responsible: Infrastructure(global network security), Configuration and vulnerability analysis, Compliance validation
    You: Users, Groups, Polices, management and monitoring, Enable MFA on all devices, Use IAM tools to assign permissions, Analyze access patterns and revise the permissions
### IAM Summary
    Users: mapped to a physical user, has a password for AWS console
    Groups: Groups only contain users
    Polices: JSON documents that outlines permissions of users or groups
    Roles: for EC2 instance or AWS Services
    Security: MFA + Password Policy
    AWS CLI: manage your AWS service using command line
    AWS SDK: mangage your AWS services using programming language
    Access Key: Access Aws using cli or SDK
    Audit: IAM Credentials Report and IAM Access Advisor(Lat access)
### Quiz
    What is a proper definition of IAM Roles?
        An IAM entity that defines set of permissions for making AWS service request, that will be used by AWS Services
    Which answer is incorrect regarding IAM User?
        a)IAM Users can belong to multiple groups
        b)Iam users dont have to belong to a group
        c)IAM users have policies assigned to them
        d)IAM users access AWS with the root account credentials
        Ans: D IAM Users access AWS using a username and a password.
    Under the shared responsibility model, what is the customer responsible for in IAM?
        a) Infrastructure security
        b) Compliance validation
        c) configuration and vulnerability analysis
        d) Assigning users proper IAM polices
        Ans: D
### AWS Budget Setup
    Search billing and cost management
    if you see all the access denied for IAM User
    Login to root account 
    Search billing and cost management, now click on the username -> account -> scroll down and edit IAM user/role access to billing information
    Give access to IAM User, Now IAM user can access billing details
    How to check bills
        navigate Billing and cost management -> Bills -> search by month -> search by service
    Click on free tier to check what is free and how much did we we utilize
    Now Click on Budget -> Click on create budget -> use template(simplified), Zero spend budget, create budget
    Best to see the expenses 1)Bill 2) Free tier checks
## Amazon EC2
    Ec2 it is the most popular AWS offering
    EC2 = Elastic Compute Cloud = Infrastructure as a Service
    It mainly consists of in the capability of:
        Returing Virtual Machine(EC2)
        Storing data on virtual drives(EBS)
        Distributing load across machines(ELB)
        Scaling the services using auto scaling group(ASG)
    knowing EC2 is the fundamental to understand how cloud works
### EC2 Sizing and configuration options
    operating system(OS): Linux, Windows, or Mac Os
    how much compute power and cores (CPU)
    how much randam access memory (RAM)
    How much storage space:
        Network attached (EBS & EFS)
        hardware(EC2 instance store)
    Network card: speed of the card, public Ip address
    Firewall rules: security group
    Bootstrap script: EC2 User data
    It is possible to bootstrap our instance using an ec2 user data scripts
    bootstrapping means lauching commands when a machine starts
    The script only run once at the instance first start
    EC2 user data used to automate boot tasks such as:
        Installing updates
        Installing software
        Downloading common files from internet
    The Ec2 user data scripts run with the root user
    EC2 instance types
![tcsglobal udemy com_course_aws-certified-cloud-practitioner-new_learn_lecture_20055638](https://github.com/user-attachments/assets/d536b093-1543-4b68-8ef4-dc536ace206e)
    t2.micro is part of aws free tier(upto 750 hours per month)
### EC2 handson
    Launching an EC2 instance running linux
    Navigate EC2 -> Dashboard -> instances -> lauch instances
    Add name: first_instance
    os: amazon_linux
    Architecture: 64 bit
    instance type: t2.micro (1cpu, 1gb ram eligible for free tier)
    keyvalue: click on create keyvalue, name: ec2 tutorial, algorithm: rsa, file type: pem, download the pem file
    firewall security: allow HTTP traffic
    In the advanced details: scroll down and add this code in user data box
        #!/bin/bash
        # Use this for your user data (script from top to bottom)
        # install httpd (Linux 2 version)
        yum update -y
        yum install -y httpd
        systemctl start httpd
        systemctl enable httpd
        echo "<h1>Hello World from $(hostname -f)</h1>" > /var/www/html/index.html
    This script will be exectuted when the instance started and it will run once once at the end of the lifecycle.
    It will update, install httpd webserver, create a index.html file
    We can start and stop the instances, The public ip address will be changed when ever we stop and start the instance, but the private ip address will not change
### AWS instance types
    AWS instance have this naming conventions
        m5.2xlarge
        m: instance class
        5: generation
        2xlarge: size within the instance class
    General Purpose:
        Great for web servers or code repositories
        Balanace Between:
            Compute
            Memory
            Networking
        t2.micro is the general purpose instance
    Compute optimized:
        Great for compute instance tasks that requires high performance processors:
            Batch processing workloads
            Media transcoding
            High performance web servers
            High performance computing(HPC)
            Scientific modeling and machine learning
            Dedicated Gaming servers
            C series(Cpus)
    Memory Optimized:
        Fast Performance for workloads that processes large data sets in memory
        Use Cases:
            High Performance, relational/non-relational databases
            Distributed web scale stores
            In memory databases optimized for Business Intelligence(BI)
            Applications performing realtime processing of big unstructured data
            R series(Ram)
    Storage Optimized
        Great for storage instensive tasks that require high, sequential read and write access to large data sets on local storage
        Use Cases:
            high frequency online transcation processing(OLTP) systems
            Relational and non-relational databases
            Cache for in memory database(for example redis)
            Data warehousing applications
            Distributed file system
            D series(Disk)
### Security Groups
    Security Groups are the fundamental of network security in AWS
    They control how traffic is allowed in or out of ec2 instance
    security groups only contains allow rules
    Security groups rules can reference by Ip or security group
    They control inbound traffic and outbound traffic
    They are acting as a firewall on EC2 instances
    They regulate:
        Access to ports
        Authorized IP ranges - IPV4 and IPV6
    Can be attached to multiple instances and an instance can have multiple security groups
    Locked down to a region/ VPC combination
    Does lives outside EC2 instance and if traffic is blocked the EC2 instance wont see it.
    Its good to maintain seperate security group for SSH access.
    if your application is not accessible(time out), then its a security group issue
    if your application gives connection refused error, then its a application error or its not launched
    By default all inbound traffic rules is blocked
    By default all outbound traffic is authorized
![tcsglobal udemy com_course_aws-certified-cloud-practitioner-new_learn_lecture_20055658](https://github.com/user-attachments/assets/edfd9c54-0df4-4665-b761-3fa115ca787d)
![tcsglobal udemy com_course_aws-certified-cloud-practitioner-new_learn_lecture_20055658 (1)](https://github.com/user-attachments/assets/2c756c79-6bda-437b-8a3d-e1b5c597f59d)
### Classic Ports to know
    22=SSH (Secure shell) - login to EC2 instance
    21=FTP (File Transfer Protocal) - upload files into a file share
    22=SFTP(Secure) - upload files using SSH
    80=HTTP - access unsecured websites
    443=HTTPS - access secured websites
    3389=RDP(Remote Desktop Protocal) - login into windows instance, 22 - login into linux instance
    Handson Security Groups
        EC2 -> Network and Security -> Security Groups
        Click on create security group
        add in Inbound rules http source anywhere
        add in outbound rules allow traffic
![tcsglobal udemy com_course_aws-certified-cloud-practitioner-new_learn_lecture_20055692](https://github.com/user-attachments/assets/156931ce-7b71-4cf2-a89a-e27835e1296b)
### SSH setup
    Excute this command in cmd
        ssh (if command not found then we have to use putty since your windows dont have ssh)
        

    

    
    
    


    
    

    
    
    
    
        
    
        
    
    
    
    
    
        
    
    
    
    

            
        
    

    
    
    

    
    
    
        
        
    
        
        
    
    
