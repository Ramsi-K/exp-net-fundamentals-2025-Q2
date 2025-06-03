# 🚀 Deployment Plan

1. **Provision VPC-Brown**

   - Deploy WebUI, API Gateway/ALB, and Agent Brown (Lambda or container)
   - Place logic in public/private subnets as needed

2. **Set up shared S3 bucket**

   - Acts as “window” for cross-VPC agent communication
   - Apply scoped IAM roles + bucket policies

3. **Provision VPC-Bayko**

   - Deploy Agent Bayko and toolchain (LLM, SD, TTS, etc.)
   - Use Modal or containerized runtime
   - Strict private subnet access with NAT or S3 endpoint

4. **Configure event triggers**

   - Use S3 Event or EventBridge to invoke Bayko on storyboard upload
   - Optional: Add moderation/logging Lambdas

5. **Establish IAM and security layers**

   - IAM: least-privilege roles for agents and triggers
   - SGs/NACLs: block A2A traffic, allow only necessary flows
   - NAT Gateway: route Bayko’s outbound-only comms

6. **Add delivery path**

   - CloudFront distribution or signed S3 URLs for final output
   - Optional: Add viewer access logging or expiring links

7. **Monitor and test full flow**
   - Use CloudWatch Logs for prompt handling, failures, and moderation
   - Trace full pipeline from WebUI → Brown → Bayko → Output → WebUI
