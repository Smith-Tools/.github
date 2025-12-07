# Smith Tools

**AI-powered Swift development ecosystem for modern teams that ship exceptional code**

Smith Tools is a comprehensive suite of professional-grade utilities that combines intelligent architectural validation, advanced build optimization, and AI-driven knowledge systems to help Swift developers maintain code quality throughout the development lifecycle.

---

## ✨ Features

- 🤖 **AI-Powered Knowledge** - Maxwell v4.0 with 122+ architectural patterns and sub-millisecond search
- 🏗️ **Progressive Intelligence** - Multi-level architectural validation with confidence scoring
- 🚀 **Context-Efficient Analysis** - 43-95% reduction in build output through intelligent parsing
- 📚 **Apple Documentation Integration** - Live Apple docs + 3,216 WWDC sessions with encrypted local storage
- 🔍 **Smart Project Detection** - Automatic analysis across Swift Packages, Xcode projects, and workspaces
- 🛠️ **Unified Developer Experience** - Single CLI interface orchestrating the entire ecosystem
- 🎯 **Agent-Native Skills** - Claude Code skills with mandatory tool usage patterns and comprehensive decision trees

---

## 🚀 Quick Start

```bash
# Install the complete Smith Tools ecosystem
bash install-smith-tools-unified.sh

# Get architectural guidance from Maxwell
@maxwell "How should I structure TCA reducers for navigation?"

# Validate your project with progressive intelligence
smith validate --tca

# Analyze build performance
xcodebuild build -workspace App.xcworkspace -scheme App 2>&1 | smith xcode
```

---

## 🏗️ Architecture Overview

### **Clean Separation of Concerns**

```
┌─────────────────────────────────────────────────────────────────┐
│                        SMITH TOOLS ECOSYSTEM                     │
├─────────────────────────────────────────────────────────────────┤
│                                                                  │
│  ┌─────────────┐              ┌─────────────┐                  │
│  │  @smith     │              │  @maxwell   │                  │
│  │  (agent)    │              │  (agent)    │                  │
│  │ Objective   │  Task(maxwell)│  Proactive  │                  │
│  │ enforcement │◄────────────►│  synthesis  │                  │
│  └─────────────┘              └──────┬──────┘                  │
│                                     │                           │
│                                     │ uses Maxwell (skill)      │
│                                     ▼                           │
│                             ┌─────────────┐                    │
│                             │ maxwell     │                    │
│                             │ (skill)     │                    │
│                             └─────────────┘                    │
│         │                                                        │
│         │ smith-skill (auto-trigger)                            │
│         ▼                                                        │
│  ┌─────────────────────────────────────┐                      │
│  │      smith-CLI (unified interface)   │                      │
│  │  ├─ smith validate → smith-validation│                      │
│  │  ├─ smith xcode    → smith-diagnostics│                     │
│  │  ├─ smith dependencies → smith-diagnostics │                      │
│  │  └─ smith swift    → smith-parser   │                      │
│  └────────────────┬──────────────────┘                        │
│                   │                                              │
│  ┌────────────────▼──────────────────────────────────┐        │
│  │              smith-foundation (shared)             │        │
│  │  SmithProgress │ SmithErrorHandling │ SmithOutputFormatter │
│  └───────────────────────────────────────────────────┘        │
│                                                                  │
│  Auto-Trigger Skills:                                           │
│  ┌──────────┐ ┌──────────┐ ┌──────────┐                       │
│  │ @sosumi  │ │ @scully  │ │ @maxwell │                       │
│  │ Apple    │ │ 3rd party│ │ Patterns │                       │
│  │ docs     │ │ docs     │ │ & TCA    │                       │
│  └──────────┘ └──────────┘ └──────────┘                       │
│                                                                  │
└─────────────────────────────────────────────────────────────────┘
```

### **Ecosystem Components**

#### **Skills (Auto-trigger or user-invoked)** - 4 Total
- **smith-skill** - Auto-triggers on build commands, provides routing guidance
- **maxwell-skill** - Knowledge base with extensive patterns
- **sosumi** - Apple documentation and WWDC sessions
- **scully** - 3rd party package documentation

#### **Agents (Called via @name)** - 2 Total
- **@smith** - Objective enforcement, validation, diagnostics
- **@maxwell** - Proactive synthesis, uses maxwell (skill) for extensive patterns

#### **Shared Foundation** - 1 Package (3 modules)
- **smith-foundation** - Shared infrastructure used by all CLI tools
  - SmithProgress - Spinners, progress bars, TTY detection
  - SmithErrorHandling - Structured errors with actionable guidance
  - SmithOutputFormatter - Intelligent terminal output formatting

#### **Pure CLI Tools (Used by smith-CLI)** - 4 Total
- **smith-validation** - TCA architecture validation (independent deps)
- **smith-tca-trace** - TCA performance profiling (independent)
- **smith-diagnostics** - Shared diagnostics library (uses foundation)
- **smith-parser** - Shared parsing library (uses foundation)

### **Workflow Example**

```
User: "@smith validate my TCA reducer"

@smith (agent)
  ├─ Runs: smith validate --tca
  │   └─ Uses: smith-validation CLI
  ├─ Calls: Task(maxwell, "TCA reducer patterns")
  │   └─ @maxwell (agent) uses maxwell (skill)
  │       └─ Searches knowledge base (122+ patterns)
  │       └─ Provides proactive synthesis
  └─ Reports: Validation results + Maxwell's guidance

Natural auto-trigger:
  ├─ User asks about Apple APIs → @sosumi auto-triggers
  ├─ User asks about packages → @scully auto-triggers
  └─ User asks about patterns → @maxwell skill auto-triggers
```

---

## 📦 Ecosystem

Smith Tools provides a comprehensive suite organized around **clean separation of concerns**:

### 🧠 Knowledge & Intelligence

#### **Maxwell** - AI Knowledge System (Agent & Skill)
- **v4.0 File-Based Architecture**: 50+ personal discoveries with Grep/Read/Glob tools
- **No Database Required**: Direct markdown file access in ~/.claude/resources/discoveries/
- **Git-Friendly**: Human-readable files, easy to version control and maintain
- **Auto-Activates**: Automatically searches discoveries for Swift/TCA questions

#### **Sosumi** - Apple Documentation & WWDC Intelligence (Skill)
- **Live Apple Documentation**: Real-time search via undocumented Apple JSON endpoints
- **Encrypted WWDC Database**: 3,216 sessions (2014-2025) with AES-256-GCM encryption
- **Dual Rendering Modes**: User mode (summaries) vs Agent mode (full transcripts)
- **Local Search Performance**: 850MB encrypted bundle with instant access

#### **Scully** - 3rd Party Package Documentation (Skill)
- **Package Documentation**: Fetch and search documentation for any Swift package
- **Multi-Source Support**: GitHub, GitLab, and other sources
- **Local Caching**: Cache package docs for offline access
- **Version-Aware**: Specific version documentation retrieval
- **Workflow Integration**: Pipes from `smith dependencies` for batched analysis

### 🔍 Validation & Analysis

#### **smith-validation** - Progressive Intelligence Engine (Pure CLI Tool)
- **Three Analysis Levels**: Critical, Standard, and Comprehensive with progressive enhancement
- **AI-Optimized Output**: JSON format designed for Claude agent integration
- **Enhanced TCA Rules**: Missing error handling, monolithic feature detection, and architectural compliance
- **Used by**: `smith validate --tca`

#### **smith-tca-trace** - TCA Performance Profiling (Pure CLI Tool)
- **Performance Analysis**: Deep dive into TCA reducer performance
- **Memory Tracking**: Monitor memory usage and leaks
- **Action Timing**: Measure action processing latency
- **Used by**: `smith trace`

### ⚡ Build Performance Tools

#### **smith-diagnostics** - Shared Diagnostics Library (Pure CLI Tool)
- **Smart Project Detection**: Automatic identification of project type and structure
- **Build Output Parsing**: Intelligent parsing with context reduction
- **Hang Detection**: Real-time monitoring for build hangs
- **Used by**: `smith xcode`, `smith analyze`

#### **smith-parser** - Shared Parsing Library (Pure CLI Tool)
- **Package Analysis**: Parse Swift Package manifests
- **Dependency Graph**: Build dependency relationships
- **Structure Analysis**: Project structure and organization
- **Used by**: `smith spm`, `smith swift`

### 🎯 Orchestration

#### **Smith CLI** - Ecosystem Orchestrator
- **Unified Interface**: Single entry point for all tools
- **Smart Routing**: Automatically detects project type and routes to appropriate tools
- **Agent Integration**: Designed for Claude Code agent workflows
- **Commands**: `smith validate`, `smith xcode`, `smith dependencies`, `smith swift`, `smith analyze`

---

## 🎯 Claude Code Integration & Agent-Native Skills

Smith Tools now includes **Claude Code skills with mandatory tool usage patterns** that make agents automatically use the right tools by default:

### ✨ What's New in Skills v3.0

- **Mandatory Usage Patterns** - Each skill explicitly instructs agents to always pipe output through the analysis tool
- **Comprehensive Decision Trees** - Two new knowledge files guide agents through all tool selection scenarios:
  - **BUILD-COMMAND-DEFAULTS.md** - Command templates and decision logic for build systems
  - **TOOL-SELECTION-DECISION-TREE.md** - Master decision trees covering all 5 Smith tool domains

### 🔧 How It Works

Before v3.0, agents would run bare commands:
```bash
# ❌ Old behavior (not using tools)
xcodebuild build -workspace App.xcworkspace -scheme App -quiet
```

After v3.0, agents use the proper patterns:
```bash
# ✅ New behavior (with mandatory patterns)
xcodebuild build -workspace App.xcworkspace -scheme App 2>&1 | smith xcode
```

### 📚 Tool Coverage

The decision trees cover all Smith tool domains:
1. **Build Analysis** (smith xcode, smith swift) - Xcode and Swift build output
2. **Dependency Management** (smith dependencies) - Unified dependency analysis
3. **Architecture Validation** (smith validate) - TCA patterns and code quality
4. **Performance Analysis** (smith trace) - TCA performance profiling
5. **Documentation Search** (sosumi, scully) - Apple and 3rd party documentation

### 💡 Installation

Install updated skills via:
```bash
bash install-smith-tools-unified.sh
```

This installs all 4 skills and all CLI tools automatically.

---

## 🎯 What Makes Smith Tools Different

### 🤖 AI-First Development
- **Maxwell Knowledge System**: 122+ architectural patterns with sub-millisecond SQLite search
- **Progressive Intelligence**: Three-level analysis (Critical → Standard → Comprehensive)
- **Claude Agent Integration**: AI-optimized JSON outputs for seamless agent workflows
- **Natural Language Interface**: Ask architectural questions in plain English

### ⚡ Context-Efficient Performance
- **43-95% Context Reduction**: Intelligent parsing eliminates log noise
- **Sub-millisecond Search**: FTS5 with BM25 ranking across all knowledge domains
- **Encrypted Local Storage**: 850MB WWDC database with AES-256-GCM encryption
- **Smart Caching**: Optimized for repeated analysis and documentation access

### 🏗️ Modern Swift Architecture
- **TCA-First Validation**: Built-in compliance with The Composable Architecture patterns
- **Platform-Specific Intelligence**: Specialized knowledge for iOS, macOS, visionOS, and SharePlay
- **Progressive Enhancement**: Start with Critical analysis, expand as needed
- **Real-time Build Monitoring**: Hang detection and bottleneck identification

---

## 🛠️ Installation

### Unified Installation Script (Recommended)
```bash
# Install the complete Smith Tools ecosystem
bash install-smith-tools-unified.sh

# This installs:
# - All 4 skills (smith, maxwell, sosumi, scully)
# - All CLI tools (smith-validation, smith-tca-trace, etc.)
# - Maxwell personal discoveries (50+ case studies and patterns)
# - Both agents (@smith, @maxwell)
```

### Individual Components

#### Skills (for Claude Code)
```bash
# Install individual skills to ~/.claude/skills/
cp -r Smith/skills/smith ~/.claude/skills/smith
cp -r Maxwell/skills/maxwell ~/.claude/skills/maxwell
cp -r sosumi/Skill ~/.claude/skills/sosumi
cp -r scully/Skill ~/.claude/skills/scully
```

#### CLI Tools (for command line)
```bash
# Build and install CLI tools
cd Smith/cli && swift build -c release
cp .build/release/smith /usr/local/bin/

cd smith-validation && swift build -c release
cp .build/release/smith-validation /usr/local/bin/

cd smith-tca-trace && swift build -c release
cp .build/release/smith-tca-trace /usr/local/bin/
```

### Swift Package Manager
```swift
dependencies: [
    .package(url: "https://github.com/Smith-Tools/smith-validation", from: "1.0.6"),
    .package(url: "https://github.com/Smith-Tools/smith-diagnostics", from: "1.0.0"),
]
```

---

## 📚 Documentation & Resources

### Core Documentation
- **[Maxwell Knowledge Base](https://github.com/Smith-Tools/Maxwell-data-private)** - Extensive architectural patterns
- **[Smith CLI](https://github.com/Smith-Tools/Smith)** - Ecosystem orchestrator guide
- **[Smith Validation](https://github.com/Smith-Tools/smith-validation)** - Progressive intelligence engine

### Skills
- **[sosumi](https://github.com/Smith-Tools/sosumi)** - Apple documentation & WWDC search
- **[scully](https://github.com/Smith-Tools/scully)** - 3rd party package documentation

### CLI Tools
- **[smith-validation](https://github.com/Smith-Tools/smith-validation)** - TCA architecture validation
- **[smith-tca-trace](https://github.com/Smith-Tools/smith-tca-trace)** - TCA performance profiling

### Distribution
- **[Homebrew Tap](https://github.com/Smith-Tools/homebrew-smith)** - Installation and updates

---

## 🎯 Use Cases & Workflows

### 🏗️ Architectural Decision Making
```bash
# Get TCA patterns for complex navigation
maxwell "How should I handle deep linking with multiple TCA features?"

# Validate architectural compliance
smith-validation analyze --level comprehensive ./MyApp

# Review Apple guidelines for SharePlay integration
sosumi "GroupActivities lifecycle management"
```

### 🚀 Performance Optimization
```bash
# Identify build bottlenecks
xcodebuild build -workspace App.xcworkspace 2>&1 | smith xcode

# Analyze package dependencies
smith dependencies ./MyPackage

# Monitor build hangs in real-time
smith swift monitor --hang-detection
```

### 📚 Knowledge Discovery
```bash
# Search WWDC sessions for visionOS patterns
sosumi wwdc "spatial personas" --sessions 2024,2025

# Find Swift concurrency patterns
maxwell "Actor isolation with @MainActor"

# Get Apple documentation updates
sosumi "SwiftUI @Observable" --live-docs
```

---

## 🔄 Recent Developments

### 🆕 New in v4.0
- **Maxwell Knowledge System**: SQLite-powered database with 122+ architectural patterns
- **Progressive Intelligence**: Three-level validation analysis (Critical → Standard → Comprehensive)
- **Encrypted WWDC Archive**: 3,216 sessions with AES-256-GCM encryption
- **AI-Optimized Workflows**: JSON outputs designed for Claude agent integration

### ⚡ Performance Improvements
- **43-95% Context Reduction**: Intelligent parsing eliminates build log noise
- **Sub-millisecond Search**: FTS5 with BM25 ranking across knowledge domains
- **Real-time Build Monitoring**: Hang detection and bottleneck identification
- **Smart Caching**: Optimized for repeated analysis workflows

### 🏗️ Architecture Evolution
- **Multi-Skill System**: Specialized Maxwell skills for TCA, visionOS, SharePlay, and Swift patterns
- **Progressive Enhancement**: Start with Critical analysis, expand as project complexity grows
- **Platform-Specific Intelligence**: Specialized knowledge for all Apple platforms
- **Source-Controlled Knowledge**: Git-tracked patterns with automated deployment

---

## 🤝 Contributing

Smith Tools welcomes contributions! We're actively developing:

- **Knowledge Base Expansion**: Add architectural patterns to Maxwell-data-private
- **Validation Rules**: Enhance TCA and architectural compliance checking
- **Build Tool Integration**: Extend context-efficient parsing to new scenarios
- **Documentation**: Improve coverage of Apple platform patterns

**Development Guidelines:**
- Follow Swift best practices and TCA patterns in all contributions
- Include comprehensive tests and documentation
- Ensure AI-optimized outputs for agent integration
- Validate with Smith tools before submitting

See individual repositories for specific contribution guidelines and issue reporting.

---

## 📊 Ecosystem Metrics

- **122+ Knowledge Documents**: Covering TCA, SwiftUI, visionOS, SharePlay, and Swift patterns
- **3,216 WWDC Sessions**: 2014-2025 with encrypted local storage
- **43-95% Context Reduction**: Across all build analysis tools
- **Sub-millisecond Search**: FTS5 with BM25 ranking
- **Multi-Platform Support**: iOS, macOS, visionOS, and cross-platform patterns

---

## 📄 License

All Smith Tools components are released under the MIT License.

---

**Built with ❤️ by the Smith Tools team**
*AI-powered Swift development ecosystem for modern teams that ship exceptional code*