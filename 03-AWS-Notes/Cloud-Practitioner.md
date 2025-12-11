# Cloud Computing essentials
## AWS Global infrastructure 
- AWS Regions: Separate geographic areas
  - have at least 2 Availability zones, each fully isolated and far apart, but offer complete redundancy
- Availability zones (AZ): 1 or more discrete data centers  
  - Availability zones are facilities with their own redundant power, network, and internet connection. More resilient than just having different data centers. 
- AWS Network - AWS Regions and AZs are interconnected over fully redundant parallel fiber networks.
- Point Of Presence(PoP)[edge nodes]: **Amazon Cloudfront**- Global content delivery network
  - Used to securely deliver data to end users
  - Edge locations and regional edge cache servers  
- Partitioning :
  - **AWS Elastic Load Balancing** distributes trafic accross AZs
  - in case any issue with one AZ, it will distribute traffic to a different AZ
## S3 : Storage Service
- Object storage service
- objects = files(pdf,image,etc.) plus metadata(time,date,location,etc.)
- Objects are put into named buckets
- Great for scalability, durability, and security
## EC2 : Virtual servers
- Can be run in multiple availability zones to make it more resilient
- Can attach an EBS( Elastic Block Storage):
  - Acting as a high-performance, persistent hard drive for an EC2 instance. Used for databases, boot volumes, and file systems.
- An EC2 instance can be accessed in 3 different ways (ssh requires key pairs)
## DynamoDB : Database
- Key-value and document databases
- NoSQL(Non relational database)
  - flexible scheme and can be changed easily
  - no need for column/row tables
- prefomaice at a scale
  
