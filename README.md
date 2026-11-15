# Awesome AI Agents 2025

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)

> A comprehensive, curated list of cloud-based and commercial AI agent platforms, frameworks, and tools for 2025.

## Table of Contents

- [What are AI Agents in 2025?](#what-are-ai-agents-in-2025)
- [Types of AI Agents](#types-of-ai-agents)
- [Quick Start Guide](#quick-start-guide)
- [Top 50+ AI Agent Platforms](#top-50-ai-agent-platforms)
- [Platform Comparison Matrix](#platform-comparison-matrix)
- [Choosing the Right Platform](#choosing-the-right-platform)
- [Market Statistics](#market-statistics)
- [Documentation Index](#documentation-index)

---

## What are AI Agents in 2025?

AI agents in 2025 have evolved from simple chatbots to autonomous, goal-oriented systems capable of planning, executing, and adapting to complex workflows. Unlike traditional automation tools, modern AI agents can:

- **Reason and Plan**: Break down complex tasks into executable steps
- **Execute Autonomously**: Take actions across multiple systems without constant oversight
- **Learn and Adapt**: Improve performance based on feedback and outcomes
- **Collaborate**: Work with other agents and humans in sophisticated workflows

### Key Characteristics

| Feature | 2023 | 2025 |
|---------|------|------|
| Task Complexity | Single-step | Multi-step, multi-system |
| Autonomy Level | Assisted | Semi to fully autonomous |
| Learning | Static | Continuous adaptation |
| Collaboration | Isolated | Multi-agent coordination |
| Enterprise Readiness | Experimental | Production-grade |

### The Agentic AI Shift

According to industry research, 2025 marks the transition from AI "copilots" to true AI "agents":

- **Level 1**: Chatbots (reactive, single-turn)
- **Level 2**: Copilots (assistive, context-aware)
- **Level 3**: Agents (autonomous, goal-oriented) - **We are here**
- **Level 4**: Orchestrators (multi-agent coordination)

---

## Types of AI Agents

### Enterprise Platforms
Large-scale solutions designed for Fortune 500 companies with deep integrations, compliance features, and enterprise support.

**Examples**: Salesforce Agentforce, IBM watsonx, Microsoft Copilot Studio

[View Enterprise Platforms Guide](ENTERPRISE-PLATFORMS.md)

### Cloud Provider Services
AI agent services from major cloud providers, offering scalability, security, and integration with existing cloud infrastructure.

**Examples**: AWS Bedrock Agents, Google Vertex AI Agent Builder, Azure AI Foundry

[View Cloud Platforms Guide](CLOUD-PLATFORMS.md)

### No-Code Builders
Visual, drag-and-drop platforms enabling non-technical users to create AI agents without programming.

**Examples**: Lindy, Zapier Agents, Gumloop, StackAI

[View No-Code Builders Guide](NO-CODE-BUILDERS.md)

### Specialized Agents
Purpose-built agents optimized for specific domains like coding, customer service, or voice interactions.

**Examples**: Devin AI, Cognosys, OpenAI Operator, Sierra

[View Specialized Agents Guide](SPECIALIZED-AGENTS.md)

### Developer Frameworks
Open-source and commercial frameworks for building custom AI agents with full control over architecture.

**Examples**: LangChain, LangGraph, CrewAI, AutoGen, OpenAI Swarm

[View Agentic Frameworks Guide](AGENTIC-FRAMEWORKS.md)

---

## Quick Start Guide

### For Enterprises (Non-Technical Teams)

1. **Evaluate Your Ecosystem**: Choose platforms that integrate with your existing stack
   - Salesforce users -> Agentforce
   - Microsoft 365 -> Copilot Studio
   - AWS infrastructure -> Bedrock Agents

2. **Start with a Pilot**: Begin with a single use case (e.g., customer support, sales automation)

3. **Consider Governance**: Ensure the platform meets your compliance requirements (SOC 2, GDPR, HIPAA)

### For Business Users (No-Code)

1. **Choose a No-Code Builder**:
   - Quick start: [Lindy](https://lindy.ai) - Visual builder with 3000+ integrations
   - Integration-focused: [Zapier Agents](https://zapier.com) - 8000+ app connections
   - Enterprise-ready: [StackAI](https://stack-ai.com) - SOC 2 compliant

2. **Use Templates**: Most platforms offer pre-built templates for common use cases

3. **Connect Your Tools**: Link your email, CRM, calendar, and other daily tools

### For Developers

1. **Select a Framework**:
   ```bash
   # LangChain (most popular)
   pip install langchain langchain-openai

   # CrewAI (multi-agent)
   pip install crewai

   # LangGraph (stateful workflows)
   pip install langgraph
   ```

2. **Build Your First Agent**:
   ```python
   from langchain.agents import create_react_agent
   from langchain_openai import ChatOpenAI

   llm = ChatOpenAI(model="gpt-4")
   agent = create_react_agent(llm, tools, prompt)
   ```

3. **Deploy**: Use cloud platforms for production deployment with monitoring

---

## Top 50+ AI Agent Platforms

### Enterprise Platforms (10)

| Platform | Company | Best For | Pricing |
|----------|---------|----------|---------|
| [Agentforce](https://salesforce.com/agentforce) | Salesforce | CRM automation | Per conversation |
| [watsonx Orchestrate](https://ibm.com/watsonx) | IBM | Enterprise automation | Subscription |
| [Copilot Studio](https://microsoft.com/copilot-studio) | Microsoft | M365 integration | $200/year |
| [Vertex AI Agent Builder](https://cloud.google.com/vertex-ai) | Google | GCP workflows | Usage-based |
| [Bedrock Agents](https://aws.amazon.com/bedrock) | AWS | AWS infrastructure | Usage-based |
| [ServiceNow AI Agents](https://servicenow.com) | ServiceNow | IT service management | Enterprise |
| [Moveworks](https://moveworks.com) | Moveworks | Employee support | Enterprise |
| [Sana Agents](https://sanalabs.com) | Sana Labs | Industrial enterprise | Enterprise |
| [Adopt AI](https://adopt.ai) | Adopt AI | Enterprise orchestration | Enterprise |
| [Azure AI Foundry](https://azure.microsoft.com/ai) | Microsoft | Enterprise AI | Usage-based |

### Cloud Provider Services (6)

| Platform | Provider | Key Features | Integration |
|----------|----------|--------------|-------------|
| AWS Bedrock Agents | Amazon | Multi-model, AgentCore | Full AWS |
| AWS Strands Agents | Amazon | Lightweight SDK | AWS services |
| Vertex AI Agent Builder | Google | Gemini-powered | GCP |
| Azure AI Agent Service | Microsoft | OpenAI models | Azure |
| Google ADK | Google | Agent Development Kit | GCP |
| AWS Transform | Amazon | Enterprise modernization | AWS |

### No-Code Builders (15)

| Platform | Best For | Pricing | Integrations |
|----------|----------|---------|--------------|
| [Lindy](https://lindy.ai) | SMBs | $49/month | 3000+ |
| [Zapier Agents](https://zapier.com) | App automation | From $19.99/mo | 8000+ |
| [No Stairs Please MCP](https://nostairsplease.com/mcp) | Live music venue discovery & tour routing | Free | MCP |
| [Gumloop](https://gumloop.com) | Technical marketers | Free-$37/mo | MCP support |
| [StackAI](https://stack-ai.com) | Enterprise | Custom | Enterprise |
| [Relay.app](https://relay.app) | Workflow automation | Varies | Popular apps |
| [Flowise](https://flowiseai.com) | Developers | Free (OSS) | Customizable |
| [Dify](https://dify.ai) | Visual building | Free (OSS) | APIs |
| [n8n](https://n8n.io) | Technical teams | Free-$20/mo | 400+ |
| [GenFuse AI](https://genfuse.ai) | Automation | Varies | Multiple |
| [Relevance AI](https://relevanceai.com) | Data teams | Varies | APIs |
| [Make](https://make.com) | Visual workflows | From $9/mo | 1500+ |
| [Vellum AI](https://vellum.ai) | Enterprise AI | Enterprise | Full SDK |
| [Sendbird](https://sendbird.com) | Customer engagement | Enterprise | Omnichannel |
| [Retool AI](https://retool.com) | Internal tools | From $60/mo | Databases |
| [Activepieces](https://activepieces.com) | Open source | Free-paid | 100+ |

### Specialized Agents (12)

| Agent | Domain | Company | Pricing |
|-------|--------|---------|---------|
| [Devin AI](https://cognition.ai) | Software engineering | Cognition | From $20/mo |
| [Cognosys](https://cognosys.ai) | Knowledge work | Cognosys | Subscription |
| [OpenAI Operator](https://openai.com) | Browser automation | OpenAI | ChatGPT Plus |
| [Sierra](https://sierra.ai) | Customer experience | Sierra | Enterprise |
| [Moveworks](https://moveworks.com) | IT support | Moveworks | Enterprise |
| [Bland](https://bland.ai) | Voice agents | Bland AI | Usage-based |
| [Retell AI](https://retell.ai) | Voice agents | Retell | Usage-based |
| [Claude](https://anthropic.com) | Multi-domain | Anthropic | API-based |
| [Open Interpreter](https://openinterpreter.com) | Code execution | OSS | Free |
| [Cursor](https://cursor.sh) | AI IDE | Cursor | From $20/mo |
| [GitHub Copilot](https://github.com/features/copilot) | Code completion | GitHub | $10-19/mo |
| [Qodo](https://qodo.ai) | Enterprise coding | Qodo | From $30/mo |

### Developer Frameworks (12)

| Framework | Type | Stars | Best For |
|-----------|------|-------|----------|
| [LangChain](https://langchain.com) | OSS | 50K+ | General chains |
| [LangGraph](https://langchain.com/langgraph) | OSS | - | Stateful workflows |
| [CrewAI](https://crewai.com) | OSS | 40K+ | Multi-agent teams |
| [AutoGen](https://microsoft.github.io/autogen) | OSS | 30K+ | Conversations |
| [OpenAI Swarm](https://github.com/openai/swarm) | OSS | - | Lightweight agents |
| [Semantic Kernel](https://learn.microsoft.com/semantic-kernel) | OSS | - | Enterprise .NET |
| [Phidata](https://phidata.com) | OSS | - | Memory & tools |
| [Haystack](https://haystack.deepset.ai) | OSS | 15K+ | RAG pipelines |
| [Vellum](https://vellum.ai) | Commercial | - | Production AI |
| [Rivet](https://rivet.ironcladapp.com) | OSS | - | Visual GUI |
| [MetaGPT](https://github.com/geekan/MetaGPT) | OSS | 40K+ | Software teams |
| [AgentGPT](https://agentgpt.reworkd.ai) | OSS | - | Prototyping |

---

## Platform Comparison Matrix

| Platform | Type | Multi-Agent | Integration Depth | Ease of Use | Enterprise Ready | Pricing Model |
|----------|------|-------------|-------------------|-------------|------------------|---------------|
| Salesforce Agentforce | Enterprise | 4/5 | 5/5 | 3/5 | 5/5 | Per conversation |
| IBM watsonx | Enterprise | 3/5 | 5/5 | 3/5 | 5/5 | Subscription |
| Microsoft Copilot Studio | Enterprise | 3/5 | 4/5 | 4/5 | 4/5 | Subscription |
| AWS Bedrock | Cloud | 4/5 | 5/5 | 3/5 | 5/5 | Usage-based |
| Google Vertex AI | Cloud | 4/5 | 4/5 | 3/5 | 5/5 | Usage-based |
| Lindy | No-Code | 4/5 | 4/5 | 5/5 | 3/5 | Subscription |
| Zapier Agents | No-Code | 3/5 | 5/5 | 5/5 | 3/5 | Subscription |
| LangChain | Framework | 5/5 | 5/5 | 2/5 | 3/5 | Open source |
| CrewAI | Framework | 5/5 | 3/5 | 3/5 | 3/5 | Freemium |
| Devin AI | Specialized | 3/5 | 3/5 | 4/5 | 3/5 | Subscription |

---

## Choosing the Right Platform

### Decision Tree

```
Start
  |
  v
Are you a developer?
  |
  +-- Yes --> Do you need multi-agent coordination?
  |             |
  |             +-- Yes --> CrewAI, LangGraph, or AutoGen
  |             |
  |             +-- No --> LangChain or OpenAI API
  |
  +-- No --> Do you have technical resources?
              |
              +-- Yes --> StackAI, Gumloop, or n8n
              |
              +-- No --> Lindy, Zapier Agents, or Relay.app
```

### By Use Case

| Use Case | Recommended Platforms |
|----------|----------------------|
| Customer Support | Salesforce Agentforce, Zendesk AI, Intercom |
| Sales Automation | Lindy, HubSpot AI, Salesforce Einstein |
| Software Development | Devin AI, GitHub Copilot, Cursor |
| IT Operations | ServiceNow, Moveworks, IBM watsonx |
| Marketing | Zapier Agents, Make, Relevance AI |
| Data Analysis | Vertex AI, Bedrock, StackAI |
| Voice Assistants | Bland, Retell AI, VAPI |

### By Company Size

| Size | Budget | Recommended |
|------|--------|-------------|
| Startup (1-10) | < $500/mo | Lindy, Zapier, open-source |
| SMB (10-100) | $500-5K/mo | StackAI, n8n, Gumloop |
| Mid-Market (100-1000) | $5K-50K/mo | Bedrock, Vertex AI, Copilot Studio |
| Enterprise (1000+) | $50K+/mo | Agentforce, watsonx, Custom |

### By Technical Expertise

| Level | Platforms |
|-------|-----------|
| No-code | Lindy, Zapier, Relay.app |
| Low-code | Copilot Studio, StackAI, Flowise |
| Pro-code | LangChain, CrewAI, AutoGen |
| Full-stack | Custom + Cloud services |

---

## Market Statistics

### 2025 AI Agent Market Overview

- **Market Size**: $7.84 billion (2025) -> $52.62 billion (2030)
- **CAGR**: 46.3%
- **Adoption Rate**: 79% of organizations deploying AI agents
- **Expansion Plans**: 96% planning expansions in 2025

### Enterprise ROI Metrics

| Metric | Value |
|--------|-------|
| Average ROI | $3.70 return per $1 invested |
| Top performers | Up to $10 return per $1 |
| Microsoft Copilot reported ROI | 353% |
| Production AI use cases | 31% (doubled from 2024) |

### Framework Popularity (GitHub Stars)

| Framework | Stars | Growth |
|-----------|-------|--------|
| LangChain | 50,000+ | +200% YoY |
| CrewAI | 40,000+ | +500% YoY |
| AutoGen | 30,000+ | +300% YoY |
| MetaGPT | 40,000+ | +400% YoY |

### Enterprise Adoption

- **81%** of executives now leading AI adoption (up from 53%)
- **44%** identify infrastructure as primary obstacle
- **85%** of enterprises plan to adopt AI agents by end of 2025
- **Fortune 500**: ~50% using CrewAI for multi-agent workflows

---

## Documentation Index

| Document | Description |
|----------|-------------|
| [ENTERPRISE-PLATFORMS.md](ENTERPRISE-PLATFORMS.md) | Enterprise-grade AI agent platforms |
| [CLOUD-PLATFORMS.md](CLOUD-PLATFORMS.md) | Cloud provider agent services |
| [NO-CODE-BUILDERS.md](NO-CODE-BUILDERS.md) | No-code and low-code builders |
| [SPECIALIZED-AGENTS.md](SPECIALIZED-AGENTS.md) | Domain-specific AI agents |
| [AGENTIC-FRAMEWORKS.md](AGENTIC-FRAMEWORKS.md) | Developer frameworks |
| [COMPARISON-MATRIX.md](COMPARISON-MATRIX.md) | Detailed comparison tables |
| [RESOURCES.md](RESOURCES.md) | Learning materials and links |
| [CONTRIBUTING.md](CONTRIBUTING.md) | Contribution guidelines |

---

## Contributing

We welcome contributions! Please see our [Contributing Guide](CONTRIBUTING.md) for details.

### Quick Contribution

1. Fork the repository
2. Add your platform/tool following the existing format
3. Submit a pull request with clear description

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## Acknowledgments

Research and data compiled from:
- Gartner AI Agent Market Reports
- GitHub repository statistics
- Official platform documentation
- Community benchmarks and reviews

---

**Last Updated**: November 2025

**Maintained by**: The AI Agents Community

---

If this list helped you, please star it and share with others!
