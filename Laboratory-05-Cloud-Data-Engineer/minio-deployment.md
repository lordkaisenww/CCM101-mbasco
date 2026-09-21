# MinIO Object Storage Deployment

## Overview
This document records the technical steps taken to deploy an S3-compatible object storage server (MinIO) using Docker on a KillerCoda Ubuntu Playground.

## Docker Command Used

```bash
docker run -d -p 9000:9000 -p 9001:9001 --name minio-server \
  -e "MINIO_ROOT_USER=cloudadmin" \
  -e "MINIO_ROOT_PASSWORD=CloudNova2026!" \
  quay.io/minio/minio server /data --console-address ":9001"
```

Note: the image was pulled from `quay.io/minio/minio` rather than Docker Hub's `minio/minio`, since MinIO's official image is no longer available on Docker Hub for anonymous pulls.

## Port Used to Access the Web Console
- **Port 9001** — the MinIO Web Console, accessed via the KillerCoda "Traffic / Ports" tab.
- Port 9000 is the S3-compatible API endpoint (not used for browser access).

## Bucket Created
- **Bucket name:** `client-photos`
- Created via the Buckets section of the MinIO Web Console, then used to upload a test file to confirm the deployment works end-to-end.

## Explanation of the -e (Environment Variable) Flags
The `-e` flags pass environment variables into the container at startup, which MinIO reads to configure itself instead of requiring a config file:
- `-e "MINIO_ROOT_USER=cloudadmin"` sets the administrator username used to log in to the MinIO server and its web console.
- `-e "MINIO_ROOT_PASSWORD=CloudNova2026!"` sets the administrator password paired with that username, securing access to the server.

This keeps credentials configurable per-deployment rather than hardcoded into the image, which is standard practice for containerized services.

## Evidence
- `screenshots/minio-deployed.png` — terminal showing the container running successfully.
- `screenshots/minio-bucket-upload.png` — MinIO web console showing the `client-photos` bucket with the uploaded file.
