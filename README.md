# Evolving Agents Labs - Framework Core

This repository contains the foundational markdown files for building **document-centric agentic systems**. This is a low-level framework for developers, researchers, and creators looking to build and experiment with a new class of AI agents that operate without traditional code.

---

## The Vision: Democratizing Agent Development

The evolution of AI agents has often been tied to complex coding libraries and infrastructure. After exploring the next steps in agentic systems, we asked a fundamental question: *What if we could lower the barrier to entry so dramatically that anyone could build, run, and evolve sophisticated AI agents?*

The answer lies in shifting the paradigm from **code-centric** to **document-centric**.

This framework was born from that idea. We realized that by using structured text documents (specifically markdown) as a "programming language" and a powerful Large Language Model (LLM) as the "runtime," we could create a system that is:

-   **Accessible:** If you can write a document, you can build an agent.
-   **Transparent:** The logic of every agent and tool is described in plain English.
-   **Infinitely Extensible:** New capabilities are added by writing new documents, not by compiling code.

**This is how LLM-OS was born**—as a laboratory for exploring what's possible when we treat the LLM as the CPU and markdown as its assembly language. Our mission is to democratize the development of intelligent agents, making it possible for anyone to automate and orchestrate complex tasks in any domain.

**For a full-fledged example of an operating system built on this framework, see the [LLMUNIX project](https://github.com/EvolvingAgentsLabs/llmunix).**

## Core Concepts: The OS Analogy

The framework is built around three core "system files" that function like the essential components of a traditional operating system:

-   **`SystemAgent.md` (The Kernel):** This is the master prompt that defines the core execution loop. It instructs the LLM on how to think, plan, execute tasks, and learn—acting as the central nervous system of the OS.

-   **`SmartLibrary.md` (The Package Manager):** This file is a human-readable registry of all available "software" (the agents and tools). The SystemAgent consults this library to discover the capabilities it needs to achieve a user's goal.

-   **`SmartMemory.md` (The System Log & Long-Term Memory):** This is an append-only log where the SystemAgent records the outcome of every task. By consulting its memory, the system learns from past successes and failures, enabling continuous improvement and more intelligent planning over time.

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
