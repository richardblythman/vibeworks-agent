# Miha Rothl Demo Notes

## Background & Introduction

Miha is a software engineer who discovered Claude in October and spent two months building a full-scale project. His story: "From 0 to 100 lines of code in two months" - demonstrating Claude's capability as an AI pair programmer.

### Initial Discovery

- Friend recommended Claude in October
- Was reluctant initially (kept putting it off)
- Tried setting up with PyCharm/JetBrains (didn't work with his version)
- Switched to VS Code
- Discovery moment: During CLI setup (`curl code cli` installation), realized he loved the terminal interface and decided to play around instead of just setting up a plugin

## First Project: Personal Minecraft

**Scope**: Built a Minecraft-like 3D game in C from scratch in half an hour

**Approach**:
- Stayed in terminal the entire time
- Didn't need to check what Claude was doing
- Process was: describe step → Claude delivers → test → describe next step

**Key Steps**:
1. Wire up OpenGL and set up projection matrix
   - Claude handled it, resolved compilation errors
   - Saw black window (success indicator)
2. Project cube onto the scene (immediate success)
3. Add WASD movement and mouse look controls
4. Create explorable 3D world
5. Implement ray casting for block mining/placing

**Impact**:
- First realization of Claude's power compared to ChatGPT
- Previously spent 3 years copying basic code from ChatGPT (Ctrl+C, Ctrl+V)
- Now: just press Enter and move forward

## Main Project: Legal Direct

**Timeline**: Built over two months (summer project)

**Project Type**: Legal tech agentic RAG (Retrieval-Augmented Generation) system for Irish law

**Components Built**:
1. **Crawler** - scrapes public legal websites, downloads documents
2. **Parser** - parses documents to extract structured data
3. **Embedder** - transforms text into embeddings using ML model
4. **Vector Database** - stores embedded information
5. **Services** - supporting microservices
6. **User Interface** - chatbot interface for querying

### Scale & Comparison

**Lines of Code**: ~80,000 lines produced by Claude in 2 months

**Historical Comparison**:
- One year prior worked on similar project with 6-person team
- That team produced ~90,000 lines using same tech stack (Python APIs, TypeScript frontend)
- Miha's results:
  - Same line count in half the time
  - Better code coverage with Claude
  - Fraction of the cost
  - Vastly superior quality

### Key Technology Choices

- **Backend**: Python (APIs)
- **Frontend**: TypeScript
- **Infrastructure**: Kubernetes clusters with GPUs
- **Vector Database**: Custom infrastructure setup

## Claude as AI Pair Programmer

### Workflow Philosophy

Miha uses Claude more as a senior engineer pair programmer rather than white-box coding tool:
- Claude reminds him of edge cases
- Brainstorms system design together
- Collaborates on component naming
- Documents code (Claude handles this automatically)
- Writes supporting tools (index recreation, database utilities, etc.)
- Implements comprehensive testing (handles test code generation)

### Capability Assessment

- **View**: Claude operates at a senior software engineer level, not junior
- Anthropic positioning: junior engineer
- Miha's assessment: already senior, improving rapidly ("What's coming next year?")

## Specification-Driven Development (SDD)

### RFC (Request for Comment) Documents

Miha's key innovation: Using specifications as the interface between himself and Claude

**Process**:
1. Write RFC specification document (learned from open-source tradition)
2. Use Claude to write the initial specification
3. Use another Claude conversation to review/iterate
4. Iterate until specification converges on solution
5. Load specification context into Claude before implementation
6. Claude implements according to spec

### Three Levels of SDD (Martin Fowler concept)

**Level 1 - Spec First**
- Write specification
- Agent generates code
- Throw away specification
- (Not sustainable for production)

**Level 2 - Spec Anchored** (Miha's current approach)
- Write specification
- Agent generates code
- Keep both specification and code in sync
- Specification guides implementations

**Level 3 - Spec as Source** (Future direction)
- Only write specifications
- Never touch code directly
- Higher-level programming language
- Tools emerging: GitHub Spec Kit, TESOL

**Important Note**: SDD is cited as "one of the most important things you can learn right now" - enables unlimited scalability in what you can build

## Development Workflow

### Project Structure (Foundation)

**Layer 1: Foundation**
- Code style specifications
- Git workflow standards
- Testing approach for each package

**Layer 2: Architecture**
- Clean/Hexagonal architecture patterns
- REST API specifications
- Security standards

**Layer 3: Infrastructure**
- Kubernetes cluster definitions
- Registry locations
- Namespace policies

**Layer 4: Package Structure**
- Python package layout standards
- TypeScript project structure
- Script locations and naming

**Layer 5: Services** (What we're building)
- Platform services (Customer, Identity, Monetization)
- Crawler specifications
- Parser specifications
- Embedder architecture
- Inter-service communication patterns

### Implementation Workflow

1. **Create RFC** - Specification document defining service/feature
2. **Load Context** - RFC loaded into Claude conversation
3. **Implement** - Claude writes code based on specification
4. **Monitor** - Actively read Claude's output, remind of previous decisions via RFC references
5. **Testing**:
   - Libraries: target 100% code coverage
   - APIs/Interfaces: 80% unit test coverage or 60% integration test coverage
6. **Build**: Claude creates Docker/Podman images and pushes to registry
7. **Deploy**: Claude updates Helm charts and can deploy (usually manual)

## Key Insights & Principles

### What Matters in Production

1. **Human Skill**: While AI generates 20 different solutions for each problem, human judgment determines what ages well in production

2. **AI as Amplifier**: AI amplifies whatever you give it - good constraints produce good code, bad constraints produce bad results

3. **Constraints Drive Quality**:
   - Architectural constraints
   - Build gates
   - Test coverage requirements

4. **Domain Understanding**: Essential human knowledge
   - Network understanding (referenced Steven's expertise)
   - Business logic
   - System design patterns
   - Leave tactical implementation (Python tricks, Kubernetes config) to LLMs

5. **Ownership Cycle**: One person can now own entire project lifecycle
   - Before: distributed across multiple roles
   - Now: single person with AI pair programmer covers crawler → implementation → deployment

## Productivity & Economic Impact

### The Shift (2024 vs 2025)

**2024 Reality**:
- Need budget, team, meetings, roadmap
- Multi-person coordination required
- Higher overhead

**2025 Reality**:
- One person with clear vision + Claude can do everything
- Design, implement, enforce quality, deploy
- Half the time traditional team needs
- Fraction of cost

### Solo Builder Power

- "Solo builders can punch with the force of a small IT department"
- What once cost multi-hundred thousand dollars, one person builds in 2 months
- New workflow is "definitely a game changer"

### The Scary Part

- Traditional routine coding value dropping rapidly
- Economic disruption of conventional development workflows
- Need for rethinking talent/roles

## Background & Philosophy

**Professional Background**: Software engineer with multi-year professional experience

**Key Philosophy**: Treat Claude as a capable colleague/senior engineer, not a code snippet generator
- Provide good specifications and constraints
- Collaborate on design and quality
- Let Claude handle the implementation details
- Focus human effort on architecture, domain understanding, and quality gates

## Comparison: ChatGPT vs Claude

**Before Claude (ChatGPT era)**:
- 3 years of copying basic code snippets
- High friction workflow
- Limited ability to build complete systems
- Keyboard shortcuts: Ctrl+C, Ctrl+V

**With Claude**:
- Comprehensive system building in weeks
- Just press Enter to move forward
- Senior-level code quality
- Can maintain 80-100% test coverage
- Production-ready architectures

