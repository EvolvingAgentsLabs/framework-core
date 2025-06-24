# Evolving Agents Labs - Framework Core

Core architectural patterns and building blocks for autonomous agent systems inspired by LLMunix's adaptive behavior management and sentient state architecture.

---

## Overview

Framework Core provides the foundational components and patterns discovered through LLMunix development, enabling the creation of intelligent agents that can adapt, learn, and evolve their behavior based on context and experience.

Building on LLMunix's breakthrough in **Adaptive Behavior Management**, this framework distills the key architectural insights into reusable patterns for creating truly intelligent autonomous agents.

## Key Innovations from LLMunix

### 🧠 Sentient State Architecture
Beyond traditional state management, Framework Core implements **behavioral constraints** that actively modify agent decision-making:
- **Dynamic Constraint Evolution**: Agent behavior adapts based on user sentiment and execution context
- **Memory-Driven Learning**: Historical patterns guide current decisions and optimization strategies
- **Modular State Components**: Atomic updates to specialized state files (plan.md, context.md, constraints.md)

### 🎯 Adaptive Behavior Management
System behavior dynamically evolves through real-time constraint modification:
- **User Sentiment Tracking**: Emotional state detection with adaptive response strategies
- **Priority Adaptation**: Execution focus shifts between speed, comprehensiveness, and cost efficiency
- **Persona Switching**: Communication style adapts to optimize user experience
- **Error Tolerance Management**: Risk acceptance adjusts based on task criticality

### 🔍 Intelligent Memory System
Structured experience database with pattern recognition and actionable insights:
- **YAML Frontmatter Querying**: Complex queries across historical executions
- **Behavioral Pattern Learning**: User preference evolution and constraint effectiveness tracking
- **Adaptive Recommendations**: Memory provides context-aware guidance for current tasks

**For the complete implementation of these concepts, see the [LLMunix project](https://github.com/EvolvingAgentsLabs/llmunix).**

## Architecture Patterns

### 1. Adaptive State Management Pattern

Based on LLMunix's sentient state architecture:

```
agent-workspace/
├── state/
│   ├── plan.md          # Execution roadmap and metadata
│   ├── context.md       # Accumulated knowledge base
│   ├── variables.json   # Structured data passing
│   ├── history.md       # Complete execution log
│   └── constraints.md   # Behavioral modifiers (the sentient layer)
└── outputs/            # Task results and artifacts
```

### 2. Behavioral Constraint Pattern

Dynamic behavior modification through evolving constraints:

```yaml
# constraints.md example
user_sentiment: "frustrated"          # Detected emotional state
priority: "speed_and_clarity"         # Execution focus
active_persona: "concise_assistant"   # Communication style
error_tolerance: "strict"             # Risk acceptance level
human_review_trigger_level: "low"     # Escalation threshold
```

### 3. Memory-Driven Decision Pattern

Intelligent consultation of historical experiences:

```yaml
# memory-entry.yml
---
timestamp: "2024-06-24T10:30:00Z"
task_type: "research_analysis"
user_sentiment_evolution: ["neutral", "impatient", "satisfied"]
constraint_adaptations:
  - trigger: "user_time_pressure"
    adaptation: "priority: comprehensiveness → speed_and_clarity"
success_metrics:
  completion_rate: 0.95
  user_satisfaction: 0.89
  cost_efficiency: 0.76
lessons_learned:
  - "Concise summaries preferred under time pressure"
  - "Web scraping requires graceful degradation strategies"
---
```

## How to Use This Framework

This repository provides the minimal "kernel" files. To build your own LLM-OS instance:

1.  **Clone this repository.**
2.  **Create your "software":** Add `components/agents/` and `components/tools/` directories and populate them with your own markdown-defined agents and tools.
3.  **Define your tasks:** Create a `scenarios/` directory with markdown files that describe high-level goals.
4.  **Boot your OS:** Use the `LLMUNIX` master prompt (found in the [LLMUNIX repository](https://github.com/EvolvingAgentsLabs/llmunix)) to instruct your chosen LLM to run your system.

---

## Future Vision & Roadmap

This framework is the foundation for a new kind of computing. Our vision is to build upon this core to create even more powerful and sophisticated autonomous systems. Our upcoming development will focus on these key areas:

🌱 **Autonomous Evolution & Self-Improvement**
-   The system will not only create new components but also analyze its own performance from `SmartMemory.md` to proactively evolve its existing agents and tools for better efficiency, accuracy, and cost-effectiveness.

🛡️ **Controlled Evolution (Firmware)**
-   We will introduce a `Firmware.md` component that defines a set of immutable rules, ethical constraints, and operational boundaries. This will guide the agent's evolution, ensuring that even as it improves itself, it adheres to core principles and safety protocols.

⚡ **Parallel Task Processing**
-   To overcome the single-threaded nature of current LLMs, we will develop a "Process Manager" agent and state management techniques that allow the SystemAgent to orchestrate and manage multiple, concurrent task executions, similar to multitasking in a modern OS.

🔌 **Multi-LLM Engine Support**
-   The framework will be enhanced to be truly LLM-agnostic. A new layer will allow the `SystemAgent` to dynamically choose the best LLM for a specific task (e.g., a creative model for content generation, a logic-focused model for planning) and manage interactions across different AI engines.

🌐 **Distributed Environments**
-   We aim to extend the OS concept to distributed systems. This will enable multiple LLMUNIX instances to communicate, share components from their libraries, and collaborate on goals that a single agent could not accomplish alone.

🖥️ **Intuitive User Interface (UI/UX)**
-   ...?

We believe these next steps will push the boundaries of what's possible with document-centric AI and create a truly adaptive and intelligent operating system.

## Acknowledgements

-   **Original Concept Contributors:** [Matias Molinas](https://github.com/matiasmolinas) and [Ismael Faro](https://github.com/ismaelfaro).
