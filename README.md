# AppleDocumentationForAIAgents

Local-first, AI-readable Apple Developer documentation with on-demand MCP deep lookup.

Build iOS, macOS, watchOS, tvOS, and visionOS apps using AI faster, cheaper, and with fewer hallucinations.

---

## Overview

Apple's official documentation is comprehensive, but it is not optimized for AI systems. It is heavily JavaScript-based, fragmented across many pages, and expensive to repeatedly fetch and parse.

When used with AI agents, this results in:

- High token usage
- Repeated scraping
- Slow responses
- Incorrect API usage
- Increased hallucinations

This repository provides a structured, offline-first knowledge base of Apple framework documentation in Markdown format, optimized for AI consumption, with optional live expansion through the sosumi.ai MCP server.

---

## Key Idea

Instead of forcing AI agents to constantly re-fetch Apple documentation, this project makes the core knowledge available locally and uses live MCP access only when deeper detail is required.

Primary access: Local Markdown  
Fallback access: MCP → Official Apple Docs

This hybrid model reduces cost, increases speed, and improves reliability.

---

## Architecture

```
AI Agent
↓
Local Markdown Documentation (this repository)
↓ (only if needed)
Sosumi.ai MCP Server
↓
Official Apple Developer Documentation
```

Most development tasks are handled using local files. MCP is used only for edge cases or deep references.

---

## What This Repository Contains

- 376+ Apple framework documentation files
- Converted to clean Markdown
- Optimized for AI parsing
- Preserved official Apple links
- Cross-framework references
- Multi-platform coverage

Supported platforms:

- iOS
- macOS
- watchOS
- tvOS
- visionOS

Coverage includes:

- SwiftUI, UIKit, AppKit
- AVFoundation, Metal, RealityKit
- Core ML, Vision, Create ML
- CloudKit, Core Data, SwiftData
- CryptoKit, Security, Authentication
- XCTest, Xcode Cloud, Developer Tools

---

## Why This Project Exists

This project was created after observing that:

- AI agents repeatedly download the same Apple documentation
- MCP and scraping tools waste tokens on stable information
- Most framework knowledge does not change frequently
- Apple's documentation format is not AI-friendly

Instead of treating documentation as a remote dependency, this project treats it as local infrastructure.

This improves:

- Development speed
- Cost efficiency
- Output accuracy
- Long-term stability

---

## Quick Start

### 1. Clone the Repository

```bash
git clone https://github.com/ayaan-there/AppleDocumentationForAIAgents.git
cd AppleDocumentationForAIAgents
```

---

### 2. Optional: Configure MCP for Deep Lookup

If your agent supports MCP, configure sosumi.ai:

```json
{
  "mcpServers": {
    "sosumi": {
      "command": "npx",
      "args": ["sosumi-mcp"],
      "url": "https://sosumi.ai/documentation"
    }
  }
}
```

This enables live access when local files are insufficient.

---

### 3. Configure Your AI Agent

Tell your agent to prioritize this repository:

```
Use AppleDocumentationForAIAgents as your primary
Apple documentation source.
Use MCP only if additional detail is required.
```

---

## Example Workflows

### Example 1: SwiftUI Camera App

Prompt:

```
Build a camera app using SwiftUI and AVFoundation.
Use local documentation first.
```

Agent behavior:

1. Reads SwiftUI.md
2. Reads AVFoundation.md
3. Designs architecture
4. Generates code
5. Uses MCP only for edge cases

Result: faster generation, fewer mistakes, lower cost.

---

### Example 2: Machine Learning Integration

Prompt:

```
Add real-time image classification using Core ML.
```

Agent reads:

* CoreML.md
* Vision.md
* AVFoundation.md

Builds correct inference pipeline without repeated scraping.

---

### Example 3: macOS Porting

Prompt:

```
Port this iOS app to macOS with native UI.
```

Agent uses:

* AppKit.md
* Mac Catalyst.md
* Foundation.md

Maps platform differences correctly.

---

## Benefits

### Token Efficiency

* No repeated scraping
* Smaller context windows
* Reduced API calls
* Lower operational cost

### Accuracy

* Based on official Apple sources
* Preserves exact APIs
* Reduces hallucination
* Stable references

### Speed

* Instant local access
* Faster planning
* Faster code generation
* No network latency

### Reliability

* Works offline
* Not dependent on live services
* Consistent context
* Reproducible results

---

## Supported Environments

This repository works well with:

* Cursor
* Claude MCP
* GPT-based agents
* AutoGPT / CrewAI
* Local LLMs
* Custom development agents

Any system that can read Markdown can use this project.

---

## Repository Structure

```
/
├── Apple-Documentation/
│   ├── SwiftUI.md
│   ├── AVFoundation.md
│   ├── CoreML.md
│   ├── UIKit.md
│   └── ...
└── README.md
```

Each framework file includes:

* Overview
* Core APIs
* Usage patterns
* Best practices
* Official references

---

## How It Was Built

1. Apple documentation links were collected
2. Content was converted using sosumi.ai
3. Files were normalized into Markdown
4. References were preserved
5. Structure was standardized
6. Content was validated for AI readability

The focus was on consistency, long-term usability, and agent compatibility.

---

## Updating and Maintenance

Planned improvements:

* Automated synchronization
* Version tracking
* Deprecation indicators
* Release tagging
* Change diffs

Community contributions are encouraged.

---

## Contributing

Contributions are welcome.

You can help by:

1. Improving formatting
2. Adding new frameworks
3. Fixing broken links
4. Adding usage examples
5. Creating benchmarks
6. Updating deprecated APIs

Open a pull request with a clear description.

---

## Legal Notice

This repository contains documentation derived from Apple Developer Documentation.

All original content belongs to Apple Inc.

This project is provided for educational and development purposes.

---

## Long-Term Vision

The goal is to build a shared, open, AI-native knowledge base for Apple development.

No scraping.
No wasted tokens.
No unnecessary API calls.
No hallucinations.

Just reliable infrastructure for AI-assisted software development.

---

## Author

Created by Ayaan.

If this project is useful to you, consider starring the repository.
