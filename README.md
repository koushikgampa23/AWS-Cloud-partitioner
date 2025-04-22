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
    In the advanced details: scroll down and add this code in user data scripts in user data box
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
    SSH is one of the most important function, that allows you to control remote machine, all using command line
    How to ssh into your EC2 instance windows
        After creating EC2 instance we had downloaded the pem file, go to that location
        Now use this command 
            ssh -i <pemifile> ec2-user@<ec2-instance-public-ipv4-ipaddress>
            ssh -i '.\ec2 tutorial.pem' ec2-user@3.82.146.18
        if promted to enter yes
        Now we are in ec2 instance on windows machine
    Alternative way is use browser
        on the instance click on connect
        it will automatically detect ec2-user
        if i click on connect it will upload a temporary ssh key and establish a connection with it.
### Attach IAM role to EC2 instance
    In the aws console check wheather we had attached any IAM role to the instance or not.
        EC2 -> instances -> instance1 -> In the security tab check IAM role
    if IAM role is not attached then click on 
        actions -> security -> modify Iam role -> Add iam role -> Choose EC2Demo
    If i havent created iam role for ec2 follow this
        IAM -> Roles -> create Role -> choose Trusted entity type, Use case: EC2 -> permission policy: IAMReadOnlyAccess -> EC2Demo
    In the EC2 instance try this command
        aws iam list-users
### EC2 Purchasing Options
    On-demand Instance - short workload, predictable pricing, pay by second
    Reserved(1 & 3 years)
        Reserved instances - long workloads
        Convertable Reserved instances - long workloads with flexible instances
    Savings Plan(1 & 3 years) - commitment to an amount of usage, long workloads
    Spot instances - short workloads, cheap, can lose instances(less reliable)
    Dedicated Hosts - book an entire physical server, control instance placement
    Dedicated Instances - no other customer will share your hardware
    Capacity Reservations - reserve capacity in a specific AZ for any duration
### EC2 on demand
    Pay for what you use
        linux or windows - billing per second, after first minute
        All other operating system - billing per hour
    Has highest cost but no upfront payment
    No long-term commitment
    Recommended for short-term and un-interrupted workloads, where you cant predict how your application will behave
### Reserved Instances
    Up to 72% discount compared to ondemand 
    you reserve a specific instance attributes(Instance type, Region, Tenancy, OS)
    Reservation period - 1 year(+discount) or 3 years(+++discount)
    Payment options - No upfront, partial upfront(++), All upfront(+++)
    Reserved instance scope - Regional or zonal (reserve capacity in AZ )
    Recommended for steady-state usage applications(think database)
    You can buy or sell reserved instances in the market place
    Convertible Reserved instances
        Can change the ec2 instance type, instance family, OS, scope and tenancy
        up to 66% discount
### Ec2 Saving plan
    Get a discount on long term usage(upto 72% - same as RI)
    Commit to certain type of usage(10$/hour for 1 or 3 years)
    Usage beyond EC2 Savings Plans is billed at the on-demand price
    Locked at a specific instance familiy & AWS region(eg i want M5 instance at us-east-1)
    Flexible across:
        Instance Size(m5.xlarge or m5.2xlarge)
        OS(linux or windows)
        Tenancy(Host, Dedicated, Default)
### EC2 spot instances
    can get a discount upto 90% as compared to ondemand
    Instances that you can lose at any point of time if your max price is less than the current sport price
    The MOST efficient instance in AWS
    Useful for workloads that are resilent to failure
        Batch jobs
        Data Analysis
        Image Processing
        Any distributed workloads
        workloads with a flexible start and end time
    Not suitable for critical jobs or databases
### EC2 Dedicated Hosts
    A physical server with EC2 instance capacity fully dedicated to your use.
    allows you use complience requirements and use your exisiting server-bound software licenses
    Purchasing Options
        Ondemand - pay per second for active Dedicated host
        Reserved - 1 or 3 years(No upfront, parital upfront, all upfront)
    This is the most expensive one
    Useful for softwares that has a complicated licensing model(BYOL - Bring Your Own Licence)
    Or the companies that have strong regulatory or complience needs
### EC2 dedicated Instances
    Instances that run on hardware that are dedicated to you.
    May share hardware with other instances in same account
    No control over instance placement(can move hardware after they stop/start)
### Difference between dedicated hosts and dedicated instances
![tcsglobal udemy com_course_aws-certified-cloud-practitioner-new_learn_lecture_20055756](https://github.com/user-attachments/assets/62aed980-d0ec-4598-b47d-45c2fe072c74)
### Ec2 Capacity Reservations
    Reserve on-demand instances capacity in a specific region for any duration
    You always had access to Ec2 capacity when you need it.
    No time commitement(Create/Cancel anytime), no billing discount
    Combine with regional reserved instances and savings plans to benefit from billing discounts
    your charged with on-demand price whether you run instances or not
    suitable for short time, uninterupted workloads that needs to be in a specific Az
### Which type of instance i choose
![tcsglobal udemy com_course_aws-certified-cloud-practitioner-new_learn_lecture_20055756 (1)](https://github.com/user-attachments/assets/b64e9df1-d4bf-4d99-90c9-6fa8718d5aa1)
![tcsglobal udemy com_course_aws-certified-cloud-practitioner-new_learn_lecture_20055756 (1)](https://github.com/user-attachments/assets/b307e2c7-aa47-4d1a-bd15-6649420b6e62)
### AWS charges for IPv4 address
    Starting Feb 1st 2024, there is a charge for all the public IPv4 address created in your account
    0.005$ per hour of public IPv4(~3.6$ for month)
    For new accounts in aws, you have 1 year tier for the EC2 service: 750 hours of public Ipv4 for the first 12 months
    what about IPv6?
        Unfortunatly many of the Internet service provides(ISP) around the world doesnot support IPv6.
    IPv6 there are no charges, since aws want to push IPv6 it started introduced charges on Ipv4
    How to trouble shoot charges?
        Go into AWS bill
        Look into AWS public Ip insights service
        Hands on:
        billing and cost management -> Bills
        
![tcsglobal udemy com_course_aws-certified-cloud-practitioner-new_learn_lecture_46796935](https://github.com/user-attachments/assets/6dc55a20-569b-42de-bc6a-d1d4370dba1e)
### Create public Ip Address
    Search for IPAM -> Amazon VPC IP Address Manager -> IPAM's -> Create IPAM -> Enable Allow VPC IP address Manager -> Select Region -> Create IPAM
    In the IPAM -> Public Ip insights
### Shared responsibility model of EC2
    managed by aws:
        Infrastructure (global network security)
        Isolation on physical hosts
        Replacing faulty hardware
        Compliance validation
    Managed by user:
        Security Group rules
        Operating system patches and updates
        Softwares and utilies installed on the EC2 instance
        IAM roles assigned to EC2 and IAM user access management
        Data security on your instance
### EC2 section - Summary
    EC2 instance: AMI(OS) + Instance Size(CPU+RAM) + Storage + Security Groups + EC2 User Data(Bootstrap scripts that run only one once when ec2 instance created)
    Security Group - Firewall attached to EC2 instance
    EC2 user data - Script launched at the first start of an instance
    SSH - start a terminal into our EC2 instances
    Ec2 instance role : link to IAM roles
    Purchasing options: On demand, Spot, Reserved(standard+convertable), Dedicated host, Dedicated instance
### Quiz
    1.Which EC2 Purchasing Option can provide the biggest discount, but is not suitable for critical jobs or databases?
        Spot Instance
    2.Which network security tool can you use to control traffic in and out of EC2 Instances?
        a.Network Access Control List(NACL)
        b.Identity and access Management(IAM)
        c.GuardDuty
        d.Securtiy Groups
        ans:Security Groups
    3.Under the Shared Responsibility Model, who is responsible for operating-system patches and updates on EC2 Instances?
        Customer
    4.How long can you reserve an EC2 Reserved Instance?
        a.1 or 3 years
        b.anytime between 1 and 3 years
        ans:a,1 year or 3 years terms are available for EC2 Reserved Instances.
    5.A company would like to deploy a high-performance computing (HPC) application on EC2. Which EC2 instance type should it choose?
        Compute Optimized EC2 instances are great for compute-intensive workloads requiring high performance processors, such as batch processing, media transcoding, high performance web servers, high performance computing, scientific modeling & machine learning, and dedicated gaming servers.
    6.Which of the following is NOT an EC2 Instance Purchasing Option?
        a.Reserved Instance
        b.spot instance
        c.on-demand instance
        d.connect instance
        ans:d.connect instance
    7.Which EC2 Purchasing Option should you use for an application you plan on running on a server continuously for 1 year?
        a.Reserved instances
        b.spot instances
        c.ondemand instances
        d.convertible instances
        ans:a.Reserved instances
## EC2 Instance Storage Section
### EBS overview
    EBS - An EBS(Elastic Block storage) volume is a network drive you can attach to your instances while they run
    It allows your instances to persist data, even after its termination
    They can be mounted to one instance at a time(at the CCP level)
    They are bound to a specific availablity zone
    
    Analogy: Think of them as "network USB stick"
    Free Tier: 30 GBS of free EBS storage of type general purpose(SSD) or magnetic per month

    Note: CCP: certified cloud practionior - one EBS can be mouted to only one EC2 instance
    Associate level(Solutions Architect, Developer, SysOps): "multi-attach" feature for some EBS
### EBS volume
    It is a network drive(not a physical drive)
        It uses network to communicate with ec2 instance, which means there might be a bit of latency
        It can be detached from an EC2 instance and attached to another instance quickly
    Its locked to an avaliablity zone(AZ)
        An EBS volume in us-east-1a cannot be attached to us-east-1b
        To move a volume across, you first need to snapshot it.
    Have a provisioned capacity(size in GBs and IOPS)
        You get billed for all the provisioned capacity
        you can increase the capacity of the drive over the time
    One or more EBS volumes can be attached to one instance
    Its not mandatory for EBS volume to attach to a EC2 instance
![tcsglobal udemy com_course_aws-certified-cloud-practitioner-new_learn_lecture_20055762](https://github.com/user-attachments/assets/758efe98-c33c-481e-b3ba-9c0f607dcf35)
### EBS delete on termination attribute
    Controls the EBS behaviour when an EC2 instance terminates
        By default the root EBS volume is deleted (attribute enabled)
        By default, any other EBS volumes attached is not deleted(attribute disabled)
    This can be controlled by AWS console/AWS cli
    Use case: preserve root volume when instance gets terminated
![tcsglobal udemy com_course_aws-certified-cloud-practitioner-new_learn_lecture_20055762 (1)](https://github.com/user-attachments/assets/55e0281e-40f3-4914-9540-6f85f478a204)
### EBS handson
    Create a EBS storage of 2gb ssd
    Step1) Check the instance region of EC2 instance
        EC2 -> instances -> Networking -> Availibility Zone(AZ)
        In the storage tab check for any EBS attached, also check for Delete on Termination, we can see root will be delete on termination enabled
    Step2) Create a volume
        EC2 -> volumes -> create volume -> select gp2, 2gb, Enter same availibilty zone of ec2 instance -> create volume
    Step3) Attach it on EC2 instance
        Actions -> attach volume -> Select instance -> attach volume
    To disable delete on termination for root
    Step1) while creating EC2 instance, while selecting storage click on advanced tab and disable the delete on termination the root EBS
### EBS snapshot
    Make a backup(snapshot) of your EBS volume at any point in time
    Not necessary to detach volume to do snapshot, but recommended
    can copy snapshot across AZ or region
    EBS snapshot features:
        EBS snapshot archive
            Move a snapshot to an archieve tier which is 75% cheaper
            takes within 24-72 hours for restoring the archive
        Recyle Bin for EBS snapshot
            Setup rules to retain deleted snapshots so you can recover them after an accidental deletion
            Specify retenion (from 1day to 1year)
            
![tcsglobal udemy com_course_aws-certified-cloud-practitioner-new_learn_lecture_20055798](https://github.com/user-attachments/assets/e9748c9c-7c6f-428c-a2a1-dd1933a1a604)
### Hands on EBS Snapshot
    Suppose i have EBS on us-east-1a region i want to change region to us-east-1b region
    Ec2 -> volumes -> select volume, click on actions -> select create snapshot
    Ec2 -> snapshots -> select snapshot, click on actions, select create volume from snapshot -> change the AZ to us-east-1b
    Check volumes we can see the new volume at us-east-1b zone
    Enable Snapshot recycle bin
        EC2 -> snapshots -> click on lauch recycle bin -> retension rule -> create retension rule -> enter name: DemoRentensionRule, resourse type: EBS snapshot, lock setting: Unlock so that we can remove snapshot from the bin
        Try deleting snapshots
        Now we can see the deleted snapshots under recyle bin -> resources and can restore as well
### AMI
    AMI = Amazon Machine Image
    AMI's are customization of EC2 instance
        you can add your own software, configuration, operating system, monitoring
        Faster boot/ configuration time because all you softwares is pre-packaged
    AMI's are built for a specific region(and can be copied across regions)
    You can launch ec2 instance from:
        A public AMI: AWS provided
        Your own AMI: you make and maintain by your self
        An AWS marketplace AMI: an AMI someone else made(and potentially sells)
    AMI Process:
        start an EC2 instance and cutomize it
        Stop the instance(for data integrity)
        Build an AMI - this will also create EBS snapshots
        Lauch instances from other AMIs
#### AMI Handson
    Step1) Create a Sample instance
        Lets create a instance named AMI
        In the user data scripts
        Lets add this code
            #!/bin/bash
            # Use this for your user data (script from top to bottom)
            # install httpd (Linux 2 version)
            yum update -y
            yum install -y httpd
            systemctl start httpd
            systemctl enable httpd
        here we are installing apche server
        and lauch the instance
    Step2) Right click on the instance, click on image and templates, click on create image, add name: DemoImage
    Step3) EC2 -> AMI we can see our DemoImage is there. Now we can create instances from the DemoImage, That means if we want to have a instance with apache server preinstalled we can directly use this image without writing any user data code
    Step4) Create the instance based on the DemoImage
            while creating the new instance under Application and OS Images (Amazon Machine Image), select MyAMI's and select DemoImage
            In the advanced tab under add user data scripts there
            echo "<h1>Hello World from $(hostname -f)</h1>" > /var/www/html/index.html
        now copy paste the public ip in the browser this will work
### EC2 image builder
    Used to automate the creation of Virtual machines or container images
    Automate the creation, maintain, validate and test EC2 AMIs
    Can be run on schedule (weekly, where packages are updated,etc...)
    Free Service(only need to pay for the underlying service)
![tcsglobal udemy com_course_aws-certified-cloud-practitioner-new_learn_lecture_24682456](https://github.com/user-attachments/assets/3847c392-50e2-4b68-bd41-b571b625acba)
### EC2 Instance Store
    EBS volumes are network drives with good but "limited" performance
    if you need a higher performance hardware disk, use EC2 Instance store
    Better I/O performance
    Ec2 instance store lose their storage if they're stopped
    It is not suitable for durable, long term to store your data
    Good for buffer/cache/scratch data/temporary content
    Risk of data loss if hardware fails
    Backups and replications are your responsibility
    
    for long term storage EBS is the best one we can use
    Comparision of EC2 instance and EBS
    IOPS(input output per second)
    look at i3.16xlarge 3.3 million(instance store) 1.4 million (EBS)
![tcsglobal udemy com_course_aws-certified-cloud-practitioner-new_learn_lecture_20055816](https://github.com/user-attachments/assets/3d2f719d-3ebd-4428-a476-b1032517c33d)
### Elastic File System(EFS)
    It is a Managed NFS(Network file system) that can be mounted to 100s of EC2 instances
    The idea and benefit is that it can be mounted to 100s of instances at a time
    Before we had EBS volume that is attached to only one instance at a time, now EFS can be attached to 100s of EC2 at a time
    so that makes shared network file system
    EFS only works with Linux Ec2 instances in multiple AZ
    Highly available, scalable, expensive(3x price of gp2), pay per use, no capacity planning(if you store 20gb data then you have to pay only 20gb price)
    Below is the diagram how they connected
![tcsglobal udemy com_course_aws-certified-cloud-practitioner-new_learn_lecture_20055824](https://github.com/user-attachments/assets/6420a404-361e-4733-9445-cdfb7e2c27ef)
### EBS vs EFS
    rectangle represents instances
![tcsglobal udemy com_course_aws-certified-cloud-practitioner-new_learn_lecture_20055824 (1)](https://github.com/user-attachments/assets/e448323b-5027-4ecc-b176-5b805c2752b7)
### EFS Infrequent Access(ESA-IA)
    Storage that is cost optimized for files not accessed everyday
    upto 92% lower cost compared to EFS
    EFS will automatically move your files to EFS-IA based on the last time they are accessed
    Enable EFS-IA with a life cycle policy
    ExampleL Move files that are not accessed for 60 days to EFS-IA
    Transparent to the applications accessing EFS
![tcsglobal udemy com_course_aws-certified-cloud-practitioner-new_learn_lecture_20055824 (2)](https://github.com/user-attachments/assets/15bb6d1f-9a36-41b0-9da8-0b1f9ff4d5d5)

    

    
    

    

    
        
            
    
    




    
    
        
    
    
    





    
        
    
        
    

    

    
    
    


    
    

    
    
    
    
        
    
        
    
    
    
    
    
        
    
    
    
    

            
        
    

    
    
    

    
    
    
        
        
    
        
        
    
    
