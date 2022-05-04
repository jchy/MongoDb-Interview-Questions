# MongoDb-And-Backend-Interview-Questions

There are two types of data as we know – (i) structured data and (ii) unstructured data. 
Structured data is usually stored in a tabular form whereas unstructured data is not. 
To manage huge sets of unstructured data like log or IoT data, a NoSQL database is used.

What is MongoDB?
MongoDB is an open-source NoSQL database written in C++ language. It uses JSON-like documents with optional schemas. 
It provides easy scalability and is a cross-platform, document-oriented database.
MongoDB works on the concept of Collection and Document.
It combines the ability to scale out with features such as secondary indexes, range queries, sorting, aggregations, and geospatial indexes.
1. What are some of the advantages of MongoDB?
Some advantages of MongoDB are as follows:
MongoDB supports field, range-based, string pattern matching type queries. for searching the data in the database 
MongoDB support primary and secondary index on any fields
MongoDB basically uses JavaScript objects in place of procedures
MongoDB uses a dynamic database schema
MongoDB is very easy to scale up or down
MongoDB has inbuilt support for data partitioning (Sharding).
2. What is a Document in MongoDB?
A Document in MongoDB is an ordered set of keys with associated values. It is represented by a map, hash, or dictionary. In JavaScript, documents are represented as objects:
{"greeting" : "Hello world!"}
Complex documents will contain multiple key/value pairs:
{"greeting" : "Hello world!", "views" : 3}
5. What is the Mongo Shell?
It is a JavaScript shell that allows interaction with a MongoDB instance from the command line. With that one can perform administrative functions, inspecting an instance, or exploring MongoDB. 
The mongos acts as a query router, providing an interface between client applications and the sharded cluster.
Q. What are SQL Databases? What are some companies who use Mongo, what type of applications are these?
Ans. https://medium.com/@rsk.saikrishna/when-to-use-mongodb-rather-than-mysql-d03ceff2e922

Q. What is the difference between SQL and NoSQL databases?
Ans. SQL is used for managing data that has many schemas and relations. NoSQL is a non-relational database that does not require a fixed schema and is easy to scale. These databases are sometimes also referred to as “Not Only SQL” databases. With NoSQL, data can be stored in a schema-less, any data can be stored in any record.

https://medium.com/dot-intern/nosql-vs-sql-which-is-better-1abe3a6db268#:~:text=SQL%20is%20used%20for%20manage%20data%20that%20has%20many%20schemas%20and%20relations.&text=NoSQL%20is%20a%20non%2Drelational,be%20stored%20in%20any%20record
https://www.mongodb.com/nosql-explained/nosql-vs-sql

Q. What are some features of MongoDB?
Ans. https://www.upgrad.com/blog/mongodb-real-world-use-cases/

Q. What are aggregate queries in mongodb?
Ans. https://www.mongodb.com/what-is-mongodb/features 

Q. What are aggregate queries in mongodb?
Ans. Aggregation groups documents in a collection and is used to provide results like the total number of documents, sum, average, maximum and minimum values. To the people who are acquainted with SQL the aggregation stages of MongoDB are analogous to COUNT(), SUM(), GROUP BY, LIMIT etc of SQL's

https://medium.com/@ashiqgiga07/aggregation-in-mongodb-209515e5b0ba#:~:text=Aggregation%20groups%20documents%20in%20a,BY%2C%20LIMIT%20etc%20of%20SQL's

Q. What are pipelines in aggregation?
Ans. https://medium.com/mongodb-performance-tuning/explaining-aggregation-pipelines-2d1edd46a341

An aggregation pipeline consists of one or more stages that process documents: Each stage performs an operation on the input documents. For example, a stage can filter documents, group documents, and calculate values. The documents that are output from a stage are passed to the next stage.

Q. How do you do aggregate queries?
Ans. https://www.idera.com/glossary/aggregate-query 

Q. How can you group by a particular value in MongoDB?
Ans. https://www.mongodb.com/docs/manual/reference/operator/aggregation/group/ 

Q. How can you paginate on MongoDB?
Ans. https://www.educba.com/mongodb-pagination/ 


Q. How can you sort in MongoDB?
Ans. https://www.tutorialspoint.com/mongodb/mongodb_sort_record.htm#:~:text=To%20sort%20documents%20in%20MongoDB,is%20used%20for%20descending%20order 


Q. What is indexing in MongoDB? Why do we need to use indexing? What are pros and cons for indexing?
Ans. https://medium.com/@irfan.ali_65238/indexes-in-mongodb-df227ca95ce0

Q. Write the query for indexing a field in MongoDB?
Ans. https://www.mongodb.com/docs/manual/reference/method/db.collection.createIndex/ 

Q. What is the improvement in performance in MongoDB?
Ans. Other ways to improve MongoDB performance after identifying your major query patterns include: Storing the results of frequent sub-queries on documents to reduce read load. Making sure that you have indices on any fields you regularly query against. Looking at your logs to identify slow queries, then check your indices.

https://www.mongodb.com/basics/best-practices#:~:text=Other%20ways%20to%20improve%20MongoDB,queries%2C%20then%20check%20your%20indices

Q. What is the data structure used for indexing?
Ans. The db. collection. createIndex() method only creates an index if an index of the same specification does not already exist. MongoDB indexes use a B-tree data structure.

Q. Are values sorted in indexes? Are indexes sorted?
Ans. Indexing is a way of sorting a number of records on multiple fields. Creating an index on a field in a table creates another data structure which holds the field value, and a pointer to the record it relates to. This index structure is then sorted, allowing Binary Searches to be performed on it.


Q. What are Replica Sets in MongoDB?
Ans. A replica set in MongoDB is a group of mongod processes that maintain the same data set. Replica sets provide redundancy and high availability, and are the basis for all production deployments. This section introduces replication in MongoDB as well as the components and architecture of replica sets.

https://medium.com/swlh/mongodb-creating-a-3-node-replica-set-cluster-7ca94849b139#:~:text=By%20the%20end%20of%20this,maintain%20the%20same%20data%20set

Q. Explain the structure of ObjectID in MongoDB.

Ans. An ObjectId in MongoDB is a 12-byte BSON type. In the 12-byte structure, the first 4 bytes of the ObjectId represent the time in seconds since the UNIX epoch. The next 3 bytes of the ObjectId represent the machine identifier. The next 2 bytes of the ObjectId represent the process ID.

Q. By default, which index is created by MongoDB for every collection?
Ans. MongoDB creates a unique index on the _id field during the creation of a collection. The _id index prevents clients from inserting two documents with the same value for the _id field.
Q. In which format MongoDB represents document structure?
Ans. In MongoDB, data is stored as documents. These documents are stored in MongoDB in JSON (JavaScript Object Notation) format.

Q. What is the limitation of a document in MongoDB?

Ans. The maximum BSON document size is 16 megabytes. The maximum document size helps ensure that a single document cannot use excessive amount of RAM or, during transmission, excessive amounts of bandwidth. To store documents larger than the maximum size, MongoDB provides the GridFS API.

https://www.mongodb.com/docs/manual/reference/limits/#:~:text=The%20maximum%20BSON%20document%20size,MongoDB%20provides%20the%20GridFS%20API

Q. What is the difference between MongoDB and Redis database?

Ans. MongoDB is a document-oriented, disk-based database optimised for operational simplicity, schema-free design and very large data volumes. Redis is an in-memory, persistent data structure store that enables developers to perform common operations with minimal complexity and maximum performance.
https://www.geeksforgeeks.org/difference-between-redis-and-mongodb/#:~:text=Redis%20offers%20memory%20efficiency%2C%20fast,(i.e.%20NoSQL)%20database%20program 

Q. How can you add references between multiple collections?
Ans. https://www.mongodb.com/docs/manual/reference/database-references/ 

Q. What are lookups in aggregation for MongoDB?
Ans. https://medium.com/cameoeng/mongodb-lookups-and-populates-an-unexpected-journey-940e08e36a94 

Q. What are graph lookups?
Ans. Definition. $graphLookup. Performs a recursive search on a collection, with options for restricting the search by recursion depth and query filter.

Q. What is the alternative for lookups in MongoDB?
Ans. https://www.mongodb.com/community/forums/t/how-to-properly-utilize-lookup-with-alternate-join-conditions/14701


Q. How can you do one to many relation in MongoDB?
Ans. what is load balancing?
A load balancer is a device that acts as a reverse proxy and distributes network or application traffic across a number of servers. It helps scale horizontally across an ever-increasing number of servers.


CAP Theorem:~
The CAP theorem states that it is not possible to guarantee all three of the desirable properties – consistency, availability, and partition tolerance at the same time in a distributed system with data replication. 

The theorem states that networked shared-data systems can only strongly support two of the following three properties: consistency, availability and partial tolerance.


PACELC theorem:~

The PACELC theorem is an extension to the CAP theorem. It states that in case of network partitioning (P) in a distributed computer system, one has to choose between availability (A) and consistency (C) (as per the CAP theorem), but else (E), even when the system is running normally in the absence of partitions, one has to choose between latency (L) and consistency (C).

Q. What is meant by eventual consistency?
Ans. Eventual Consistency is a guarantee that when an update is made in a distributed database, that update will eventually be reflected in all nodes that store the data, resulting in the same response every time the data is queried

Q. What do you mean by strong consistency?
Ans. Strong Consistency simply means the data must be strongly consistent at all times. All the server nodes across the world should contain the same value as an entity at any point in time. And the only way to implement this behavior is by locking down the nodes when being updated. 
Q. What are the different types of databases?
Ans. https://www.matillion.com/resources/blog/the-types-of-databases-with-examples 

Q. What are message queues used for?
Ans. Message queues allow different parts of a system to communicate and process operations asynchronously. A message queue provides a lightweight buffer which temporarily stores messages, and endpoints that allow software components to connect to the queue in order to send and receive messages.

Q. What is the purpose of a reverse proxy?
Ans. A reverse proxy ultimately forwards user/web browser requests to web servers. However, the reverse proxy server protects the web server's identity. This type of proxy server also moves requests strategically on behalf of web servers, typically to help increase performance, security, and reliability.

Q. What is TLS and how does it work?
Ans. Transport Layer Security (TLS) encrypts data sent over the Internet to ensure that eavesdroppers and hackers are unable to see what you transmit which is particularly useful for private and sensitive information such as passwords, credit card numbers, and personal correspondence.

Q. What is Docker? Why do we use it?
Ans. Docker is an open source containerization platform. It enables developers to package applications into containers—standardised executable components combining application source code with the operating system (OS) libraries and dependencies required to run that code in any environment.

Q. What are webhooks used for?
Ans. A webhook is a lightweight API that powers one-way data sharing triggered by events. Together, they enable applications to share data and functionality, and turn the web into something greater than the sum of its parts. APIs and webhooks both allow different software systems to sync up and share information.

Q. Which service by Amazon Web Services (AWS) can you use for Queues?

Ans. Amazon Simple Queue Service (SQS)

Amazon Simple Queue Service (SQS) is a fully managed message queuing service that enables you to decouple and scale microservices, distributed systems, and serverless applications.

Q. What does Pub Sub mean?
Ans. Publish/subscribe messaging
Publish/subscribe messaging, or pub/sub messaging, is a form of asynchronous service-to-service communication used in serverless and microservices architectures. In a pub/sub model, any message published to a topic is immediately received by all of the subscribers to the topic.

Q.What is S3 Service in AWS? What is the AWS S3 service used for?
Ans. Amazon Simple Storage Service (Amazon S3) is an object storage service that offers industry-leading scalability, data availability, security, and performance. You can use Amazon S3 to store and retrieve any amount of data at any time, from anywhere.

Q. What is EC2 Instance in AWS?

Ans. An Amazon EC2 instance is a virtual server in Amazon's Elastic Compute Cloud (EC2) for running applications on the Amazon Web Services (AWS) infrastructure.

Q. What is Cloudfront in AWS?

Ans. Amazon CloudFront is a web service that speeds up distribution of your static and dynamic web content, such as . html, . css, . js, and image files, to your users. CloudFront delivers your content through a worldwide network of data centres called edge locations.


Q. What is Route 53 In AWS?

Ans. Amazon Route 53 is a highly available and scalable cloud Domain Name System (DNS) web service. It is designed to give developers and businesses an extremely reliable and cost effective way to route end users to Internet applications by translating names like www.example.com into the numeric IP addresses like 192.0.

Q. What are ELBs in AWS?

Ans. Elastic Load Balancing (ELB) automatically distributes incoming application traffic across multiple targets and virtual appliances in one or more Availability Zones (AZs).



How to Store Huge Media Files in Mongo Database
We can use mongodb gridFS to achieve this. Generally mongodb has a limitation of 16MB size of documents but with the help of Gridfs we can store video/ audio/ pdf/ images of sizes larger than the 16 MB. we will be able to store the files having sizes in Gigabytes. 




Steps to upload a file named  “ABC” in MongoDB using gridFS of mongoDB :
if you are in the current directory where the file named :”myvideo.mp4” to be uploaded is present then run the following command in your default terminal(not one provided by mongod, mongosh)
The following code will upload the file to a database name myfirstdb
mongofiles -d myfirstdb put "myvideo.mp4" 

If you are not in the same directory where file to be sent is located then instead of file name you have to put the path of the file along with the fileName.
mongofiles -d myfirstdb put "/Users/jaswantchaudhary/Desktop
/myvideo.mp4" 

The above command will create a database named myfirstdb and put the given file there in the fs.files ( it will store metadata of the file) and fs.chunks (it will store you file in form of chunks each of size 256KB, numbered 0 1 2 3…..(size_of_file_in_KB/256)-1);

Use the following command in monosh to view the metadata of the uploaded file.
db.fs.files.find().pretty()
OutPut will be 
[
  {
    _id: ObjectId("62663c4a27e1afffc51109b8"),
    length: Long("21022879"),
    chunkSize: 261120,
    uploadDate: ISODate("2022-04-25T06:14:34.871Z"),
    filename: 'myvideo.mp4',
    metadata: {}
  }
]

To view all the chunks we can use following command: 
db.fs.chunks.find()
To get the chuks info without data and _id use the following projection query:
db.fs.chunks.find({},{data:0, _id:0}).pretty();
To get your data back from the database use the following query:
mongofiles -d myfirstdb get "myvideo.mp4" 

NOTE : To view the files of a particular extension in the current directory use the following commands : 
ls -ltrh *.mp4

We can insert many documents in a collection using for loop and insertMany both
for(let i=0;i<50;i++){
...  db.Student.insert({name:`A${i}`,age:i})
... }

We can assign the result of a query to a variable and then can get all the result using variable like
val = db.Student.find()
We can get the single values also by typing 
val.next();

db.students.update({"name":"Amit"},{$set:{"age":25}},{ upsert: true});


To select any database we use CAP theorem to select them:
Consistency : All user the clients have same view of the data
Availability : All the clients can read and write to the database .
Partition Tolerance : Even though there is a partition in the network, clients can access the database.


RDBMS
MongoDB
Database
Database
Table
Collection
Row/ Tuple
Documents
Column
Filed
Table Join
Embedded Documents
Primary Key
Primary Key


JSON full form : JavaScript Object Notation
Maximum we can put 100 embedded documents in a JSON document.


