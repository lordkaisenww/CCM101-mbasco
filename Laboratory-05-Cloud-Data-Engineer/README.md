# Laboratory 05 — Cloud Data Engineer

## Mission Overview
In this lab, I was assigned to the Cloud Data Engineering Team to help a client build a proof-of-concept object storage environment for a photo-sharing application. Since containers are ephemeral and can't be used to permanently store user-uploaded images, I deployed MinIO, an open-source, S3-compatible object storage server, using Docker on a KillerCoda Ubuntu Playground. I then created a storage bucket and uploaded a test file to confirm the system works.

## Objectives
- Differentiate between Block, File, and Object Storage.
- Deploy an S3-compatible Object Storage server (MinIO) using Docker.
- Access a cloud service via a web interface using port forwarding.
- Create a storage bucket and upload objects (files) to the cloud.
- Document cloud storage operations using Markdown.
- Continue expanding a professional GitHub Cloud Computing Portfolio.

## Tools Used
- **Docker** — to containerize and run the MinIO server.
- **MinIO** — S3-compatible object storage server software (pulled from `quay.io/minio/minio`).
- **KillerCoda Playground** — cloud sandbox environment (Ubuntu/Docker).
- **Git & GitHub** — version control and portfolio documentation.
- **Markdown** — technical documentation format.

## Skills Learned
- Differentiating block, file, and object storage and identifying appropriate use cases for each.
- Deploying a containerized service with multiple exposed ports and environment-variable-based configuration.
- Accessing a containerized web service through port forwarding in a cloud sandbox.
- Creating buckets and uploading objects through an S3-compatible web console.
- Troubleshooting a real-world deployment issue (deprecated Docker Hub image, resolved via `quay.io`).
- Writing clear technical documentation in Markdown for a cloud deployment.
