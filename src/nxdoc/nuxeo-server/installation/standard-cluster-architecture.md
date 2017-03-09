---
title: Standard Nuxeo Cluster Architecture
description: This page details standard architecture options to deploy a Nuxeo cluster.
review:
    comment: ''
    date: '2017-02-22'
    status: ok
labels:
    - lts2016-ok
    - deployment
    - clustering
    - architecture
toc: true
confluence:
    ajs-parent-page-id: '3866685'
    ajs-parent-page-title: Installation
    ajs-space-key: NXDOC
    ajs-space-name: Nuxeo Platform Developer Documentation
    canonical: Deployment+Options
    canonical_source: 'https://doc.nuxeo.com/display/NXDOC/Deployment+Options'
    page_id: '950298'
    shortlink: GoAO
    shortlink_source: 'https://doc.nuxeo.com/x/GoAO'
    source_link: /display/NXDOC/Deployment+Options
tree_item_index: 100
history:
    -
        author: Manon Lumeau
        date: '2016-06-09 12:29'
        message: ''
        version: '42'
    -
        author: Thibaud Arguillere
        date: '2016-05-27 19:39'
        message: ''
        version: '41'
    -
        author: Solen Guitter
        date: '2016-03-29 14:15'
        message: Fix title capitalization and typos
        version: '40'
    -
        author: Thibaud Arguillere
        date: '2016-03-22 16:01'
        message: ''
        version: '39'
    -
        author: Solen Guitter
        date: '2015-10-15 13:33'
        message: Update related pages
        version: '38'
    -
        author: Alain Escaffre
        date: '2015-10-13 14:03'
        message: ''
        version: '37'
    -
        author: Solen Guitter
        date: '2014-11-20 10:21'
        message: ''
        version: '36'
    -
        author: Thierry Delprat
        date: '2014-11-19 23:38'
        message: ''
        version: '35'
    -
        author: Thierry Delprat
        date: '2014-11-19 23:37'
        message: ''
        version: '34'
    -
        author: Thierry Delprat
        date: '2014-11-19 23:29'
        message: ''
        version: '33'
    -
        author: Thierry Delprat
        date: '2014-11-19 21:23'
        message: ''
        version: '32'
    -
        author: Thierry Delprat
        date: '2014-11-19 21:03'
        message: ''
        version: '31'
    -
        author: Alain Escaffre
        date: '2014-11-02 15:21'
        message: ''
        version: '30'
    -
        author: Solen Guitter
        date: '2014-09-24 11:20'
        message: merging current page with Data segregation page
        version: '29'
    -
        author: Solen Guitter
        date: '2014-09-19 12:01'
        message: ''
        version: '28'
    -
        author: Solen Guitter
        date: '2014-01-21 18:48'
        message: ''
        version: '27'
    -
        author: Solen Guitter
        date: '2014-01-21 18:48'
        message: Added related topics
        version: '26'
    -
        author: Thierry Delprat
        date: '2014-01-20 19:04'
        message: ''
        version: '25'
    -
        author: Thierry Delprat
        date: '2014-01-20 18:40'
        message: ''
        version: '24'
    -
        author: Thierry Delprat
        date: '2014-01-20 18:09'
        message: ''
        version: '23'
    -
        author: Thierry Delprat
        date: '2014-01-20 16:46'
        message: ''
        version: '22'
    -
        author: Solen Guitter
        date: '2013-12-27 14:41'
        message: ''
        version: '21'
    -
        author: Thierry Delprat
        date: '2013-12-13 11:39'
        message: ''
        version: '20'
    -
        author: Solen Guitter
        date: '2013-10-17 11:17'
        message: ''
        version: '19'
    -
        author: Alain Escaffre
        date: '2013-10-16 01:45'
        message: ''
        version: '18'
    -
        author: Solen Guitter
        date: '2013-09-20 09:51'
        message: Fixed typos
        version: '17'
    -
        author: Alain Escaffre
        date: '2013-09-17 04:06'
        message: ''
        version: '16'
    -
        author: Solen Guitter
        date: '2013-09-04 14:57'
        message: ''
        version: '15'
    -
        author: Solen Guitter
        date: '2013-04-08 14:42'
        message: ''
        version: '14'
    -
        author: Florent Guillaume
        date: '2013-03-30 00:28'
        message: ''
        version: '13'
    -
        author: Solen Guitter
        date: '2012-09-06 15:39'
        message: Migrated to Confluence 4.0
        version: '12'
    -
        author: Solen Guitter
        date: '2012-09-06 15:39'
        message: ''
        version: '11'
    -
        author: Solen Guitter
        date: '2011-01-07 11:19'
        message: added toc
        version: '10'
    -
        author: Solen Guitter
        date: '2011-01-07 11:18'
        message: ''
        version: '9'
    -
        author: Thierry Delprat
        date: '2010-10-19 13:54'
        message: ''
        version: '8'
    -
        author: Thierry Delprat
        date: '2010-10-19 13:49'
        message: ''
        version: '7'
    -
        author: Thierry Delprat
        date: '2010-06-14 12:02'
        message: ''
        version: '6'
    -
        author: Thierry Delprat
        date: '2010-06-14 02:41'
        message: ''
        version: '5'
    -
        author: Thierry Delprat
        date: '2010-06-14 02:38'
        message: ''
        version: '4'
    -
        author: Thierry Delprat
        date: '2010-05-25 12:12'
        message: ''
        version: '3'
    -
        author: Thierry Delprat
        date: '2010-05-24 19:23'
        message: ''
        version: '2'
    -
        author: Admin name placeholder
        date: '2010-03-01 00:55'
        message: ''
        version: '1'

---
{{! excerpt}}
This page details standard architecture options to deploy a Nuxeo cluster.
{{! /excerpt}}

Setting up a Nuxeo cluster consists in answering to three main constraint types, independently or in combination with the others:
1. **Scalability** - My setup has to scale easily without sacrificing performances to adapt to a varying load.
1. **Failover** - When something goes wrong, I should be able to restore service quickly, losing as little data as possible in the process.
1. **High Availability** - My service should always be available, no matter what happens.

## Cluster Basics

In order to scale out and provide high availability (HA), Nuxeo provides a simple clustering solution. When cluster mode is enabled, you can have several Nuxeo server nodes connected to the same database server: you can then simply add more Nuxeo server nodes if you need to serve more requests. 

Nuxeo cluster mode also manages the required cache invalidation between the nodes. There is no need to activate any application server level cluster mode: cluster mode works without a dedicated application server. The default caching implementation uses simple JVM Memory, but we recommend using Redis to better handle cache invalidation.

Several architecture diagrams will be detailed below: 
- a logical architecture diagram to explain the recommended architecture with all components,
- an HA architecture diagram to see how you could translate the logical architecture for a physical deployment,
- a compact deployment option that will be particularly interesting where the number of machines could quickly become an issue.

## Logical Architecture

![]({{file name='nuxeo-cluster-logical-architecture.png'}} ?border=true)

This diagram represents the recommended architecture for a Nuxeo cluster.
- Two load balancers in front with sticky sessions handle incoming requests and direct them to the appropriate Nuxeo server nodes.
- Each Nuxeo server node is protected by a reverse proxy (usually Apache or Nginx).
- At least two Nuxeo server nodes are available. You can add any number of nodes to scale out performances.
- At least three nodes are available for the Elasticsearch cluster. Same for Redis. Contrarily to Nuxeo server nodes, these two components always require an odd number of nodes, which means you need to add at least two when wishing to scale out performances.
- Database system should provide high availability. Each solution has its own options for this, therefore we can't go into further details here.
- A shared file system is used to store binary files.

### Deployment Options
This diagram translates perfectly for a cloud based deployment. Considering Amazon AWS as a possible cloud infrastructure provider:
- The AWS ELB would be used for load balancing.
- EC2 instances can be used for the Nuxeo server nodes. We provide a [Nuxeo server CloudFormation template]({{page page='deploying-nuxeo-on-amazon-aws'}}) to help in that regard.
- EC2 instances can be used for Elasticsearch cluster nodes too. The Amazon ElasticCache service does not provide the required APIs at this point to allow us to have a completely managed cluster.
- Amazon ElasticCache can be used for a managed Redis cluster. Another option is to have a cluster hosted and managed by RedisLabs.
- Database can be handled through Amazon RDS. MongoDB Atlas is also an option for a hosted MongoDB cluster.
- An Amazon S3 bucket can be used for replicated file storage.

## High Availability Architecture

![]({{file name='nuxeo-cluster-ha-architecture.png'}} ?border=true)

This diagram shows how the logical architecture can translate in terms of physical deployment and installation sharing.
- The load balancers are usually deployed on separate machines from where the Nuxeo server nodes will be, as otherwise stopping a Nuxeo node could have consequences on serving the requests.
- On the machines where Nuxeo server nodes will be installed, a reverse proxy can be installed as well. It is lightweight, and having a reverse proxy for each Nuxeo node makes sense: if it fails for some reason, only the Nuxeo node behind it will be affected.
- Redis can also be installed on the same physical machine as Nuxeo server: our Redis usage is usually low enough for that.
- Elasticsearch nodes have to be installed on dedicated machines: for performance reasons Elasticsearch

### Deployment Options

## Compact Deployment

The compact deployment architecture is well suited for on premise deployment. The number of machines to install is low and their installation can be automated easily, ensuring scalability when needed.

![]({{file name='compact-deployment-numbered.png'}} ?w=1180,h=786,thumbnail=true,border=true)

In this architecture:
1. A load balancer with sticky sessions is used, as well as a reverse proxy.
2. A total of three machines are prepared for the application cluster. Each machine holds a Nuxeo server node, and an Elasticsearch node. More machines can be added later for scalability purpose.

{{#> callout type='info' heading='Number of Machines'}}
In this setup, **you always need to have an odd number of machines** (3, 5, 7...). This is tied to the fact Elasticsearch always needs to have an odd number of nodes in order to safely handle failover when a network partioning error occurs. Imagine that your cluster gets cut in half: 2 nodes on side A cannot communicate anymore with the third node on side B. In this situation, if the master node is the one isolated on side B, failover can be achieved properly because a majority (the 2 nodes on side A) can elect a new master node between them and keep service available. If you had 4 nodes in the same situation, service wouldn't be available anymore because a majority could not be obtained when voting. This is known as the split-brain problem. This also means that the minimum number of nodes to obtain high availability is of 3.
{{/callout}}

3. The machines described at step will all connect to the same database server.
4. A single Redis node is used.
5. File storage is done on a replicated filesystem.

### Limitations
#### Potential Single Point of Failures
Two potential single point of failures exist in this architecture: the Redis server and the database server.

##### Database Server
The database server is the most impacting of the two, as having it fail means not being able to store or retrieve documents anymore. To prevent the database server from becoming a single point of failure, you have several options:

- Use database replication
- Use a clusterized database (like Oracle RAC)
- Use a distributed / failsafe database like MongoDB

##### Redis Server
Redis server is known to be very resilient, and is less impacting when failing ; this is why we considered deploying it as a single node in our architecture schema. If it ever fails, consequences will be rather low as it mainly stores transient data, but you would still lose pending asynchronous jobs in the process. Losing these jobs will result in a loss of features in the application, but will not prevent it from working overall. 

Depending on the importance of these jobs in your application (for instance, they could be considered mission critical in a DAM application), you have options to provide high availability using Redis:

//TODO determine what we want to recommend exactly for persistence, see https://redis.io/topics/persistence

- Use Redis with <a href="https://redis.io/topics/sentinel" target="_blank">Sentinel</a>: in this case, you will need at least 3 Redis nodes to prevent the split-brain problem.
- Use Redis Entreprise Solution.

#### Disk Becomes the Main Bottleneck
Since Nuxeo server nodes are installed on the same machine as Elasticsearch nodes, disk access may quickly become a bottleneck in terms of performances.

Depending on the UI framework used for presentation layer, the network load balancing may need to be stateful.

Typically:

- JSF Backoffice UI is stateful,
- WebEngine and HTML/JS based UI are mainly stateless.

Anyway, even with JSF:

- Authentication can be transparent if you use a SSO system,
- The Nuxeo Platform knows how to restore a JSF view from a URL (most Nuxeo JSF views are bound to REST URLs).

{{#> callout type='tip' }}
For more information, please see the page [Setting up a HA Configuration Using the Nuxeo Platform and PostgreSQL]({{page page='setting-up-a-ha-configuration-using-the-nuxeo-platform-and-postgresql'}}).
{{/callout}}

### Scaling out Processing

<div class="table-scroll"><table class="hover">
<tbody>
<tr>
<td colspan="1">
![]({{file name='cluster.png'}} ?w=500)</td>
<td colspan="1">Nuxeo Cluster system by itself allows to scale out processing:
you can add new Nuxeo nodes as the number of requests increase.</td>
</tr>
</tbody>
</table>
</div>

### Dedicated Processing Nodes

The async tasks can be managed in a distributed way using the&nbsp;[WorkManager]({{page page='work-and-workmanager'}})&nbsp;and Redis.

This can be used to have some nodes of the Cluster dedicated to some heavy processing like Picture or Video conversions.

![]({{file name='dedicated.png'}} ?w=500,h=289,border=true)

Having such a demarcation between nodes is also a good way to be sure that async processing won't slow down Interactive processing.

### Scaling out the Storage

As seen before, it is easy to scale out processing on Nuxeo Platform.

![]({{file name='Cluster-Big.png'}} ?w=300,h=255,border=true)

However, at some point, you may also need to be able to scale out the Storage layer: we provide several options for that.

#### Scaling the Queries&nbsp;

When correctly configured, most databases can handle a heavy load of Store and Retrieve operations: the first bottleneck is usually complex queries.

So, a first solution to Scale out the Storage Layer is to split the work between:

- The DataBase&nbsp;
    - Focus on Store & Retrieve operation
    - Small technical queries
- Elasticsearch index
    - Handle complex search used to build the screens
    - Can also be used to retrieve the document that is fully stored in the index.

At the Nuxeo level, directing a query to the Repository Database or to Elasticsearch is just a matter of configuration: code and query remain the same.

This approach allows to leverage Elasticsearch capability:

- Very fast query engine
- Capability to scale out easily

![]({{file name='Cluster-ES.png'}} ?w=500,h=284,border=true)

#### Sharding on several Databases

Unlike Nuxeo Nodes, the Database server nodes can not be simply added to handle more load:

- Multi-masters SQL DB architecture (like Oracle RAC) work but don't really provide scale out, only HA.
- Leveraging replicated ReadOnly SQL DB nodes is complex in terms of transaction management

However, the Nuxeo Platform does provide a way to scale out the data: using several repositories.
The idea is that a single Nuxeo application can be bound to several repositories, each repository being a DB instance and a BlobStore.&nbsp;So, if one application is connected to two repositories, the data will be partitioned between two couples (ex: (DB+FS) + (DB+S3) ).

The repositories are like mount points: The default configuration is to have only one repository named "Default Repository" and mounted under&nbsp;`/default/`. But you can add new repositories as needed. These new repositories will appear inside the application as several content roots. This typically means that when accessing a document, you have to know what is the host repository.

Typical use cases for data partitioning include:

**Selecting your storage type according to the needs**

- Partitioning&nbsp;between Live and Archive documents:
    - Archive&nbsp;

        - Storage: slower but massive cheap storage that can scale
        - Indexes: add indexes on the database to make search faster (few Write)
    - Live
        - Storage: fast storage to make work faster, lower volume
        - Indexes: fast database with few index to maximize write speed
- Partitioning between read-only and read-write repositories

    - Have a read-write repository
    - Have a read-only replicated repository

**Selecting the storage according to the isolation policy**

- Data for "clientX" goes in "repositoryX"
- Partitioning between types of documents or document status:
    - Published documents in a public repository
    - Working documents in a restricted repository

This data partitioning is visible to user, but thanks to Elasticsearch we can provide a unified Index&nbsp;

![]({{file name='multi.png'}} ?w=500,h=421,border=true)

This type of sharing has recently been tested during a performance benchmark using 10 PostgreSQL databases to reach a total of [1 Billion documents](http://www.nuxeo.com/blog/one-billion-documents/).

![]({{file name='1B.png'}} ?w=500,h=372,border=true)

#### Leveraging NoSQL and Distributed Storage

One the key advantages of NoSQL Storage like MongoDB is that they allow to scale out by simply adding nodes to the cluster and propose natively sharding on the nodes.

## Cloud & PaaS and Deployment Automation

### Nuxeo & AWS

To be able to run efficiently on the Cloud, you need to be able to use as much as possible the infrastructure of the Cloud Provider: in the case of AWS, there are a lot of services that you want to be able to use.

Nuxeo Platform, makes it easy since:

- We are standard based
- The pluggable component model (Extension Point) allows to easily change backend implementation when needed

That's why leveraging AWS infrastructure was almost a natural fit for Nuxeo:

- Meta-Data Store: Oracle RDS or PostgreSQL RDS
    - Native plug (nothing specific to AWS)
- Binary Store: S3 Binary Store
    - Our BinaryManager is pluggable and we use it to leverage the S3 Storage capabilities
- Cache: ElasticCache / Redis
    - Our cache infrastructure is pluggable to support Redis
    - Our distributed Job queuing was already Redis based

The same idea is true for all the Cloud Specific services like provisioning and monitoring.

We try to provide everything so that the deployment in the target IaaS is easy and painless:&nbsp;

- Nuxeo is packaged as Debian packages (this is one of the available packaging)

    - We can easily setup Nuxeo on top of AMI
    - We&nbsp;can&nbsp;use&nbsp;CloudFormation
- Nuxeo exposes its metrics via JMX
    - CloudWatch can monitor Nuxeo
    - We&nbsp;can&nbsp;use&nbsp;AutoScaling

<div><span class="text plain"><span class="meta paragraph text">![]({{file name='aws.png'}} ?w=500,h=320,border=true)
</span></span></div>

### Platform as a Service and nuxeo.io

Cloud infrastructure pricing is a complex task: you just need to take a look at the AWS pricing rules to be convinced of that.

However, there are great optimizations opportunities:

- Reserved instance are significantly cheaper if you can commit in long term
- Sport instances can be a great solution if you can cope with their transient nature

Being able to leverage these opportunities implies to distribute the applications parts across enough VM so that:

- You can use all the resources available
- You can loose VMs without breaking the system

At Nuxeo, we use Docker to multiplex several Nuxeo Applications on top of a set of AWS VMs running CoreOS.

Using this architecture provide high resilience, fast scale out and a very efficient performance / cost ratio.

This was one of the starting point of the[ nuxeo.io ]({{page page='platform-as-a-service'}})architecture that uses&nbsp;[Docker](http://www.nuxeo.com/blog/docker-containers-nuxeo-part-1/)&nbsp;to provide on demande Nuxeo Platform deployment.

## <span style="color: rgb(0,0,0);">Other Deployment Options</span>

### Hot Standby (DRP)

If you want to provide a Disaster Recovery Plan, you need to host two separated Nuxeo infrastructures and be sure you can switch from one to an another in case of problem.

The first step is to deploy two Nuxeo infrastructures on two hosting sites. These infrastructure can be mono-VM, cluster or multi-VM. The key point is to provide a way for each hosting site to have the same vision of the data:

- SQL data stored in the SQL database server,
- Filesystem data.

Because Nuxeo storage VCS+Filesystem is safe, you can use a replication system between the two sites. Basically, you can use the replication/standby solution provided by the database server you choose. This replication tool just has to be transactional.

For the filesystem, any replication system like RSync can be used.

Because the blobs are referenced by their digest in the database, you don't have to care about synchronization between the DB and FS: In the worst case, you will have blobs that are not referenced by the DB on the replicated site.

This kind of DRP solution has been successfully tested in production environment using:

- PosgreSQL stand-by solution (WAL shipping),
- RSync for the file system.

![]({{file name='HA.jpg'}} ?w=500,border=true)

{{#> callout type='note' }}

The Warm standby DB nodes are not used by Nuxeo active nodes.

{{/callout}}

### Read-Only Synchronization

The Nuxeo Platform being flexible, you can use several add-ons together to achieve a complex architecture:

- Use&nbsp;`nuxeo-platform-sync` to create a read-only copy of a remote repository;
- Use remote plublisher to push information between two distant Nuxeo instances;
- Use multi-repository support to segregate Local vs Central data.

![]({{file name='distant.png'}} ?w=500,h=417,border=true)

&nbsp;

* * *

<div class="row" data-equalizer data-equalize-on="medium"><div class="column medium-6">{{#> panel heading='Related pages in this documentation'}}

- [Understanding Bundles Deployment]({{page page='understanding-bundles-deployment'}})
- [Platform as a Service]({{page page='platform-as-a-service'}})
- [Nuxeo and Redis]({{page page='nuxeo-and-redis'}})
- [Nuxeo Clustering Configuration]({{page page='nuxeo-clustering-configuration'}})

{{/panel}}</div><div class="column medium-6">

&nbsp;

&nbsp;

</div></div>
