
# AWS Cloud Infrastructure Architecture

## Project Overview

This project demonstrates basic AWS networking and cloud infrastructure.

## Architecture Diagram

```mermaid
flowchart TB
    U["Internet Users"]
    IGW["Internet Gateway"]
    RT["Public Route Table"]

    subgraph VPC["AWS VPC"]
        subgraph PUB["Public Subnet"]
            EC2["EC2 Instance"]
            SG["Security Group"]
        end

        subgraph PRIV["Private Subnets"]
            PS["Private Subnets"]
        end
    end

    S3["Amazon S3 - Website Files"]

    U --> IGW
    IGW --> RT
    RT --> EC2
    SG -.-> EC2
    U -.-> S3
```

## AWS Resources

- VPC and Subnets
- EC2 Instance
- Security Groups
- Internet Gateway
- Route Tables
- Amazon S3

## Notes

This is a logical overview of the project.
Actual network routes and resource configuration may vary.
```
