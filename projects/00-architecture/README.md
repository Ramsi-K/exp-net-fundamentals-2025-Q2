# Bayko & Brown: CloudToon Studio

(AKA: Agent-Powered Cartoon Generation Pipeline)

## 🔹 Overview

**Bayko & Brown** is a secure, cloud-native pipeline that transforms user prompts into fully generated comic strips using GenAI agents in isolated VPCs.

The system demonstrates advanced AWS networking principles including VPC design, cross-VPC communication via S3, subnet isolation, secure firewalls, and event-driven workflows.

---

## 💡 Use Case

A user enters a storytelling prompt via a secure WebUI (like Andrew's Smart TV).  
The system responds with:

- Stylized dialogue
- Rendered comic panels
- Optional voiceover narration

Behind the scenes, two agents — Bayko and Brown — process and generate the comic collaboratively while remaining isolated via network boundaries.

---

## 📚 Architecture Diagrams

This project includes a full suite of system diagrams in [architecture.md](./architecture.md), covering:

- 🧠 System Architecture Overview
- 🔁 Agent Processing Flow
- 🔀 MCP Subsystem Orchestration
- 📦 Output Artifact Structure
- 🔐 Network Security & Isolation

Each diagram is rendered using Mermaid and maps directly to the actual infrastructure and agent logic used in the pipeline.

---

## 👥 Agent Roles

Detailed breakdown of each GenAI agent is available in [agents.md](./agents.md):

- 🤖 **Agent Brown**: Input validator, style tagger, and storyboard author
- 🧠 **Agent Bayko**: MCP-driven backend agent for image, audio, and video generation

Covers toolchain decisions, moderation logic, and agent boundaries.

---

## 🎬 Pipeline Steps

1. **User enters prompt via WebUI (external interface)**

   - Frontend interface (Smart TV style)
   - Sends the prompt to Agent Brown via API Gateway or ALB (VPC-Brown)

2. **Agent Brown processes the prompt**

   - Sanitizes, styles, and tags the request
   - Creates `storyboard.json` with layout, dialogue, UUID, metadata
   - Writes it to S3 “window” bucket (shared resource)

3. **S3 triggers Agent Bayko (VPC-Bayko)**

   - Via S3 event or EventBridge
   - Bayko receives `storyboard.json` and begins generation

4. **Agent Bayko uses MCP internally**

   - **MCP is a protocol inside Bayko**, not an external router
   - Bayko uses it to:
     - Choose between SDXL or other tools
     - Decide if TTS is needed
     - Assemble toolchain for current task
     - Optionally spawn subagents or use modal tools
   - All decisions are logged or passed through a planner module

5. **Bayko generates the full comic output**

   - Generates dialogue (if needed), renders frames
   - Adds narration/subtitles if requested
   - Outputs media as `.mp4`, `.zip`, or image bundle

6. **Bayko writes to Output S3 ("Jellyfin Server")**

   - Stored under `output/{UUID}/final.mp4`
   - Contains images, audio, captions, metadata, logs

7. **Agent Brown detects output and responds to WebUI**
   - Delivers signed URL (CloudFront or pre-signed S3)
   - Optionally logs session metadata

---

## 📦 Infra & Roles Overview

| Component          | Role                                         | Service                                   |
| ------------------ | -------------------------------------------- | ----------------------------------------- |
| **User**           | External request initiator                   | Enters via public API Gateway (VPC-Brown) |
| **Agent Brown**    | Frontend agent (dialogue intake, validation) | Lambda/API behind ALB/NLB in VPC-Brown    |
| **S3 Bucket**      | “Window” for agent comms                     | Shared AWS S3 with access policy          |
| **Agent Bayko**    | Backend agent (animation, voice)             | Lambda/API in VPC-Bayko                   |
| **Output S3**      | Comic/video delivery bucket                  | Public-read S3 or CloudFront              |
| **Optional Tools** | Logging, Moderation, TTS                     | Lambdas or Docker containers              |

---

## 🚀 Deployment Plan

See [`deployment.md`](./deployment.md) for full setup instructions and architecture rollout.

---

## 🛠️ Technologies Used

- **AWS VPC, Subnets, Routing Tables, NACLs, Security Groups**
- **Lambda** for trigger/event logic
- **API Gateway** for public entrypoint
- **S3** as communication bridge
- **EventBridge** for orchestration (optional)
- **LLMs** (OpenAI / Claude / HuggingFace) for dialogue
- **Stable Diffusion / ComfyUI** for image generation
- **Modal / Docker** for secure inference hosting
- **CloudFront (Optional)** for fast public delivery

---

## 🛠️ Included Capabilities

| Capability              | Description                                              |
| ----------------------- | -------------------------------------------------------- |
| **MCP Routing**         | Agent-layer routing + tool/subagent selection            |
| **Session Logging**     | UUID tracking for multi-user comic histories             |
| **Moderation Tools**    | Agent Brown includes moderation + content filters        |
| **WebUI**               | Replaces Smart TV UI with secure entry point             |
| **Voice + Animation**   | Audio synthesis + animated frame sequencing              |
| **Firewall Simulation** | Enterprise-grade no-backflow setup with layered security |

---

## 🧠 Networking Concepts Mapped

| Bootcamp Concept           | Where It Shows Up                                                                          |
| -------------------------- | ------------------------------------------------------------------------------------------ |
| VPCs & Subnets             | Bayko and Brown are in separate VPCs                                                       |
| Public/Private Networking  | Public APIs, private inference workloads                                                   |
| Firewalls / SGs            | No agent-to-agent direct communication                                                     |
| L4 Firewall Isolation      | Bayko cannot receive inbound traffic from Brown; traffic must flow via S3/EventBridge only |
| NAT Gateway                | Bayko's outbound traffic routed through NAT                                                |
| S3 as Network Bus          | White box "window" analogy for inter-agent comms                                           |
| Load Balancer (ALB/NLB)    | ALB fronts Agent Brown                                                                     |
| Bastion Host / VPN         | Optional intranet access for Bayko                                                         |
| CloudWatch Logs            | Used for story failures, moderation, or trace capture                                      |
| Wireshark-style Monitoring | Simulated via logging Lambda                                                               |

---

## 🔐 Security Philosophy

This system mimics secure enterprise infrastructure:

- No direct A2A traffic
- All agent interaction flows through monitored “windows” (S3)
- Layer 4 firewalls prevent direct ingress to Bayko — access only via triggers
- Optional NAT Gateway + VPC peering simulate advanced network boundaries
- Lambdas serve as trusted relays only — no wide-open ingress

## ⚙️ Example Prompt

```text
Prompt: “A moody K-pop idol finds a puppy on the street. It changes everything.”
Style: 4-panel, Studio Ghibli, whisper-soft lighting
Language: Korean with English subtitles
Extras: Narration + backing music
```

---
