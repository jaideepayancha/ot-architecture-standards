# Cloud Ingestion Architecture

## Approved Platforms

- Azure
- AWS
- GCP

## Ingestion Methods

| Platform | Method |
|--------|--------|
| Azure | IoT Hub / Event Hub |
| AWS | IoT Core / Kinesis |
| GCP | Pub/Sub |

## Security

- TLS only
- Certificate-based auth
- No shared keys

## DMZ Services

All cloud connections originate from:

Industrial DMZ only

## Rate Control

- Throttling to protect WAN
- Burst buffering at site
