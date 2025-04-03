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
    How to AWS region?
    If you want to lauch a application in which region will you lauch?
        
        
    
        
        
    
    
