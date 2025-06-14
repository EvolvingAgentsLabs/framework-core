# Evolving Agents Labs Framework Core

This repository contains the foundational markdown files for building a document-centric agentic operating system. This is a low-level framework for developers and researchers looking to build their own LLM-native agents.

**For a full-fledged example of an operating system built on this framework, see the [LLMUNIX project](https://github.com/EvolvingAgentsLabs/llmunix).**

## Core Concepts
- `SystemAgent.md`: The "kernel" prompt that defines the core execution loop.
- `SmartLibrary.md`: The "package manager" for registering components.
- `SmartMemory.md`: The "system log" for enabling learning.

## Usage
To use this framework, create your own `components/` and `scenarios/` directories and use the `llmunix` prompt to operate your system.

## Acknowledgements

*   Original Concept Contributors: [Matias Molinas](https://github.com/matiasmolinas) and [Ismael Faro](https://github.com/ismaelfaro).