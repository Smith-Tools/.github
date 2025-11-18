# Smith Tools - Swift Architecture Validation Framework

> **Automated architectural analysis, pattern validation, and agentic guidance for production-ready Swift applications.**

---

## 🎯 What is Smith Tools?

Smith Tools is a comprehensive framework that helps Swift teams:

- **Prevent architectural violations** with automated validation (Rules 1.1-1.5)
- **Extract monolithic features** systematically with effort estimation
- **Improve testability** by detecting closure injection and untestable patterns
- **Validate code patterns** against expert best practices
- **Integrate guidance** directly into Claude Code workflow
- **Access Apple documentation** with WWDC context through sosumi

### The Problem We Solve

Developers waste time on:
- ✗ Deciding when to extract reducers vs. keep state flat
- ✗ Understanding whether their architecture violates composition rules
- ✗ Finding the WWDC session that explained this exact pattern
- ✗ Knowing how much effort refactoring will take
- ✗ Validating code against inconsistent architectural standards

Smith Tools solves this in seconds.

---

## 🚀 Quick Start (3 Steps)

### For Claude Code Users (Recommended)

```bash
# 1. Install smith skill
git clone https://github.com/Smith-Tools/smith-skill.git
ln -s $(pwd)/smith-skill ~/.claude/skills/smith

# 2. Install sosumi skill (optional, but recommended)
git clone https://github.com/Smith-Tools/sosumi.git
ln -s $(pwd)/sosumi ~/.claude/skills/sosumi

# 3. Use in Claude
"Use Smith skill to analyze my TCA reducer"
```

**Result:** Claude automatically detects your architecture question and routes to the right patterns, with optional WWDC context from sosumi.

### For CLI Users (Direct Validators)

```bash
# Quick TCA composition analysis
./smith-skill/Scripts/validate-tca-composition.sh Sources/

# Get testability score
./smith-skill/Scripts/check-tca-testability.sh Sources/

# Extract recommendations
./smith-skill/Scripts/recommend-tca-extractions.sh Sources/
```

### For CI/CD Integration

```yaml
- name: Validate TCA Architecture
  run: |
    ./smith-skill/Scripts/validate-tca-composition.sh Sources/ --strict
    ./smith-skill/Scripts/check-tca-testability.sh Sources/ --threshold 75
```

---

## 📦 What's Included

Smith Tools is a collection of independent, well-integrated components:

### **smith-skill** - Claude Agentic Skill (v1.2.0)

The main integration point for Claude Code users. Provides:

- **TCA Composition Validators** - Automatically detect architectural violations
- **Build Analysis Tools** - Context-efficient compilation debugging
- **Pattern Library** - 40+ validated TCA, concurrency, and testing patterns
- **Decision Trees** - Architectural guidance for common scenarios
- **visionOS/iOS/macOS Patterns** - Platform-specific best practices

**Status:** v1.2.0 (with integrated sosumi routing)
**Repository:** https://github.com/Smith-Tools/smith-skill

### **sosumi-skill** - Apple Documentation + WWDC

Complementary skill providing real-time access to Apple ecosystem:

- **Apple Documentation** - Swift, SwiftUI, Combine, RealityKit, and more
- **WWDC Transcripts** - 2018-2025 sessions (searchable, cached)
- **Code Examples** - From Apple's official documentation
- **Intelligent Routing** - Works seamlessly with smith-skill

**Status:** Production-ready
**Repository:** https://github.com/Smith-Tools/sosumi

### **TCA Composition Validators** - Four Powerful Scripts

Automated architectural analysis:

1. **validate-tca-composition.sh** - Detects Rules 1.1-1.5 violations
   - Monolithic features (State > 15 props, Actions > 40 cases)
   - Closure dependency injection (blocks testing)
   - Code duplication
   - Unclear organization
   - Tight state coupling

2. **check-tca-testability.sh** - Testability scoring (0-100)
   - Identifies testing blockers
   - Scores @Dependency usage
   - Provides improvement guidance

3. **recommend-tca-extractions.sh** - Feature extraction planning
   - Prioritizes extractions by value
   - Estimates effort (2h - 12h)
   - Sprint planning guidance

4. **analyze-tca-dependency-graph.sh** - Complexity mapping
   - Maps state dependencies
   - Calculates coupling scores
   - Identifies problematic patterns

### **Analysis Tools**

**smith-core** - Universal Swift Patterns
- Dependency injection (@Dependency patterns)
- Swift concurrency (async/await, @MainActor)
- Modern testing (Swift Testing, @Test)
- Access control boundaries
- Type-safe error handling

**smith-spmsift** - SPM Analysis
- 96% reduction in output verbosity
- Circular dependency detection
- Deep import analysis
- Dependency health scoring

**smith-sbsift** - Swift Build Analysis
- Compilation bottleneck identification
- Progress monitoring
- ETA calculations
- Resource usage tracking

**smith-xcsift** - Xcode Analysis
- Build hang detection
- Index store corruption detection
- Workspace build monitoring
- Schema analysis

---

## 💡 How It Works

### The Workflow

```
Your Question
    ↓
    ├─ Architecture question? → smith-skill
    ├─ API reference needed? → sosumi-skill
    └─ Both? → Combined response (optimal)
    ↓
Expert Guidance + Code
    ↓
Production-ready solution
```

### Real Example: RCP Timeline Query

**Your question:** "How do I play RCP timelines directly without Behaviors using playAnimation()?"

**Smith provides:**
- Architecture pattern (Behavior vs direct call)
- TCA integration recommendation
- When to use which approach

**Sosumi provides:**
- `playAnimation()` exact API signature
- Code examples from Apple
- WWDC session references (2023, 2024, 2025)
- RealityComposer Pro timeline guide

**Result:** Complete understanding + implementation + WWDC context

---

## 📊 Performance & Efficiency

### Comparison: WebSearch vs Smith Tools

| Query Type | WebSearch | Smith + Sosumi | Savings |
|-----------|-----------|----------------|---------|
| API lookup | 1,500 tokens | 700 tokens | 53% |
| Architecture pattern | 2,000 tokens | 400 tokens | 80% |
| WWDC context + API | 3,000 tokens | 1,000 tokens | 67% |
| **Average** | **2,167 tokens** | **700 tokens** | **68%** |

### Benefits Beyond Tokens

- ✅ No network latency (local validators)
- ✅ Cached WWDC context (no repeated searches)
- ✅ Integrated workflow (no context switching)
- ✅ Architectural validation (not just API docs)
- ✅ CI/CD ready (bash scripts)

---

## 🎓 TCA Composition Rules (1.1-1.5)

Smith enforces five foundational architectural rules:

| Rule | Problem | Trigger | Solution | Effort |
|------|---------|---------|----------|--------|
| **1.1** | Monolithic feature | State > 15 props OR Actions > 40 | Extract child features | 4-8h |
| **1.2** | Untestable closures | `var x: (...) -> Effect` | Use @Dependency | 2h |
| **1.3** | Code duplication | Duplicate handlers | Consolidate | 1h |
| **1.4** | Unclear organization | 5+ vague methods | Better naming | 4-8h |
| **1.5** | Tight coupling | 5+ child features | Reduce nesting | 6-12h |

---

## ✨ What's New in v1.2.0

**smith-skill:**
- ✅ TCA Composition Validators (4 powerful bash scripts)
- ✅ Integrated sosumi routing
- ✅ WWDC coverage updated to 2025
- ✅ Enhanced pattern library (40+ patterns)
- ✅ Improved visionOS documentation

**sosumi-skill:**
- ✅ Real-time Apple documentation access
- ✅ WWDC transcripts 2018-2025
- ✅ Seamless integration with smith-skill
- ✅ Production-ready implementation

---

## 🔗 Links

**Core Skills:**
- **smith-skill Repository:** https://github.com/Smith-Tools/smith-skill
- **sosumi Repository:** https://github.com/Smith-Tools/sosumi
- **Organization:** https://github.com/Smith-Tools

**Analysis Tools:**
- **smith-core:** https://github.com/Smith-Tools/smith-core
- **smith-spmsift:** https://github.com/Smith-Tools/smith-spmsift
- **smith-sbsift:** https://github.com/Smith-Tools/smith-sbsift
- **smith-xcsift:** https://github.com/Smith-Tools/smith-xcsift

---

## ✅ Status

**v1.2.0 - Production Ready**

- ✅ TCA Composition Validators (tested)
- ✅ Sosumi Integration (verified)
- ✅ WWDC Coverage (2018-2025)
- ✅ Documentation (comprehensive)
- ✅ GitHub Synced
- ✅ Ready for Production Use

---

**Smith Tools - Making Swift Architecture Production-Ready**

*Automated validation, expert patterns, agentic guidance - all built for real projects.*

---

Last updated: November 18, 2025
Version: v1.2.0
Status: Production Ready