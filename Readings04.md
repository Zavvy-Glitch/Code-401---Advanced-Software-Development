# Data Modeling

## NoSQL vs SQL 
*Information provided by: [theGeekStuff](https://www.thegeekstuff.com/2014/01/sql-vs-nosql-db/?utm_source=tuicool)*

### Differences:
   - SQL databases are primarily called as Relational Databases (RDBMS); whereas NoSQL database are primarily called as non-relational or distributed database
   - NoSQL databases are the collection of key-value pair, documents, graph databases or wide-column stores which do not have standard schema definitions which it needs to adhered to.
   - SQL databases uses structured query language for defining and manipulating the data, which is very powerful. In NoSQL database, queries are focused on collection of documents.
   - For scalability: In most typical situations, SQL databases are vertically scalable. You can manage increasing load by increasing the CPU, RAM, SSD, etc, on a single server. On the other hand, NoSQL databases are horizontally scalable. You can just add few more servers easily in your NoSQL database infrastructure to handle the large traffic.

### SQL Databases
   - MySQL
        - Replication: By replicating MySQL database across multiple nodes the work load can be reduced heavily increasing the scalability and availability of business application
        - Sharding: MySQL sharding os useful when there is large no of write operations in a high traffic website. By sharding MySQL servers, the application is partitioned into multiple servers dividing the database into small chunks. As low cost servers can be deployed for this purpose, this is cost effective.
        - Memcached as a NoSQL API to MySQL: Memcached can be used to increase the performance of the data retrieval operations giving an advantage of NoSQL api to MySQL server.
   - MS-SQL
        - Integrated Development Environment: Microsoft visual studio, Sql Server Management Studio and Visual Developer tools provide a very helpful way for development and increase the developers productivity.
        - Disaster Recovery: It has good disaster recovery mechanism including database mirroring, fail over clustering and RAID partitioning.
        - Cloud back-up: Microsoft also provides cloud storage when you perform a cloud-backup of your database
   - Oracle Express
        - Easy to Upgrade: Can be easily upgraded to newer version, or to an enterprise edition.
        - Wide platform support: It supports a wide range of platforms including Linux and Windows
        - Scalability: Although the scalability of this database is not cost effective as MySQL server, but the solution is very reliable, secure, easily manageable and productive
### NoSQL Databases
   - MongoDB
        -  Speed: For simple queries, it gives good performance, as all the related data are in single document which eliminates the join operations.
        - Scalability: It is horizontally scalable i.e. you can reduce the workload by increasing the number of servers in your resource pool instead of relying on a stand alone resource.
        - Manageable: It is easy to use for both developers and administrators. This also gives the ability to shard database
        - Dynamic Schema: Its gives you the flexibility to evolve your data schema without modifying the existing data   
   - CouchDB
        - Schema-less: As a member of NoSQL family, it also have dynamic schema which makes it more flexible, having a form of JSON documents for storing data.
        - HTTP query: You can access your database documents using your web browser.
        - Conflict Resolution: It has automatic conflict detection which is useful while in a distributed database.
        - Easy Replication: Implementing replication is fairly straight forward 
   - Redis
        - Data structures: Redis provides efficient data structures to an extend that it is sometimes called as data structure server. The keys stored in database can be hashes, lists, strings, sorted or unsorted sets.
        - Redis as Cache: You can use Redis as a cache by implementing keys with limited time to live to improve the performance.
        - Very fast: It is consider as one of the fastest NoSQL server as it works with the in-memory dataset. 
