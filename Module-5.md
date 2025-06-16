# Amazon S3 Bucket and Route 53

### What is Amazon S3 ?
- Simple Storage Service
#### Core Concepts:
  1. *buckets* - container to store data
  2. *object* - storing format.
  3. globally unique naming of bucket.
  4. Storing Data - any format data can be stored
  5. Durability & Availability - 99.99999999999(11 times)% durable and 99.99% availability
#### Accessing S3:
1. AWS Management Console - service search box
2. AWS CLI Commands - aws s3 ls, aws s3 mv, aws s3 cp

- Programming Scripts / AWS SDKs
- Permissions and Security
- Access Control Lists
- Bucket Policies
- IAM Policies
- Blocking Public Access
- Encryption
- Server-Side encryption (SSE)
- In-Transit Encryption
- Versioning

#### Common use cases
1. Data Storage
2. Backup and Recovery
3. Hosting Static Websites
4. Data Archiving
5. Big Data Analytics
6. Mobile / Web app
7. Software Delivery
8. Disaster recovery
9. IoT devices

/ *Advantage - Cost & Pricing* /

#### Application use
- General Data Storage -> (Storing data concept)
- Backup and Recovery -> (Durability & Availability concept)
- Hosting Static Websites -> low-latency and cost-effectiveness
- Data Archiving -> S3 Glacier Service
- Big Data Analytics / Data Lake -> capacity to store large amount of structured and unstructured data
- Integration with third party workflows -> SDKs
- Automating workflows -> AWS Lambda

#### Static website hosting process
1. Create an S3 bucket
2. Upload Website files
3. Enable static website hosting
4. Initial access attempt (Forbidden)
5. Unblock Public Access
6. Add a bucket policy
7. Website is Publicly Accessible
- Limitations -> does not support HTTPS
- CloudFront -> Amazon's Content Delivery Network (CDN) caches static content at edge locations
- Route 53 -> AWS's DNS service. to map a custom domain name.
- AWS Certificate Manager (ACM) -> generate SSL certificates
#### S3 versioning 
- keep multiple versions of an object in same bucket.
1. Enable versioning
2. Uploading objects
3. Viewing versions
4. Deleting objects with versioning
5. Restoring Previous Versions
6. Permanent Deletion

#### S3 storage classes
1. S3 standard
2. S3 Standard-Infrequent Access (IA)
3. S3 one zone-Infrequent Access (IA)
4. S3 Intelligent-Tiering
5. S3 Glacier Instant Retrieval
6. S3 Glacier Flexible Retrieval
7. S3 Glacier Deep Archive

#### Amazon Route 53
- highly available and scalable cloud domain name system (DNS) web service.
- translate human-readable names into numeric IP addresses.
##### 3 main functions
- Domain Name Registration
- DNS Routing
- Health Checking

##### Setup process
1. Registering a domain name
2. Creating a hosted zone
3. Creating records
4. Hosted Zone - Public or Private

- Common record types
  1. A record
  2. AAAA record
  3. CNAME Record
  4. Alias Record
  5. NS Record (Name Server)
  6. SOA Record (Start of Authority)
  7. MX Record (Mail Exchange)
  8. TXT Record (Text)
  9. PTR Record (Pointer)
  10. SRV Record (Service)
  11. TTL (Time to Live)

- Policy of directing traffic
  - Simple
  - Weighted
  - Latency-based
  - Geo-location
  - Geo-Proximity
  - Health Checking
  - Alias Records
  - Time to Live (TTL)

##### Routing Policies
1. Simple Routing policy
2. Failover Routing policy
3. Geolocation Routing policy
4. Geoproximity Routing policy
5. Latency-based Routing policy
6. IP-based Routing policy
7. Multi-value Answer Routing policy
8. Weighted Routing policy.