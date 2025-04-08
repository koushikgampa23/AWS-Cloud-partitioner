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
    
        
    

    
    
    

    
    
    
        
        
    
        
        
    
    
