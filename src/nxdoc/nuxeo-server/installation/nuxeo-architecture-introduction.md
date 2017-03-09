---
title: Nuxeo Architecture Introduction
description: This page covers the elements that can be included in a production ready Nuxeo architecture.
labels:
    - deployment
    - architecture
review:
    date: '2017-02-22'
    status: ok
    comment: ''
toc: true
tree_item_index: 90
---

{{! excerpt}}

This page covers the elements that can be included in a production ready Nuxeo architecture.

{{! /excerpt}}

![]({{file name='../standard-cluster-architecture/nuxeo-cluster-logical-architecture.png'}} ?border=true)

A Nuxeo architecture is composed of the following elements:
- A load balancer,
- A reverse proxy,
- A Nuxeo server node or cluster,
- A database Nuxeo can connect to,
- An Elasticsearch cluster,
- A Redis cluster,
- A filesystem where binaries will be stored.

We will quickly introduce these items below.

## Load Balancer

The load balancer is used to allocate load between the Nuxeo nodes, or potentially to redirect queries to specific nodes. In all cases (even if you use Nuxeo as a bare server without a UI), a load balancer with sticky sessions is mandatory.

## Reverse Proxy

A reverse proxy is used to avoid users from accessing the Nuxeo server directly. One simple rule you have to follow is that on a production setup, your Nuxeo server should *never* be exposed directly. Setting up a reverse proxy brings many benefits on performance and security aspects:

- HTTPS/SSL encryption
- HTTP caching
- URL rewritting

![]({{file name='reverse.png'}} ?w=500,h=349,border=true)

Additionally, when some clients use a WAN to access the server, the reverse proxy can also be used to protect the server against slow connections that may use server side resources during a long time. You may refer to the [reverse proxy configuration]({{page page='http-and-https-reverse-proxy-configuration'}}) for more details.

## Nuxeo Server

The Nuxeo server can be installed in a variety of ways, including a docker container, a VM image, a debian repository, or a simple cross-platform zip file. It is distributed in a prepackaged Tomcat server that includes Nuxeo, a transaction manager (JTA), a pool manager (JCA). The WAR file is generated dynamically upon each Nuxeo server restart, allowing easy configuration changes and customization deployment. Further information on this subject can be found in the [Understanding Bundles Deployment]({{page page='understanding-bundles-deployment'}}) documentation.

The Nuxeo server can be deployed anywhere, including as an embedded tool. Having a lightweight embedded Nuxeo server is a solution commonly used for unit testing or offline access. For the latter, the Nuxeo server would be embedded client side (for instance in a tablet) to allow offline access, and would synchronize with a central Nuxeo server when going back online.

## Database

The database is a core component for your Nuxeo infrastructure, since it will store all document properties, and will be used as well for various queries. Nuxeo supports many databases ;  among them, MongoDB and PostgreSQL are the ones that are considered to provide the best overall performances currently for Nuxeo usage. Please refer to our [database configuration]({{page page='database-configuration'}}) documentation for further details.

{{#> callout type='info'}}
When choosing MongoDB, a relational database (e.g. PostgreSQL, Oracle...) is still needed for now. Using MongoDB as the only database in your infrastructure is a work in progress that will be supported in Nuxeo LTS 2016 and above through optional addons.
{{/callout}}

## Elasticsearch

Elasticsearch is used to relieve the database from the costliest operations. 
- It keeps indexes on the documents in order to allow blazingly fast searches and modern search options like real time filtering (aka facets), even on very high volumes.
- It stores the documents audit log. Since every operation on a document in Nuxeo is stored for possible audit purpose, the corresponding table would grow very rapidly and possibly reach millions of tuples when stored in the database. Using Elasticsearch, this is not a problem anymore.
- It scales horizontally and provides constant performance even with growing content size.

Elasticsearch remains an optional component and can be deactivated if needed. But except for some specific use cases where installation size and setup steps highly matter (for instance when embedding a Nuxeo server), it is highly recommended to take advantage of it. Refer to the [Elasticsearch setup]({{page page='elasticsearch-setup'}}) documentation for more information.

## Redis

Redis is an optional but strongly recommended component for any Nuxeo cluster. It is mainly used to persist any [asynchronous job]({{page page='work-and-workmanager'}}) created by the Nuxeo server nodes. Fulltext content extraction from files, thumbnail generation, metadata extraction or write for pictures, video conversion tasks are all examples of such jobs. When a Redis instance or cluster is set up, you can safely stop your Nuxeo server nodes anytime without being worried of losing these jobs in the process.

Redis can also serve as a centralized caching tool, allowing to share cache between Nuxeo nodes for various data sources and thus preventing invalidation issues. You may refer to the [Nuxeo and Redis]({{page page='nuxeo-and-redis'}}) page for all details.

## File System

Nuxeo stores binaries attached to the documents on a file system by default, that can be a shared file system, a NAS, an Amazon S3 bucket, etc. More options are available depending on your target deployment. This is described in the [Storage Alternatives](#storage-alternatives) section below.

## Storage Alternatives

Nuxeo is pluggable so that it can be adapted to different deployment environments and use cases.

This means you can define _"where you want to manage your data"_ and because the answer may depend on the type of data, Nuxeo provides different types of backend for different types of storage.

### Document Storage

You can configure

- Where you store the Document metadata and hierarchy
    - SQL Database (PostgresSQL, Oracle, MSSQL, MySQL, Amazon RDS)
    - MongoDB
- Where you store the binary streams (the files you attach to documents)
    - Simple FileSystem
    - SQL Database
    - S3, Azure
    - Leveraging Content Delivery Networks for caching content securely all around the globe.

<div class="table-scroll">
    <table class="hover">
        <tbody>
            <tr>
                <td colspan="1">
                    ![]({{file name='VCS1.png'}} ?w=200,thumbnail=true)
                </td>
                <td colspan="1">
                    ![]({{file name='VCS2.png'}} ?w=200,thumbnail=true)
                </td>
                <td colspan="1">
                    ![]({{file name='DBS.png'}} ?w=200,h=317)
                </td>
            </tr>
            <tr>
                <td colspan="1">
                    **_PosgreSQL + FileSystem_**
                </td>
                <td colspan="1">
                    _**Oracle + S3**_
                </td>
                <td colspan="1">
                    _**MongoDB + S3**_
                </td>
            </tr>
        </tbody>
    </table>
</div>

### Indexes

You can also select where you store the indexes (including the full-text)

- SQL Database
- Elasticsearch

![]({{file name='ES-Single.png'}} ?w=300,h=213,border=true)

Since 6.0, the default configuration uses Elasticsearch.

### Others

In the same logic, you can choose:
- Where you store the caches and the transient data
    - In Memory (per instance basis)
    - Redis (shared memory)
- Where you store [Users and Groups]({{page page='data-lists-and-directories'}})
    - SQL Database
    - LDAP or Active Directory
    - Mix of both
    - External system
