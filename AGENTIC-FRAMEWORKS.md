# Agentic AI Frameworks

> Developer frameworks for building custom AI agents in 2025.

## Table of Contents

- [Overview](#overview)
- [Framework Comparison](#framework-comparison)
- [LangChain & LangGraph](#langchain--langgraph)
- [CrewAI](#crewai)
- [AutoGen](#autogen)
- [OpenAI Swarm](#openai-swarm)
- [Other Frameworks](#other-frameworks)
- [Choosing a Framework](#choosing-a-framework)

---

## Overview

Agentic AI frameworks provide developers with tools to build custom AI agents with specific architectures, memory systems, and orchestration patterns.

### Why Use a Framework?

- **Don't reinvent**: Proven patterns and abstractions
- **Community**: Active development and support
- **Integrations**: Pre-built tool connections
- **Best practices**: Established design patterns

### Framework Landscape 2025

| Category | Frameworks |
|----------|------------|
| General Purpose | LangChain, Haystack |
| Multi-Agent | CrewAI, AutoGen, LangGraph |
| Lightweight | OpenAI Swarm, Phidata |
| Enterprise | Semantic Kernel |
| Visual | Rivet, Langflow |

---

## Framework Comparison

### Quick Comparison

| Framework | Stars | Best For | Learning Curve | Multi-Agent |
|-----------|-------|----------|----------------|-------------|
| LangChain | 50K+ | General chains | Medium | Yes |
| LangGraph | - | Stateful workflows | High | Yes |
| CrewAI | 40K+ | Role-based teams | Low | Yes |
| AutoGen | 30K+ | Conversations | Medium | Yes |
| Swarm | - | Lightweight | Low | Yes |
| Semantic Kernel | - | Enterprise .NET | High | Yes |

### Architecture Philosophy

| Framework | Approach | Key Pattern |
|-----------|----------|-------------|
| LangChain | Chains & LCEL | Composable pipelines |
| LangGraph | Graphs | State machines |
| CrewAI | Crews | Role-based teams |
| AutoGen | Conversations | Message passing |
| Swarm | Handoffs | Agent transfers |

---

## LangChain & LangGraph

### LangChain

**Repository**: [langchain-ai/langchain](https://github.com/langchain-ai/langchain)
**Stars**: 50,000+
**Language**: Python, JavaScript

#### Overview

LangChain is the industry-standard framework for building LLM-powered applications. It provides abstractions for chains, agents, memory, and tools.

#### Key Features

```yaml
Core Components:
  - Models: LLM wrappers for all providers
  - Prompts: Templates and management
  - Memory: Conversation state
  - Chains: Sequential operations
  - Agents: Tool-using LLMs
  - Tools: Pre-built integrations
  - Retrievers: RAG components
```

#### Architecture

```python
from langchain.agents import create_react_agent
from langchain_openai import ChatOpenAI
from langchain.tools import tool

@tool
def search_database(query: str) -> str:
    """Search the product database"""
    return results

llm = ChatOpenAI(model="gpt-4")
agent = create_react_agent(llm, [search_database], prompt)
```

#### Pros

- Largest ecosystem and community
- Comprehensive documentation
- Most integrations (100+)
- Active development
- Production-ready

#### Cons

- Can be complex for simple use cases
- Frequent breaking changes
- Abstraction overhead
- Learning curve

#### Best For

- General LLM applications
- RAG systems
- Quick prototypes
- Teams already using LangChain

---

### LangGraph

**Repository**: [langchain-ai/langgraph](https://github.com/langchain-ai/langgraph)
**Part of**: LangChain ecosystem

#### Overview

LangGraph extends LangChain with graph-based orchestration for stateful, multi-agent applications. It provides explicit control over agent state machines.

#### Key Features

```yaml
Core Concepts:
  - Nodes: Agent functions or LLM calls
  - Edges: Transitions between nodes
  - State: Shared graph state
  - Conditional edges: Branching logic
  - Cycles: Loops and iterations
  - Persistence: State checkpointing
```

#### Architecture

```python
from langgraph.graph import StateGraph, END
from typing import TypedDict

class AgentState(TypedDict):
    messages: list
    next_step: str

graph = StateGraph(AgentState)

graph.add_node("research", research_agent)
graph.add_node("write", writing_agent)
graph.add_node("review", review_agent)

graph.add_edge("research", "write")
graph.add_conditional_edges(
    "write",
    should_review,
    {"review": "review", "end": END}
)
graph.add_edge("review", "write")

app = graph.compile()
```

#### New Features (2025)

- **LangGraph Supervisor**: Hierarchical multi-agent systems
- **useStream**: React integration
- **Interrupt**: Human-in-the-loop
- **Command**: Edgeless graphs

#### Pros

- Explicit state control
- Visual debugging
- Complex workflows
- LangChain integration
- Persistence/checkpointing

#### Cons

- Higher learning curve
- More verbose than alternatives
- Requires graph thinking
- LangChain coupling

#### Best For

- Complex, stateful workflows
- Multi-agent orchestration
- Workflows needing human oversight
- Production systems

---

## CrewAI

**Repository**: [joaomdmoura/crewAI](https://github.com/joaomdmoura/crewAI)
**Stars**: 40,000+
**Language**: Python

### Overview

CrewAI is a framework for building collaborative multi-agent systems inspired by real-world team dynamics. Agents have roles, goals, and work together as a "crew."

### Key Concepts

```yaml
Core Components:
  - Agent: Role-based AI worker
  - Task: Specific work item
  - Crew: Team of agents
  - Tools: Agent capabilities
  - Process: Execution strategy
```

### Architecture

```python
from crewai import Agent, Task, Crew, Process

# Define agents
researcher = Agent(
    role='Senior Research Analyst',
    goal='Find and analyze market trends',
    backstory='Expert in market research...',
    tools=[search_tool, analysis_tool]
)

writer = Agent(
    role='Content Writer',
    goal='Create engaging reports',
    backstory='Experienced technical writer...'
)

# Define tasks
research_task = Task(
    description='Research AI market trends for 2025',
    agent=researcher,
    expected_output='Detailed market analysis'
)

write_task = Task(
    description='Write report based on research',
    agent=writer,
    expected_output='Comprehensive report'
)

# Create crew
crew = Crew(
    agents=[researcher, writer],
    tasks=[research_task, write_task],
    process=Process.sequential
)

result = crew.kickoff()
```

### Pros

- Intuitive role-based design
- Quick to get started
- Good documentation
- Active community
- Snowflake integration

### Cons

- Less control than LangGraph
- Limited advanced orchestration
- Smaller integration library
- Growing pains from rapid growth

### Enterprise Adoption

- **~50% of Fortune 500** using CrewAI
- Integrated with IBM watsonx
- Growing enterprise features

### Best For

- Role-based workflows
- Content generation pipelines
- Research and analysis
- Teams new to multi-agent

---

## AutoGen

**Repository**: [microsoft/autogen](https://github.com/microsoft/autogen)
**Stars**: 30,000+
**Company**: Microsoft

### Overview

AutoGen is Microsoft's framework for building multi-agent conversational systems. Agents communicate through natural language exchanges.

### Key Concepts

```yaml
Core Components:
  - ConversableAgent: Base agent class
  - AssistantAgent: LLM-powered agent
  - UserProxyAgent: Human or automated proxy
  - GroupChat: Multi-agent conversations
  - GroupChatManager: Orchestrates discussions
```

### Architecture

```python
from autogen import AssistantAgent, UserProxyAgent, GroupChat, GroupChatManager

# Create agents
coder = AssistantAgent(
    name="Coder",
    system_message="You are a Python developer...",
    llm_config=llm_config
)

reviewer = AssistantAgent(
    name="Reviewer",
    system_message="You review code for quality...",
    llm_config=llm_config
)

user = UserProxyAgent(
    name="User",
    human_input_mode="NEVER",
    code_execution_config={"work_dir": "coding"}
)

# Create group chat
groupchat = GroupChat(
    agents=[user, coder, reviewer],
    messages=[],
    max_round=10
)

manager = GroupChatManager(
    groupchat=groupchat,
    llm_config=llm_config
)

# Start conversation
user.initiate_chat(manager, message="Create a web scraper")
```

### Pros

- Natural conversation flow
- Human-in-the-loop built-in
- Code execution support
- Microsoft backing
- Async support

### Cons

- More complex setup
- Build many integrations yourself
- Less structured than CrewAI
- Conversation can be verbose

### Best For

- Conversational agents
- Research and exploration
- Human-AI collaboration
- Microsoft ecosystem

---

## OpenAI Swarm

**Repository**: [openai/swarm](https://github.com/openai/swarm)
**Company**: OpenAI

### Overview

Swarm is OpenAI's lightweight, experimental framework for multi-agent orchestration. It focuses on agent handoffs and minimal complexity.

### Key Concepts

```yaml
Core Components:
  - Agent: Has instructions and tools
  - Handoff: Transfer to another agent
  - Context: Shared variables
  - Run: Execution loop
```

### Architecture

```python
from swarm import Swarm, Agent

client = Swarm()

def transfer_to_sales():
    return sales_agent

support_agent = Agent(
    name="Support Agent",
    instructions="Help with product questions. Transfer to sales for purchases.",
    functions=[transfer_to_sales]
)

sales_agent = Agent(
    name="Sales Agent",
    instructions="Handle purchases and pricing questions."
)

response = client.run(
    agent=support_agent,
    messages=[{"role": "user", "content": "I want to buy a laptop"}]
)
```

### Pros

- Very simple API
- Easy to understand
- OpenAI native
- Lightweight
- Good for learning

### Cons

- Experimental/educational
- Limited features
- No persistence
- Basic orchestration

### Best For

- Learning multi-agent patterns
- Simple handoff workflows
- Prototyping
- OpenAI-focused projects

---

## Other Frameworks

### Semantic Kernel

**Company**: Microsoft
**Language**: .NET, Python, Java

Enterprise SDK for building AI applications with LLMs.

```csharp
var kernel = Kernel.CreateBuilder()
    .AddAzureOpenAIChatCompletion(
        deploymentName: "gpt-4",
        endpoint: "...",
        apiKey: "..."
    )
    .Build();

var agent = new ChatCompletionAgent
{
    Kernel = kernel,
    Instructions = "You are a helpful assistant."
};
```

**Best For**: Enterprise .NET applications

---

### Phidata

**Repository**: [phidatahq/phidata](https://github.com/phidatahq/phidata)

Toolkit for building AI applications with memory, tools, and reasoning.

```python
from phi.agent import Agent
from phi.model.openai import OpenAIChat
from phi.tools.duckduckgo import DuckDuckGo

agent = Agent(
    model=OpenAIChat(id="gpt-4"),
    tools=[DuckDuckGo()],
    show_tool_calls=True
)

agent.print_response("Search for AI agent news")
```

**Best For**: Quick agent building with memory

---

### Haystack

**Repository**: [deepset-ai/haystack](https://github.com/deepset-ai/haystack)
**Stars**: 15,000+

Framework for building RAG and multimodal AI applications.

**Best For**: RAG pipelines, document processing

---

### MetaGPT

**Repository**: [geekan/MetaGPT](https://github.com/geekan/MetaGPT)
**Stars**: 40,000+

Multi-agent framework for software development simulation.

**Best For**: Simulating software teams

---

### Rivet

**Repository**: [Ironclad/rivet](https://github.com/Ironclad/rivet)

Visual, drag-and-drop GUI for building AI agents.

**Best For**: Visual workflow design

---

### Langflow

**Company**: DataStax

Visual framework for building RAG and multi-agent apps.

**Best For**: No-code agent building

---

## Choosing a Framework

### Decision Matrix

| Need | Recommendation |
|------|----------------|
| Getting started | CrewAI |
| Maximum control | LangGraph |
| Conversational | AutoGen |
| Lightweight | OpenAI Swarm |
| Enterprise .NET | Semantic Kernel |
| Visual building | Rivet, Langflow |
| RAG focus | Haystack |

### By Experience Level

| Level | Framework |
|-------|-----------|
| Beginner | CrewAI, Swarm |
| Intermediate | LangChain |
| Advanced | LangGraph |
| Enterprise | Semantic Kernel |

### By Use Case

| Use Case | Framework | Why |
|----------|-----------|-----|
| Content generation | CrewAI | Natural role assignment |
| Complex workflows | LangGraph | State machine control |
| Coding assistants | AutoGen | Code execution |
| Simple routing | Swarm | Easy handoffs |
| Enterprise apps | Semantic Kernel | .NET integration |

### By Team Size

| Size | Recommendation |
|------|----------------|
| Solo developer | Swarm, Phidata |
| Small team | CrewAI, LangChain |
| Large team | LangGraph, Semantic Kernel |
| Enterprise | Semantic Kernel, LangGraph |

---

## Best Practices

### General

1. **Start simple**: Use the least complex framework
2. **Understand patterns**: Learn agent design patterns
3. **Test extensively**: Agents are non-deterministic
4. **Monitor costs**: LLM calls add up
5. **Version prompts**: Track prompt changes

### Multi-Agent Specific

1. **Define clear roles**: Avoid overlap
2. **Limit agents**: More isn't better
3. **Plan communication**: Explicit protocols
4. **Handle failures**: Agents make mistakes
5. **Log everything**: Debug needs visibility

### Production

1. **Use async**: Don't block
2. **Implement timeouts**: Agents can hang
3. **Cache results**: Reduce API calls
4. **Rate limit**: Stay within quotas
5. **Monitor metrics**: Track performance

---

## Resources

### Documentation

- [LangChain Docs](https://python.langchain.com)
- [LangGraph Docs](https://langchain-ai.github.io/langgraph)
- [CrewAI Docs](https://docs.crewai.com)
- [AutoGen Docs](https://microsoft.github.io/autogen)
- [Semantic Kernel](https://learn.microsoft.com/semantic-kernel)

### Tutorials

- [LangChain Cookbook](https://github.com/langchain-ai/langchain/tree/master/cookbook)
- [CrewAI Examples](https://github.com/joaomdmoura/crewAI-examples)
- [AutoGen Notebooks](https://github.com/microsoft/autogen/tree/main/notebook)

### Community

- [LangChain Discord](https://discord.gg/langchain)
- [r/LangChain](https://reddit.com/r/langchain)
- [AI Engineers Discord](https://discord.gg/ai-engineers)

---

**Last Updated**: November 2025
