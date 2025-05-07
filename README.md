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
### Shared Responsibility model for EC2 storage
    aws - infrastructure, Replication for data for EBS volumes and EFS drives, Replacing faculty hardware, Ensuring their employees cant access your data
    customer- Setting up backup/snapshot procedures, Setting up data encryption, Responsibility of any data you write on drive, Understanding risk of using EC2 instance store.
### Amazon Fsx - overview
    lauch 3rd party high-performance file systems on AWS
    fully managed system
    Amazon FSx for windows file server
        A fully managable, highly reliable, and scalable windows native shared file system
        Built on windows file server
        Supports SMB protocal and windows NTFS
        Integrated with microsoft active directory for security
        Can be accessed from AWS or your on-premise infrastructure
    Amazon FSx for lustre
        A fully managed, high performance, scalable file storage for High performance Computing(HPC)
        The name lusture is derived from linux and cluster
        Machine learning, Analytics, Video processing, Financial Modeling
        Scales upto 100s GB/s, millions of IOPS, sub-ms latencies
![tcsglobal udemy com_course_aws-certified-cloud-practitioner-new_learn_lecture_26623482](https://github.com/user-attachments/assets/882b197b-5472-4d0c-a4c7-02faeadc408c)
![tcsglobal udemy com_course_aws-certified-cloud-practitioner-new_learn_lecture_26623482 (1)](https://github.com/user-attachments/assets/2e17a192-f4b6-4733-be25-2e24cb6f20d9)
### EC2 Instance storage - summary
    EBS volume:
        network drives attached to one EC2 instance at a time
        Mapped to availibility zones
        can use EBS Snapshots for backup/transferring EBS volumes across AZ
    AMI: create read-to-use EC2 instance with customization
    EC2 image builder: automatically build, test and distribute AMI
    EC2 Instance store: 
        High performance hardware disk attached to our EC2 instance
        Lost if our EC2 instance is stopped/terminated
    EFS: network file system, can be attached to 100s Ec2 instances in a region
    EFS-IA: cost optimized storage class for infrequent accessed files
    FSx for windows: Network file system for windows servers
    FSx for Lusture: High performance computing linux file system
### Quiz
    1)Which EC2 Storage would you use to create a shared network file system for your EC2 Instances?
        a)EBS volume
        b)Ec2 instance store
        c)EBS snapshots
        d)EFS
        ans: D
    2)Which service can be used to automate image management processes?
        a)AMI
        b)EC2 Image Builder
        c)EBS snapshots
        D) IAM
        ans: B
    3)Which of the following is a fully managed native Microsoft Windows file system?
        a)EFS
        b)FSx
        c)EBS
        ans: B
        Amazon FSx makes it easy and cost effective to launch and run popular file systems that are fully managed by AWS. It comes in two offerings: FSx for Windows File Server (used for business applications), and FSx for Lustre (used for high-performance computing).
    4)What are AMIs NOT used for?
        a)Add your own software license
        b)Add your own configuration
        c)Add your own operting system
        d)Add your own ip address
        ans: You cannot use AMIs to add your IP addresses. IP addresses are added to an instance as you create it.
    5) EBS Volumes CANNOT be attached to multiple EC2 instances at a time.
        True
    6) An EBS Volume is a network drive you can attach to your instances while they run, so your instances' data persist even after their termination.
        True
        EBS Volumes allows instances' data to persist even after their termination.
    7) Which statement is CORRECT regarding EC2 Instance Store?
        It has better I/O performance, but the data is lost if the EC2 instance is terminated
    8) What is an EBS Snapshot?
        A backup of your EBS volume at a point in time
    9) Where can you find a third party's AMI so you can use it to launch your EC2 Instance?
        a)Public AMIs
        b)My own AMIs
        c)AWS market AMIs
        ans: C
        You can use AWS Marketplace AMIs to use someone else's AMI.
    10) What is an EBS Volume tied to?
        a) A region
        b) An availibility zone
        ans: b
        EBS Volumes are tied to only one availability zone.
## Elastic load balancing and auto scaling Groups section
### Scalability and high availibility
    Scalability means that an application/system can handle greater loads by adapting
    There are two kinds of scalabilities:
        Vertical scalability
        Horizontal scalability (= elasticity)
    Scalability is linked but different to High Availibility
#### Vertical Scalability
    Vertical Scalability means increasing the size of the instance 
    for example your application runs on t2.micro. Scaling that application vertically means running it on t2.large
    Vertical scalability is very common for non distributed systems, such as database
    There's are limit to How much you can vertically scale(hardware)
#### Horizontal Scalability
    Horizontal Scalability means increasing instances for your application
    Horizontal Scaling that implies distributed systems.
    This is common for web applications/modern applications
    Its easy to horizontall scale thanks the cloud offerings such as Amazon EC2
#### High Availbility
    High Availbility usally goes hand-in-hand with horizontal scaling
    High Availbility means running your application in at least 2 availbility zones(AZ)
    The goal of availbility is to survive data center loss(disaster)
#### Summary
    Vertical Scaling: Increase instance size(=scale up/down)
        From t2.nano:0.5Gb of RAM,1vCPU to u-12tbl-metal:12.3TB of RAM, 448 vcpus
    Horizontal Scaling: Increase number of instances(=scale out/in)
        Auto scaling Groups
        load balancers
    High Availbility: Run instances for the same application across different AZ
        Auto scaling Group multi AZ
        Load balancer multi AZ
### Scalability vs Elasticity (vs Agility)
    Scalability: ability to accomodate larger load by making hardware stronger(scale up), by adding nodes(scale out)
    Elasticity: It is related to cloud, Once a system is scalable, elasticity means that there will be auto scaling so that the system can scale based on the load.
    This is cloud friendly, pay-per-use, match demand, optimize costs
    Agility(not related to scalability - distractor): It is related to organization how quick they have getting resources.New IT resources are only a click away,
    which means that you reduce the time to make those availible for developers from weeks to just minutes.
#### what is Load balancering?
    load balancers are servers that forward internet traffic to multiple servers (EC2 instances) downstream.
    Spread load across multiple downstream instance
    Expose a single point of access(DNS) to your application
    Seamlessly handle failures of downstream instances
    Do regular health checks to your instances
    Provide SSL termination(HTTPS) for your websites
    High availibilty across zones
#### Why Elastic Load Balancer?
    An ELB is a managed load balancer
        AWS guarantees that it will be working
        AWS will take care of upgrades, maintanance, high availibility
        AWS provides only a few configuration knobs
    It costs less to setup your own load balancer but it will be a lot more effort on your end
    4 kinds of load balancers offered by AWS:
        Application Load balancer(HTTP/HTTPS only) - also called as Layer 7
        Network Load balancer(ultra high performance, allows for TCP) - Layer 4
        Gateway load balancer - layer 3
        Classic load balanacer(retired in 2023) - layer 4 & 7
![tcsglobal udemy com_course_aws-certified-cloud-practitioner-new_learn_lecture_20055864](https://github.com/user-attachments/assets/29fd739a-1e78-4fe4-9d92-cd010d7a9e01)
#### Hands on Load balancers
    First create 2 instances in the normal way but in the right hand side add 2 in the number of instances
    Check the instances by copying the public ip address in two different tabs
    navigate -> EC2 -> Loadbalancers -> Create Application Load balancer
    Steps:
        Loadbalancer name: ALB
        Choose internet facing
        IPV4
        VPC: default
        Select all Availbility Zones(AZ)
        Security Groups: Create Security Group
                            Securtiy Group name: Allow only http
                            Description: This security group only allows http request to our application
                            Add inbound rule
                                Type: select HTTP beside the source column add ip address as 0.0.0.0/0(It allows every Ip address)
                            Add outbound rule:
                                Type: allow traffic add ip address 0.0.0.0/0
                            Create security group
        Add this Allow only http security group
        In the Listeners and routing section
        In the default action : Create target Group
                                    choose target type: instances
                                    target group name: demo-tg-ALB
                                    Choose IPV4
                                    HTTP1
                                    Select the instance you want
                                    Click as include on pending below
                                    click on create target group
        Add demo-tg-ALB in the default action
        Click on create load balancer
        Created Successfully
        Copy the DNS name and paste it in the browser it will work if not wait for few minutes
        If i keep on refreshing the page the ip address is changing between my 2 instances
        What happens when one of the instance is not working
            Go to instances and stop first instance
            Go to Loadbalancers, click on target groups and click on refresh it shows the first instance Health status is unhealthy
            Refresh the browser now we can see only one ip address that means load balancer will work even if one instance is healthy
#### Whats an Auto Scaling Group (ASG)?
    In reallife the load on your websites and applications change, if we have a shopping application if it is a daytime the application load increases and at night there is no load to the application
    In the cloud we can create and get rid of servers very quickly
    The goal of an Auto Scaling group is to
        Scale out(add EC2 instances) to match increased load
        Scale in(remove Ec2 instances) to match decreased load
        Ensure we have a minimum and maximum numbers of machine running
        Automatically register new instances to load balancer
        Replace unhealty instances
    Cost Savings: Only run at an Optimal capacity(principle of cloud)
    In the ASG we can add we can add minimum size, Desired Capacity, Maximum size, Scale out as needed
    It works hand-in-hand with ALB(Application Load balancer)
![tcsglobal udemy com_course_aws-certified-cloud-practitioner-new_learn_lecture_20055886](https://github.com/user-attachments/assets/76f33251-bd3f-42b5-b881-14820855afbe)
### Handson
    First lets delete the existing instances
    Navigate EC2 -> Autoscaling -> 
    Create Auto Scaling Group
        Name: DemoASG
        lauch template: Create lauch template
            Name: DemoLaunchTemplate
            Just like Create EC2 instance do the same steps
                Click on Quick start
                select : Amazon linux server
                select instance type: t2.micrp
                Select existing security group: lauch-wizard-1
                Add user data scripts:
                    #!/bin/bash
                    # Use this for your user data (script from top to bottom)
                    # install httpd (Linux 2 version)
                    yum update -y
                    yum install -y httpd
                    systemctl start httpd
                    systemctl enable httpd
        Select DemoLauchTemplate click next
        In the next page select all AZs
        In the next page click on Attach to an existing load balancer
            Select demo-tg-alb the previous one
        In the health check enable Elastic load balancing health checks
        In the next page Desired capacity: 2, minimum: 1, max: 4
        Click on next use all default
        Now in the instance if we can check we can see 2 instances were created by autoscaling, since given desired capacity2
        Check the loadbalancers, demoALb, demo-tg-alb these 2 instances we can see there as well
#### Auto scaling groups - Scaling Strategies
    Manual Scaling: update the size of the ASG manually
    Dynamic Scaling: Respond to changing demand
        Simple/step Scaling:
            when a cloud watch alarm is triggered (example cpu > 70%), then add 2 units.(if all instances are running at 70% add 2)
            When a cloud watch alarm is triggered(example cpu < 30%), then remove it.(if all instances are running at 30%)
        Target Tracking scaling:
            Example: I want the average ASG CPU to stay at around 40%. (example i want to all the ec2 instances cpus utilization to be average 40%)
        Scheduled Scaling:
            Anticipate scaling based on known usage patterns
            Example: increase min capacity to 10 at 5pm on fridays
        Predicitive Scaling:
            Uses machine learning to predict future traffic ahead of time
            Automatically provisions right number of instaces in advance
            Useful when your load has predictable time-based patterns
#### ELB & ASG - Summary
    High availibility vs scalability (vertical vs horizontal) vs Elasticity vs Agility in the cloud
    Elastic Load Balancers
        Distribute traffic across backend EC2 instances, can be mulit AZ
        Supports health checks 
        4 kinds of load balances:
            classic(old), Application(HTTP - L7), Network(TCP - L4), Gateway(L3)
        Autoscaling Groups
            Implement Elasticity for your application, across mulitple AZ
            Scale EC2 instances based on the demand on your system, replace unhealthy
            Integrated with ELB
#### Quiz
    1)What is the main purpose of High Availability in the Cloud?
        a) increase scalability
        b) Application triveing even in case of disaster
        c) Access on computer and smartphone
        d) Handle greater loads by launching EC2 instances based on the demand
        ans: B
    2)Which AWS offered Load Balancer should you use to handle hundreds of thousands of connections with low latency?
        a) Application LB
        b) Network LB
        c) Elastic LB
        ans: B, A Network Load Balancer can handle millions of requests per second with low-latency. It operates at Layer 4, and is best-suited for load-balancing TCP, UDP, and TLS traffic with ultra high-performance.
    3) Changing an EC2 Instance Type from a t3a.medium to a t3a.2xlarge is an example of?
        ans: vertical scaling
    4) What can you use to handle quickly and automatically the changing load on your websites and applications by adding compute resources?
        a) An elastic load balancer
        b) A bigger instance type
        c) An auto scaling group
        d) Health checks on your EC2 instance
        ans: D
    5) Which of the following statements is INCORRECT regarding Auto Scaling Groups?
        a) Replace Unhealthy instances
        b) Are cost effictive by running at optimal capacity
        c) Automatically register new instances to a load balancer
        d) Automatically changing the EC2 instance Types
        ans: D, Auto Scaling Groups can add or remove instances, but from the same type. They cannot change the EC2 Instances Types on the fly.
    6) Which Load Balancer is best suited for HTTP/HTTPS load balancing traffic?
        a) Network LB
        b) classic LB
        c) Elastic LB
        d) Applicaiton LB
        ans: D
    7) Which of the following is NOT an Auto Scaling Strategy?
        a) Manual Scaling
        b) Dynamic Scaling
        c) Active Scaling
        d) Predictive Scaling
        ans: C
    8) Which AWS service offers easy horizontal scaling of compute capacity?
        a) EBS
        b) AMI
        c) IAM
        d) ASG
        ans: D
    9) Which of the following statements is NOT a feature of Load Balancers?
        a) Do regular health checks to your instance
        b) Spread across multiple downstream instances
        c) Handle failures of downstream instances
        d) Backend autoscaling
        ans: D
## S3 bucket
    Amazon S3 is the one of the main building blocks of AWS
    It is advertised as "infinitely scaling" storage
    Many websites use S3 as backbone
    Many Aws services use Amazon S3 as an integration as well
### Amazon S3 use cases
    Backup and storage
    Disastery Recovery
    Archieve files in S3 that is much much cheaper
    Hybrid cloud storage
    Application hosting
    Media hosting
    Data lakes and big data analytics
    Software delivery
    static website
    Use case: Nasdaq stores 7 years of data into S3 glacier
              Sysco runs analytics on its data and gain business insights
### Amazon S3 buckets
    Allows people to store objects(files) in S3 bucket(directories)
    Bucket must have a globally unique name(across all regions all accounts)
    Buckets are defined at the region level
    S3 looks like a global service but the buckets are created in region
    Naming convension
        No uppercase, No underscore
        3-63 characters long
        Not an IP
        must start with lower or number
        Must not start with prefix xn-
        must not end with sufix -s3alias
### Amazon S3 objects
    Objects(files) have a Key
    The key is the full path:
        s3://my-bucket/my_file.txt
        s3://my-bucket/my_folder1/another_folder/my_file.txt
    The key is composed of prefix + object name
    There's no concept of directories within buckets
    (although the ui will trick you to think otherwise)
    Just keys with very long names that contain slash("/")
    object values are the content of the body:
        Max. object size is 5TB(5000 GB)
        If uploading more than 5GB,must use multi-part upload
    Metadata(list of key/value pairs - system or user metadata)
    Tags(Unicode key/value pair upto 10) - useful for security/lifecycle
    Version ID(if versioning is enabled)
### Handson
    navigate Amazon S3 -> Buckets -> create Bucket
    Except name keep remaining default
    name: koushik-demo-s3(it should be unique across regions and across all the accounts)
    Create bucket
    Click on the bucket i have created
    upload file -> Add files -> temp.png
    click on temp.png click on open button it will open the file another tab the url contains token
    if i use object url it wont work since it is only accessible by me missing token in the url
### Amazon S3 - security policies
    User Based
        IAM policies - which API calls should be allowed for a specific user from IAM
    Resource Based
        Bucket policies - bucket wide rules from the s3 console - allows cross account
        Object Access Control List(ACL) - finer grain (can be disabled)
        Bucket Access Control List(ACL) - less common (can be disabled)
    Note: An IAM priciple can access an s3 object if
            The IAM permissions allow it or the resource policy allows it
            AND there's no explicit DENY
    Encryption: encrypt objects in Amazon s3 using encryption keys
### S3 bucket policies
    JSON based policies
        {
            "version": "2012-10-17",
            "Statement": [
                {
                    "sid": "PublicRead",
                    "Effect": "Allow",
                    "Principal": "*",
                    "Action": [
                        "s3.GetObject"
                    ],
                    "Resource": [
                        "arn.aws.s3:::examplebucket/*"
                    ]
                }
            ]
        }
    Resource tells on what buckets or objects the policy applies on here the policy is applied on examplebucket/, this applies to every object inside examplebucket
    Effect tells allow or deny actions
    Actions: set of apis to allow or deny
    principal: The account or user to apply the policy to

    Here we are allowing anyone to retrieve object from my examplebucket

    Use S3 bucket for policy to:
        Grant public access to the bucket
        Force objects to be encrypted at upload
        Grant access to another account(cross account)
    Bucket settings for block public access
        Block all public access enabled when creating s3 bucket
    These settings were created to prevent company data leaks
    If you known your bucket should never be public, leave thes on
    can be set at the account level
### Handson
    Make all the objects(files) public in s3 bucket
    Step1) Click on the bucket that i have created underpermissions edit -> turn off block all public access -> save changes
    Step2) Scroll down edit bucket policy click on policy generator
            principal - *(allowing all users and accounts)
            Aws service - select s3 bucket
            actions - GetObject
            ARN(Amazon Resource Name) - copy from bucket ARN and paste there + file path
                                            example: arn:aws:s3:::koushik-demo-s3-v2/*(giving access to all files)
            Generate Policy and paste in the s3 bucket policy
    Step3) Now our file Object url is available across internet
### Amazon S3- static website hosting
    S3 can host static websites and have them available across the internet
    The website URL will be depending on the region
        http://bucket-name.s3-website-aws-region.amazonaws.com
        or
        http://bucket-name.s3-website.aws-region.amazonaws.com
        difference is - and . before aws region
    If you get a 403 forbidden error, make sure the bucket policy allows public reads
### Handson
    navigate -> Amazon s3 -> Buckets -> DemoBucket(i havae created) -> properties scroll down -> static web hosting -> edit -> enable -> index document: index.html -> save changes
    In the objects tab upload index.html file
    To get the hoisted url go to properties tab and copy Bucket website endpoint
### Amazon S3 - versioning
    You can version your files in s3
    It is enabled at the bucket level
    Same key overwrite will change the version: 1,2,3
    It is best practise to version your buckets
        Protect against unintended deletes(ability to restore a version)
        Easy rollback to previous version
    In the ui we can see that it has been overwritten 
    Note:
        any file that is not versioned prior to enabling versioning will have version is null
### Handson
    To simulate this create a new index.html file
    Step1) Enable versioning
            Go to properties -> Bucket versioning -> edit -> enable
    Step2) upload the updated index.html file and reload the hosted url to check weather it is updated or not
    Step3) in the objects enable show versions we can see two files index.html with null version and other with other version
    Step4) To delete a file permanently enable versioning select file and click on delete, write permanently delete this will delete the file
    Step5) if i want to delete the file and want to recover it later
            turn off show versions
            click on logo.png file and delete
            Now turn on show versions we can see the logo.png file there if i want to recover
            select logo.png that is of type delete marker and delete it, write permanently delete
            now refresh the objects now we got the file recovered
### Amazon s3 - Replication(CRR & SRR)
    Must enable versioning betweeen source and destination
    Cross-Region Replication(CRR)
    Same-Region Replication(STRR)
    Buckets can be in different accounts
    Copying is asynchronous
    Must give proper IAM permissions to S3(like read and write)

    Use cases:
        CRR - compliance, low latency access, replication across region
        SRR - log aggregation, live replication between production and test accounts
### Hands on
    lets create two buckets koushik-s3-demo-source, while creating enable bucket versioning and while creating another bucket try changing the region and create it
    Now i have created two buckets source and destination in two different regions what ever the file uploaded to source bucket should be replicated to destination bucket
    Step1) Create replication rule
            click on source bucket -> management -> create replication rule
                                                        name: DemoReplicationRule
                                                        In the source bucket section enable: Apply to all objects in the bucket
                                                        destination: choose this account
                                                        enter bucket name: koushik-s3-demo-destination
                                                        it should automatically detect the location of destination bucket
                                                        IAM role: Create new role
                                                        Click on No, i dont want to replicate existing objects
    For better visulization open two tabs two different buckets
    Step2) Upload a file in the source bucket and check the destination it will work
    Now check the version id in the destination bucket it will be same
### S3 Storage Classes
    Amazon S3 standard - General Purpose
    Amazon s3 standard - Infrequent Access(IA)
    Amazon S3 One zone - Infrequent Access
    Amazon S3 Glacier Instant Retrivel
    Amazon S3 Glacier Flexible Retrivel
    Amazon S3 Glacier Deep Archive
    Amazon S3 Intelligent Tiering

    While creating s3 we can choose the class and we can move between classes manually or using s3 lifecyle configuration
### S3 Durability and Availibility
    Durability
        High durability(99.999999%) of objects across multiple AZ
        if you store 10,000 objects with Amazon S3, you can on average expect to incur a loss of a single object once every 10,000 years
        Same for all storage classes
    Availibility
        Measures how readily available a service is
        Varies depending on storage class
        Example: S3 standard has 99.999999% availibity = not available 53 minutes a year
#### S3 standard - General Purpose
    99.99% Availbility
    Used for frequently accessed data
    Low latency and high throughput
    Sustain 2 concurrent failure failures

    Use cases: Big Data analytics, mobile and gaming applicaitons, content distribution
### S3 standard classes - Infrequent Access
    For data that is less frequently accessed, but requires rapid access when needed
    Lower cost than s3 standard
    Amazon s3 infrequent access(S3 standard IA)
        99.9% Availibility
        Use cases: Disaster Recovery, backups
    Amazon S3 One infrequent access(S3 one Zone-IA)
        High durability in a single AZ; data is lost when AZ is destoyed
        99.5%
    Use cases: Storing secondary backup copies of on-premise data, or data you can recreate
### Amazon S3 glacier storage class
        Low cost object storage meant for archiving/backup
        Pricing: price for storage + object retrievel cost
    Amazon s3 glacier instance retrieval
        Millisecond retrievel, great for data accessed once a quater
        Minimum storage duration is 90 days
    Amazon S3 Glacier Flexible Retrieval(formely Amazon s3 Glacier)
        Expedited(1 to 5 minutes), Standard(3 to 5 hours), Bulk(5 to 12 hours) - free
        Minimum Storage duration is 90 days
    Amazon s3 Glacier Deep archive - for long term storage
        Standard(12 hours), Bulk(48 hours)
        Minimum storage duration is 180 days
### S3 intelligent - Tiering
    Small montly monitoring and auto tiering fee
    Moves objects automatically between access tiers based on usage
    There are no retrieval charges in s3 intelligent-tiering

    frequent access tier(automatic): default tier
    Infrequent Access tier(automatic): objects not accessed for 30 days
    Archeive Instant access tier(automatic): Objects not accessed for 90 days
    Archive Access tier(optional): configurable from 90 days to 700+ days
    Deep Archive Access tier(optional): Config from 180 days to 700 days

![tcsglobal udemy com_course_aws-certified-cloud-practitioner-new_learn_lecture_20055948](https://github.com/user-attachments/assets/f832051a-762f-4493-af87-6a36a01179c3)
![tcsglobal udemy com_course_aws-certified-cloud-practitioner-new_learn_lecture_20055948 (1)](https://github.com/user-attachments/assets/66e9034e-ae98-48b9-9a81-c805d0b10029)
#### S3 Encryption
    In S3 server side encryption happens by default, when ever we upload files, server will encrypt the files automatically.
    It also supports client side encryption encrypt a file and upload the server, the server will again encrypt the file
    Both client and server side encryption is supported by s3
#### IAM Access Analyser for s3
    Ensures that only intended people have access to your bucket
    Example: Publically accessible bucket, bucket shared with other accounts
    Evaluates s3 bucket policies, s3 ACLs, s3 Access Point Policies
### Shared responsibility model for s3
    amazon
        Infrasture(global security, durability, availibility, sustain concurrent loss of data in two facilities)
        Configuration and vulnerability analysis
        compliance validation
    User
        S3 verisioning
        S3 Bucket policies
        S3 Replication setup
        Logging and monitoring
        S3 storage class
        Data encryption
#### AWS snowball
    High secure, portable devices to collect and process data at the edge and migrate into and out of aws
    Helps migrate upto pentabytes of data
    Snowball Edge storage optimized
        compute 104vCPUs, storage 210 TB(SSD), Memory 416GB
    Snowball Edge compute optimized
        compute 104vcpus, storage 28 TB(SSD), Memory 416 GB
    When to use this device
    Challenges:
        Limited connectivity
        Limited bandwidth
        High network cost
        Shared bandwidth
        Connection stability
    AWS snow ball: offline devices to perform data migrations
    if it takes over 1 week to transfer over the network, use snow ball devices
    What is Edge computing?
        Process data while the data is created at edge location
            A truck on the data, a ship on the sea, mining station underground
        These locations may have limited internet, and no access to computing power
        We setup snowball edge device to do edge computing
            Run EC2 instances and lambda function on edge
            do some preprocessing of data and send the results
        Usecases: Preprocess data, machine learning, transcoding media
#### Snowball edge pricing
    You pay for device usage and data out of aws
    Data transfer IN to amazon s3 is 0$ per gb
    On demand
        Includes one time service fee per job, which includes
            10 days of usage of snow ball edge compute optimized device
            15 days of usage of snow ball edge storage device
        shipping days are not counted towards the included 10 or 15 days
        Pay per day for any additional days
    Commited upfront
        Pay in advance for montly, yearly, and 3 years usage(edge computing)
        up to 62% discounted pricing
#### Hybrid cloud for storage
    AWS is pushing for hybrid cloud
        Part of your infrastructrue is on premises
        part of your infrastructure is on cloud
    This is due to
        Long cloud migration
        Security requirement
        compliance requirement
        IT strategy
    S3 is proprietary storage technology(unlike EFS/NFS), so how do you expose the s3 data on-premise?
    AWS storage gateway
#### AWS storage cloud native options
![tcsglobal udemy com_course_aws-certified-cloud-practitioner-new_learn_lecture_20055966](https://github.com/user-attachments/assets/d31da17a-c60f-4c98-aa6e-de08b7e0de66)
#### AWS storage gateway
    Bridge between onpremise data and cloud data in s3
    Allows onpremise to use seamlessly AWS cloud
    Use cases:
        disaster recovery, backup and restore, tiered storage
    Types of storage gateways:
        File Gateway
        Volume gateway
        Tape Gateway
![tcsglobal udemy com_course_aws-certified-cloud-practitioner-new_learn_lecture_20055966 (1)](https://github.com/user-attachments/assets/320b1656-88e5-406a-9ee6-fc913321d1e2)
#### Amazon s3 - Summary
    Buckets vs objects - global unique name, tied to a region and objects reside inside the buckets
    S3 security - IAM policy, S3 Bucket policy (public policy), S3 encryption
    S3 Websites - host a static website on s3
    S3 versioning - Multiple versions for files, prevent accidential deletes
    S3 Replication - same region or cross region, must enable versioning
    S3 storage classes - Standard, IA, IZ-IA, Intelligent, Glacier(Instant, flexible, deep)
    snow family - import data onto s3 through a physical device, edge computing
    Ops hub - Desktop application to manage snow devices
    Storage gateway - hybrid solution to extend on premise storage to s3
### Quiz
    1.Which S3 Storage Class is the most cost-effective for archiving data with no retrieval time requirement?
        a) Amazon Glacier
        b) Amazon Glacier Deep Archive
        c) Amazon s3 inadequent Access
        d) Amazon s3 intelligent tiering
        ans: B
        Amazon Glacier Deep Archive is the most cost-effective option if you want to archive data and do not have a retrieval time requirement. You can retrieve data in 12 or 48 hours.
    2.What hybrid AWS service is used to allow on-premises servers to seamlessly use the AWS Cloud at the storage layer?
        ans: storage gateway
        AWS Storage Gateway is a hybrid cloud storage service that gives you on-premises access to virtually unlimited cloud storage
    3.What are Objects NOT composed of?
        a) key
        b) value
        c) Access keys
        d) meta data
        ans c)
        Access Keys are used to sign programmatic requests to the AWS CLI or AWS API.
    4.Where are objects stored in Amazon S3?
        a)folders
        b)buckets
        c)files
        d)bin
        ans: B
    5. What can you use to define actions to move S3 objects between different storage classes?
        a) scaling policy
        b) bucket policy
        c) Lifcycle rules
        d) Replication
        B) Incorrect
        Bucket policies are JSON documents for granting permission to your Amazon S3 resources. It is not used to define actions to move S3 objects between different storage classes.
        A) Incorrect
        A Scaling Policy is used to define how to scale the capacity of your Auto Scaling group in response to changing demand. It is not used to define actions to move S3 objects between different storage classes. S3 scales automatically and is advertised as an “infinite” storage
        C) Correct
        Lifecycle Rules can be used to define when S3 objects should be transitioned to another storage class or when objects should be deleted after some time.
    6. A non-profit organization needs to regularly transfer petabytes of data to the cloud and to have access to local computing capacity. Which service can help with this task?
        a) Snowball edge - storage optimized
        b) Snowabll edge - compute optimized
        c) snowcone
        d) snowmobile
        ans: B incorrect - Snowball Edge Compute Optimized provides powerful computing resources for higher performance workloads such as machine learning, full motion video analysis, analytics, and local computing stacks. Despite providing local computing capacity, AWS Snowball Edge Compute Optimized devices are not best-suited for data transfer, but instead the high performance workloads mentioned above.
        ans: A correct
    7. Which S3 Storage Class is suitable for less frequently accessed data, but with rapid access when needed, while keeping a high durability and allowing an Availability Zone failure?
        a) Amazon s3 standard - General Purpose
        b) Amazon glacier
        c) Amazon s3 one-zone infrequent Access
        d) Amazon s3 standard-infrequent access
        ans: D
## Databases Intro
    Storing data on disk(EBS, EFS, EC2 store instance, S3) have its limit
    You can structure the data
    You build indexes to efficiently query/search through data
    You define relationships between datasets
    NoSQL - non relational databases
        Benefits:
            Flexibility: easy to evolve data model
            Scalability: Designed to scaleout by using distributed clusters
            High performance: Optimized for specific data models
            Highly functional: types optimized for data models
### Databases and shared Responsibility model on AWS
    AWS offers us to manage different databases
    Benefit include:
        Quick Provision, High availiability, Vertical and horizontal scaling
        Automated backup and Restore, Operations, Upgrade
        Operating system patches were handled by AWS
        Monitoring, alerting
    Note:
        many database technologies can be run on EC2 instance, but you must handle yourself the resiliency, backup, patching, high availibility, fault tolerance, scaling
### Amazon RDS Overview
    RDS stands for Relational Database Service
    It allows you to create databases in the cloud that are managed by AWS
        Postgres
        Mysql
        MariaDB
        Oracle
        Microsoft SQL server
        IBM DB2
        Aurora(AWS propritory database)
    Advantage over using RDS vs deploying db on EC2
        RDS is managed service
            Automated provisons, OS patching
            Continous Backups and restore to specific timestamp(Point in time restore)
            Monitoring dashboards
            Read replicas for imporved read performance
            Multi AZ setup for DR(Disaster Recovery)
            Maintainance windows for upgrades
            Scaling capability(verically and horizontally)
            Storage backed by EBS
        But you can't SSH into your instances
![tcsglobal udemy com_course_aws-certified-cloud-practitioner-new_learn_lecture_20055978](https://github.com/user-attachments/assets/1e08a198-0822-4bff-b620-d5286725794d)
### Amazon Aurora
    Aurora is proprietary technology of AWS(not open sourced)
    Postgres and Mysql are both supported as Aurora DB
    Aurora is AWS optimized and claims 5X performance improvement over MYSQL and 3X performance improvement than postgres on RDS
    Aurora storage automatically grows in increments of 10GB, upto 128TB
    Aurora costs more than RDS (20% more)- but it is more efficient
    Not in the free tier
    There is an option of serverless in aurora
    Automated database instantiation and auto-scaling based on actual usage
    Postgres and MYsql are both supported as Aurora Severless DB
    No capacity planning needed
    Least management overhead
    Pay per second, can be more cost effective
    Use cases: good for infrequent, intermittent or unpredictiable workloads
![tcsglobal udemy com_course_aws-certified-cloud-practitioner-new_learn_lecture_20055978 (1)](https://github.com/user-attachments/assets/8a397de7-c169-4b84-be3a-50638d709da5)

### RDS handson
    Naviage Aurora and RDS -> databases -> create database -> Choose standard database creation, 
                                                              Change engine type to postgres db, 
                                                              choose latest engine version, 
                                                              Template free tier, 
                                                              Avaliability zone - single AZ
                                                              Enter master password
                                                              Instance configuration
                                                              Compute resource - Dont connect to EC2 instance compute resource
                                                              Public access - public 
                                                              VPC security group(firewall)
                                                              Vpc group name - rds_firewall(some random name)
                                                              Select AZ
                                                              Click on create Db
                                                              In the additional configuration we can find the port number

![image](https://github.com/user-attachments/assets/e09c6fde-32cd-44d4-8af0-188a073f8296)

![tcsglobal udemy com_course_aws-certified-cloud-practitioner-new_learn_lecture_24682526 (1)](https://github.com/user-attachments/assets/539b2806-bbea-4706-b55f-22490c174693)


![tcsglobal udemy com_course_aws-certified-cloud-practitioner-new_learn_lecture_24682526 (2)](https://github.com/user-attachments/assets/5e7a1401-305a-4c4c-9c30-e0ed2ad9fc06)

### Amazon Elastic cache Overview
    The same way RDS is to get managed relational databases
    ElasticCache is to get managed Redis or memcached
    Caches are in-memory databases with high performance, low latency
    Helps reduce load off databases for read intensive workloads
    AWS takes care of OS maintanance/patching, optimizations, setup configuration, monitoring, failure recovery and backups

![tcsglobal udemy com_course_aws-certified-cloud-practitioner-new_learn_lecture_20055990](https://github.com/user-attachments/assets/2a9f58bc-2875-4fe7-b04e-0a56467b7082)
### Dynamo DB
    Fully managed highly available with replication across 3 AZ
    NoSQL database - not a relational database
    Scales to massive workloads, distributed serverless database
    Millions of requests per seconds, trillions of row, 100TB of storage
    Fast and consistant in performance
    Single digit millisecond latency - low latency retrival
    Integrated with IAM for security, authorization and administration
    Low cost and autoscaling capabilites
    Standard and Infrequent Access Table class
![tcsglobal udemy com_course_aws-certified-cloud-practitioner-new_learn_lecture_20055996](https://github.com/user-attachments/assets/0fa89903-f94f-40e8-bc66-e3aef0b40c14)
### DynamoDB Accelerator - DAX
    Fully managed in-memory cache for dynamo db
    10x performance improvement - single digit millisecond to microsecond latency - when accessing you dynamodb tables
    Secure, highly scalable and highly available
    Difference between ElasticCache at CCP level: DAX is only used for and integrated Dynamodb, while ElasticCache is used for other databases
### Hands on DB
    Create table
        Navigate -> Dynamo db
        Tablename - Demo Table
        Partition key - user_id
        Default settings
        create table
    Add values to table
        Go inside the table that i have created
        Click on explore table items
        Scroll down and click on create item
        click on Add new attribute that adds colums and values
### Dynamo Db Global table
    Make Dynamo db accessible with low latency in multiple regions
    Active-Active replication (read/write to any AWS region)
![tcsglobal udemy com_course_aws-certified-cloud-practitioner-new_learn_lecture_29102352](https://github.com/user-attachments/assets/f440b6d8-c678-4b54-9922-e699735b1c07)
### Redshift overview
    Redshift is based on PostgresSQL, but it is not for OLTP
    OLTP - Online Analytics Processing(analytics and data warehousing)
    Load data once every hour, not one second
    10x better performance than other data warehouses, scale to PBs of data
    Columnar storage of data inside of row based
    Massively parallel Query Exectution(MPP), highly available
    Pay as you go based on the instances provisioned
    Has a SQL interface for performing the queries
    BI tools such as AWS Quicksight or tableau intergrated with it
#### Redshift serverless
    Automatically provisions and scale data warehouse underlying capacity
    Run analytics workloads without managing data warehouse infrastructure
    Pay only for what you use
    Use cases: Reporting, dashboarding applications, realtime-analytics
![tcsglobal udemy com_course_aws-certified-cloud-practitioner-new_learn_lecture_20056000](https://github.com/user-attachments/assets/1663096c-9654-4eae-82a2-c6afbde54d90)
#### Amazon EMR
    EMR stands for Elastic MapReduce
    EMR helps to create Hadoop clusters(Big Data) to analyze and process vast amount of data
    The cluster can be made of hunderds of EC2 instances
    Also supports Apache Spark, HBase, Presto, Flink
    EMR takes care of all provisioning and configuration
    Auto scaling and integrated with spot instances
    Use cases: data processing, machine learning, web indexing, big data
#### Amazon Athena
    Serverless query service to perform analytics on s3 objects
    Uses standard sql language to query the files
    Supports CSV, JSON, ORC
    Pricing: 5$ per TB data scanned
    Use compressed or column data for cost savings(less scan)
    Use cases: Business Intelligence, analytics, reporting, analyze and query VPC Flow logs, ELB logs
    Exam Tip: analyze data in s3 using serverless SQL, use Athena
#### Amazon Quicksight
    Serverless machine learning-powered business intelligent service to create interactive dashboards
    Fast, automatically scalable, embeddable, with per-session pricing
    Use cases:
        Business Analytics
        Building visualization
        perform ad-hoc analysis
        Get business insights using data
    Integrated with RDS, Aurora, Athena, Redshift, s3,...
#### DocumentDB
    Aurora is the AWS implementation of postgres/mysql
    DocumentDb is the same for mongodb
    Mongodb is used to store, query and index json data
    Similar deployment concepts of aurora
    Fully managed, highly avaliable with replication across 3 AZ
    DocumentDb storage automatically grows in increments of 10GB
    Automatically scales to workloads with millions of requests per second
#### Neptune
![tcsglobal udemy com_course_aws-certified-cloud-practitioner-new_learn_lecture_24682534](https://github.com/user-attachments/assets/bf4062fc-13f2-441f-9324-f33352378414)
#### Amazon Timestream
    Fully managed, scalable, serverless time series database
    Automatically scales up/down to adjust capacity
    Store and analyse trillions of events per day
    1000s time faster and 1/10th cost of relational database
    Built in timeseries analytics functions(helps you identify patterns in your in near realtime)
#### QLDB
![tcsglobal udemy com_course_aws-certified-cloud-practitioner-new_learn_lecture_24682538](https://github.com/user-attachments/assets/bb7ddab4-1a32-4128-ab45-ec5457c8e75d)
#### Amazon Managed Blockchain
![tcsglobal udemy com_course_aws-certified-cloud-practitioner-new_learn_lecture_24682538](https://github.com/user-attachments/assets/caad36d5-4416-4fc7-8ab3-8e94749a0ad4)
#### Amazon Glue
    Used for ETL(Extract Transform and load)
![tcsglobal udemy com_course_aws-certified-cloud-practitioner-new_learn_lecture_20514614](https://github.com/user-attachments/assets/45c425a0-8009-4138-9ea5-05422e468437)
#### DMS - Data Migration Service
![tcsglobal udemy com_course_aws-certified-cloud-practitioner-new_learn_lecture_20514614](https://github.com/user-attachments/assets/997b4118-59c6-4d1a-8013-bdeb6ddfe7d5)
### Database and Analytics Summary in AWS
    Relational Databases - OLTP: RDS and Aurora(SQL)
    Difference between Multi-AZ, Read Replicas, Multi-Region
    In-memory Cache Database: Elastic Cache
    Key/value Database: DynamoDb(serverless) & DAX(cache for dynamo db)
    warehouse - OLAP: Redshift(SQL)
    Hadoop cluster - EMR
    Athena - query data on s3(serverless and sql)
    Quicksight - dashboards on your data(serverless)
    DocumentDB - Aurora for MongoDB
    Amazon QLDB - financial Transcations ledger(immutable, journal, cryptography verifiable)
    Amazon Managed Blockchain - managed hyperledge fabric and Ethereum blockchains
    Glue - Managed ETL and data catalog service
    Database Migration - DMS
    Neptune - Graph Database
    Timestream - Timeseries database
    
    
    




        
        
    
    
    

        
    
    
    
    
                                            
                            
        
    
    
    

            
        
                
                
            
            
                                            
                                    
    


    
    

    

    
    

    

    
        
            
    
    




    
    
        
    
    
    





    
        
    
        
    

    

    
    
    


    
    

    
    
    
    
        
    
        
    
    
    
    
    
        
    
    
    
    

            
        
    

    
    
    

    
    
    
        
        
    
        
        
    
    
