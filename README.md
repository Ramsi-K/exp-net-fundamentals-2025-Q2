# Networking Fundamentals Bootcamp 2025 - Custom Project

**Andrew Brown & Tim McConnaughy** | **Custom Implementation Path**

This repository documents my work in the 2025 Networking Fundamentals Bootcamp. **I deviated from the standard demo path** to build an original infrastructure project that demonstrates the same core networking concepts through a production-grade multi-agent orchestration system.

## 🎯 Project Overview

> This repo does not follow the bootcamp example project.

**Bayko & Brown**: a secure multi-agent orchestration system that demonstrates enterprise networking patterns through:

- **VPC Isolation**: Two isolated agents across separate VPCs with controlled communication
- **Cross-VPC Coordination**: Secure agent communication via S3 and EventBridge
- **Network Security**: Layer 4 firewalls, IAM policies, and zero-trust architecture
- **Event-Driven Workflows**: Asynchronous processing with monitoring and observability

## 📊 Bootcamp Topics → Project Mapping

| **Bootcamp Topic**        | **My Implementation**                               |
| ------------------------- | --------------------------------------------------- |
| **VPC Design**            | Dual-VPC architecture (Brown-Public, Bayko-Private) |
| **Firewall Rules**        | Security groups with Layer 4 isolation              |
| **IP Address Management** | Subnet design (10.0.0.0/16, 10.1.0.0/16)            |
| **NAT Gateways**          | Private subnet outbound-only access                 |
| **Load Balancers**        | Application Load Balancer for public tier           |
| **Network Monitoring**    | CloudWatch logging and performance metrics          |
| **Traffic Flow**          | Cross-VPC communication patterns via S3/EventBridge |
| **Zero-Trust**            | No direct agent-to-agent communication              |

## 🏗️ Architecture Highlights

- **Agent Brown (Public VPC)**: Input validation, request routing, session management
- **Agent Bayko (Private VPC)**: Backend processing, tool orchestration, output assembly
- **S3 Communication Bridge**: Secure cross-VPC message passing
- **EventBridge Orchestration**: Event-driven workflow triggers
- **CloudFront CDN**: Secure content delivery with signed URLs

## 📁 Repository Structure

```
├── projects/
│   ├── 00-architecture/          # Main project documentation
│   │   ├── README.md             # Project overview
│   │   ├── architecture.md       # System diagrams and design
│   │   ├── agents.md             # Agent responsibilities
│   │   ├── deployment.md         # Infrastructure setup
│   │   └── assets/diagrams/      # Mermaid diagrams
│   ├── 01-week1/                 # Week 1 deliverables
│   └── 02-week2/                 # Week 2 deliverables
├── journal/
│   ├── 00-architecture/          # journal for project 00
├── notes/
│   ├── OSI-babas-chakras.md      # mapping OSI layers to chakras
│   ├── glossary.md               # glossary of terms encountered
└── README.md                     # This file
```

## 🎓 Bootcamp Compliance

This custom project covers all required networking fundamentals:

✅ **VPC Design & Subnetting**  
✅ **Security Groups & Firewall Rules**  
✅ **Cross-Network Communication**  
✅ **Load Balancing & Traffic Management**  
✅ **Network Monitoring & Observability**  
✅ **Zero-Trust Security Patterns**

## 🧠 Notes

- Project intentionally diverges from bootcamp demo
- Architecture focuses on cloud-native networking patterns
- All deliverables submitted under respective topic folders as required
- Architectural diagrams, logs, and deployment details are located in `00-architecture/`

## 💼 Demonstrated Value

This project demonstrates enterprise-level skills in:

- Multi-tier network architecture
- Secure agent isolation patterns
- Event-driven system design
- Production monitoring and observability
- Infrastructure as Code practices

---

**Built by Ramsi Kalia** | [LinkedIn](https://linkedin.com/in/ramsikalia) | **Networking Fundamentals Bootcamp 2025**
