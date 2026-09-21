# Types of Cloud Storage: Block, File, and Object

## Comparison Table

| Storage Type | Description (How it stores data) | Primary Use Case | Cloud Provider Example |
|---|---|---|---|
| **Block Storage** | Stores data in blocks and provides storage that works similarly to a physical hard drive attached to a server. [1] | High-performance workloads that need direct and frequent access, such as databases and VM boot volumes. | AWS EBS [1] |
| **File Storage** | Stores data using a familiar file and folder structure that can be shared and accessed by multiple systems. [2] | Shared files, application data, home directories, and workloads that need a common file system. | AWS EFS [2] |
| **Object Storage** | Stores data as objects containing the data, metadata, and an identifier. Objects can be accessed and managed through APIs. [3] | Large amounts of unstructured data such as images, videos, documents, logs, and backups. | AWS S3 [3] |

## Why Object Storage Is the Best Choice for Client Photos

Object storage is a good choice for storing client photos because photos are unstructured files that can grow in number over time. Amazon S3 allows applications to store objects together with metadata, making the files easier to organize and manage. [3]

Object storage also keeps uploaded photos separate from the application's web server or container storage. This means the photos can remain available even when the application server is restarted, replaced, or redeployed. For a cloud-based application that handles many uploaded images, object storage provides a scalable and practical storage solution.

## References

[1] Amazon Web Services. "Amazon Elastic Block Store (EBS)." AWS Documentation.
https://docs.aws.amazon.com/ebs/

[2] Amazon Web Services. "Amazon Elastic File System (EFS)." AWS Documentation.
https://docs.aws.amazon.com/efs/

[3] Amazon Web Services. "Amazon Simple Storage Service (S3)." AWS Documentation.
https://docs.aws.amazon.com/s3/
