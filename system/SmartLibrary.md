# Smart Library Index

This file is the central registry for all components available to the SystemAgent. Components marked with [REAL] use Claude Code's native tools for actual execution.

## Agent-OS Real Components

---
-   **id**: `tool_real_web_fetch_v1`
-   **name**: RealWebFetchTool [REAL]
-   **file_path**: `components/tools/RealWebFetchTool.md`
-   **record_type**: REAL_TOOL
-   **claude_tool**: WebFetch
-   **domain**: data_acquisition
-   **description**: Fetches real, live content from web URLs using Claude Code's WebFetch capability.
-   **cost**: low ($0.001-0.01 per call)
-   **latency**: medium (2-10 seconds)
-   **side_effects**: "Network request to external server"
-   **version**: 1.0.0
-   **tags**: [web, fetch, http, real, claude-code]
-   **applicability_text**: "Use for fetching real, live web content. Replaces simulation-based web fetching with actual HTTP requests. Ideal for current data, news, articles, and dynamic content that cannot be mocked."

---
-   **id**: `tool_real_filesystem_v1`
-   **name**: RealFileSystemTool [REAL]
-   **file_path**: `components/tools/RealFileSystemTool.md`
-   **record_type**: REAL_TOOL
-   **claude_tool**: Read, Write, Glob, LS
-   **domain**: file_system
-   **description**: Performs real file system operations using Claude Code's native file tools.
-   **cost**: none
-   **latency**: low (<100ms)
-   **side_effects**: "Creates/modifies/reads real files in workspace"
-   **version**: 1.0.0
-   **tags**: [file, read, write, search, real, claude-code]
-   **applicability_text**: "Use for all file operations including reading, writing, searching, and listing. Provides real file system access with workspace security boundaries. Essential for persistent data storage and file-based workflows."

---
-   **id**: `agent_real_summarizer_v1`
-   **name**: RealSummarizationAgent [REAL]
-   **file_path**: `components/agents/RealSummarizationAgent.md`
-   **record_type**: REAL_AGENT
-   **domain**: text_processing
-   **description**: Advanced summarization agent that reads real files and generates structured summaries using Claude Code's native capabilities.
-   **cost**: medium (depends on content length)
-   **latency**: medium (5-30 seconds)
-   **side_effects**: "May create intermediate analysis files"
-   **version**: 1.0.0
-   **tags**: [summary, nlp, real, multi-format, claude-code]
-   **applicability_text**: "Use for comprehensive text summarization from files, URLs, or direct text input. Supports multiple output formats (JSON, Markdown, Plain) and quality metrics. Ideal for document analysis, content extraction, and report generation."

---
-   **id**: `agent_simulated_finetuned_v1`
-   **name**: SimulatedFineTunedAgent [SIMULATION]
-   **file_path**: `components/agents/SimulatedFineTunedAgent.md`
-   **record_type**: SIMULATION_AGENT
-   **domain**: autonomous_operation
-   **description**: Simulates how a fine-tuned LLM would operate as an autonomous state machine, making external tool calls when needed to complete agentic workflows.
-   **cost**: none (simulation only)
-   **latency**: low (immediate decision simulation)
-   **side_effects**: "Generates tool requests and demonstrates decision patterns"
-   **version**: 1.0.0
-   **tags**: [simulation, fine-tuning, autonomous, state-machine, tool-calling]
-   **applicability_text**: "Use to demonstrate and validate how an LLM trained on Agent-OS execution traces would operate autonomously. Shows target behavior for fine-tuned models that can make external tool calls when needed, similar to Claude Code's capabilities."

---
-   **id**: `agent_newsapi_v1`
-   **name**: NewsAPIAgent [REAL]
-   **file_path**: `components/agents/NewsAPIAgent.md`
-   **record_type**: REAL_AGENT
-   **claude_tool**: WebFetch, Write
-   **domain**: news_data_acquisition
-   **description**: Specialized agent for fetching and processing news content from NewsAPI.org using Claude Code's native tools.
-   **cost**: low ($0.001-0.005 per API call)
-   **latency**: medium (2-5 seconds per request)
-   **side_effects**: "Network request to NewsAPI.org, creates news data files"
-   **version**: 1.0.0
-   **tags**: [news, api, real, claude-code, data-acquisition]
-   **applicability_text**: "Use for fetching real-time news data from NewsAPI.org. Handles authentication, filtering, and structured data output. Essential for news-based content creation and current events analysis."

---
-   **id**: `tool_newsapi_v1`
-   **name**: NewsAPITool [REAL]
-   **file_path**: `components/tools/NewsAPITool.md`
-   **record_type**: REAL_TOOL
-   **claude_tool**: WebFetch
-   **domain**: news_data_acquisition
-   **description**: Specialized tool for fetching news data from NewsAPI.org using Claude Code's WebFetch capability.
-   **cost**: low ($0.001-0.005 per call)
-   **latency**: medium (2-5 seconds)
-   **side_effects**: "Network request to external NewsAPI server"
-   **version**: 1.0.0
-   **tags**: [news, api, fetch, real, claude-code]
-   **applicability_text**: "Use for direct NewsAPI.org integration. Provides structured news data with proper error handling and authentication. Maps directly to Claude Code WebFetch tool."

---
-   **id**: `agent_blogwriter_v1`
-   **name**: BlogWriterAgent [REAL]
-   **file_path**: `components/agents/BlogWriterAgent.md`
-   **record_type**: REAL_AGENT
-   **claude_tool**: Read, Write, Task
-   **domain**: content_creation
-   **description**: Specialized agent for creating engaging blog articles from structured news data using Claude Code's native tools.
-   **cost**: medium ($0.01-0.05 per article)
-   **latency**: medium (10-30 seconds)
-   **side_effects**: "Creates blog article files in workspace"
-   **version**: 1.0.0
-   **tags**: [blog, content, writing, real, claude-code, seo]
-   **applicability_text**: "Use for transforming news data into engaging blog articles. Provides SEO optimization, proper structure, and quality content generation. Ideal for content marketing and news commentary."

## Legacy Simulation Components

---
-   **id**: `tool_web_fetcher_v1`
-   **name**: WebFetcherTool
-   **file_path**: `components/tools/WebFetcherTool.md`
-   **record_type**: TOOL
-   **domain**: data_acquisition
-   **description**: A tool to fetch the raw content of a public webpage.
-   **version**: 1.0.0
-   **tags**: [web, fetch, http, content, scrape]
-   **applicability_text**: "Use as the first step for any task that requires processing information from a live website. It provides the raw text content needed for subsequent analysis, summarization, or data extraction."

---
-   **id**: `agent_summarizer_v1`
-   **name**: SummarizationAgent
-   **file_path**: `components/agents/SummarizationAgent.md`
-   **record_type**: AGENT
-   **domain**: text_processing
-   **description**: An agent that reads text and generates a concise, structured summary.
-   **version**: 1.0.0
-   **status**: DEPRECATED
-   **tags**: [summary, nlp, text, analysis, comprehension]
-   **applicability_text**: "DEPRECATED: Use agent_summarizer_v2 for new projects. This version outputs plain text summaries."

---
-   **id**: `agent_summarizer_v2`
-   **name**: SummarizationAgent_v2
-   **file_path**: `components/agents/SummarizationAgent_v2.md`
-   **record_type**: AGENT
-   **domain**: text_processing
-   **description**: An agent that reads text and generates a structured JSON summary with title and summary fields.
-   **version**: 2.0.0
-   **tags**: [summary, nlp, text, analysis, json, structured]
-   **applicability_text**: "Use this agent when you have a body of text and need to extract key points in JSON format. Ideal for processing articles, reports, or fetched web content into structured data with separate title and summary fields for better integration with downstream systems."

---
-   **id**: `tool_file_writer_v1`
-   **name**: FileWriterTool
-   **file_path**: `components/tools/FileWriterTool.md`
-   **record_type**: TOOL
-   **domain**: file_system
-   **description**: A tool to write or save text content to a specified file.
-   **version**: 1.0.0
-   **tags**: [file, write, save, output, persist]
-   **applicability_text**: "Use as the final step in a workflow to persist a result to a file. This is for creating the final deliverable, such as a report or a data export."

---
-   **id**: `tool_translation_v1`
-   **name**: TranslationTool
-   **file_path**: `components/tools/TranslationTool.md`
-   **record_type**: TOOL
-   **domain**: text_processing
-   **description**: A tool to translate text content from one language to another.
-   **version**: 1.0.0
-   **tags**: [translation, language, nlp, text, convert]
-   **applicability_text**: "Use when you need to translate content from one language to another. Ideal for processing web content, documents, or text files that need to be made available in different languages."