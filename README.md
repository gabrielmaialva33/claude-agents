<h1 align="center">
  <br>
  <img src="https://raw.githubusercontent.com/gabrielmaialva33/claude-agents/master/.github/assets/claude-agent-logo.svg" alt="Claude Agents" width="200">
  <br>
  Claude Agents - AI Development Team 🚀
  <br>
</h1>

<p align="center">
  <strong>Supercharge Claude Code with a team of specialized AI agents that work together to build complete features</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/github/license/gabrielmaialva33/claude-agents?color=00b8d3?style=flat&logo=appveyor" alt="License" />
  <img src="https://img.shields.io/github/languages/top/gabrielmaialva33/claude-agents?style=flat&logo=appveyor" alt="GitHub top language" >
  <img src="https://img.shields.io/github/languages/count/gabrielmaialva33/claude-agents?style=flat&logo=appveyor" alt="GitHub language count" >
  <img src="https://img.shields.io/github/repo-size/gabrielmaialva33/claude-agents?style=flat&logo=appveyor" alt="Repository size" >
  <a href="https://github.com/gabrielmaialva33/claude-agents/commits/master">
    <img src="https://img.shields.io/github/last-commit/gabrielmaialva33/claude-agents?style=flat&logo=appveyor" alt="GitHub last commit" >
    <img src="https://img.shields.io/badge/made%20by-Maia-15c3d6?style=flat&logo=appveyor" alt="Maia" >  
  </a>
</p>

<br>

<p align="center">
  <a href="#bookmark-about">About</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#rocket-quick-start">Quick Start</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#busts_in_silhouette-meet-your-team">Meet Your Team</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#sparkles-features">Features</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#books-documentation">Documentation</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#memo-license">License</a>
</p>

<br>

## :bookmark: About

**Claude Agents** is a collection of 34+ specialized AI agents that extend Claude Code's capabilities through
intelligent orchestration and domain expertise. Each agent masters specific technologies and patterns, working together
as your AI development team.

### :warning: Important Notice

**This project is experimental and token-intensive.** Multi-agent orchestration can consume 10-50k tokens per complex
feature. Use with caution and monitor your usage.

## :rocket: Quick Start

### :heavy_check_mark: Prerequisites

- **Claude Code CLI** installed and authenticated
- **Claude subscription** - required for intensive agent workflows
- Active project directory with your codebase
- **Optional**: [Context7 MCP](docs/dependencies.md) for enhanced documentation access

### :arrow_down: Installation

```bash
git clone https://github.com/gabrielmaialva33/claude-agents.git
```

#### Option A: Symlink (Recommended - auto-updates)

**macOS/Linux:**

```bash
# Create agents directory if it doesn't exist (preserves existing agents)
mkdir -p ~/.claude/agents

# Symlink the claude-agents collection
ln -sf "$(pwd)/claude-agents/agents/" ~/.claude/agents/claude-agents
```

**Windows (PowerShell):**

```powershell
# Create agents directory
New-Item -Path "$env:USERPROFILE\.claude\agents" -ItemType Directory -Force

# Create symlink
cmd /c mklink /D "$env:USERPROFILE\.claude\agents\claude-agents" "$(Get-Location)\claude-agents\agents"
```

#### Option B: Copy (Static - no auto-updates)

```bash
# Create agents directory if it doesn't exist
mkdir -p ~/.claude/agents

# Copy all agents
cp -r claude-agents/agents ~/.claude/agents/claude-agents
```

### :white_check_mark: Verify Installation

```bash
claude /agents
# Should show all 24 agents.
```

### :gear: Initialize Your Project

**Navigate** to your **project directory** and run the following command to configure your AI team:

```bash
claude "use @agent-team-configurator and optimize my project to best use the available subagents."
```

### :rocket: Start Building

```bash
claude "use @agent-tech-lead-orchestrator and build a user authentication system"
```

Your AI team will automatically detect your stack and use the right specialists!

## :dart: How Auto-Configuration Works

The @agent-team-configurator automatically sets up your perfect AI development team. When invoked, it:

1. **Locates CLAUDE.md** - Finds existing project configuration and preserves all your custom content outside the "AI
   Team Configuration" section
2. **Detects Technology Stack** - Inspects package.json, composer.json, requirements.txt, go.mod, Gemfile, and build
   configs to understand your project
3. **Discovers Available Agents** - Scans ~/.claude/agents/ and .claude/ folders, building a capability table of all
   available specialists
4. **Selects Specialists** - Prefers framework-specific agents over universal ones, always includes @agent-code-reviewer
   and @agent-performance-optimizer for quality assurance
5. **Updates CLAUDE.md** - Creates a timestamped "AI Team Configuration" section with your detected stack and a
   Task|Agent|Notes mapping table
6. **Provides Usage Guidance** - Shows you the detected stack, selected agents, and gives sample commands to start
   building

## :busts_in_silhouette: Meet Your AI Development Team

### :performing_arts: Orchestrators (3 agents)

- **[Tech Lead Orchestrator](agents/orchestrators/tech-lead-orchestrator.md)** - Senior technical lead who analyzes
  complex projects and coordinates multi-step development tasks
- **[Project Analyst](agents/orchestrators/project-analyst.md)** - Technology stack detection specialist who enables
  intelligent agent routing
- **[Team Configurator](agents/orchestrators/team-configurator.md)** - AI team setup expert who detects your stack and
  configures optimal agent mappings

### :briefcase: Framework Specialists (17 agents)

- **Laravel (2 agents)**
    - **[Backend Expert](agents/specialized/laravel/laravel-backend-expert.md)** - Comprehensive Laravel development
      with MVC, services, and Eloquent patterns
    - **[Eloquent Expert](agents/specialized/laravel/laravel-eloquent-expert.md)** - Advanced ORM optimization, complex
      queries, and database performance
- **Django (3 agents)**
    - **[Backend Expert](agents/specialized/django/django-backend-expert.md)** - Models, views, services following
      current Django conventions
    - **[API Developer](agents/specialized/django/django-api-developer.md)** - Django REST Framework and GraphQL
      implementations
    - **[ORM Expert](agents/specialized/django/django-orm-expert.md)** - Query optimization and database performance for
      Django applications
- **Rails (3 agents)**
    - **[Backend Expert](agents/specialized/rails/rails-backend-expert.md)** - Full-stack Rails development following
      conventions
    - **[API Developer](agents/specialized/rails/rails-api-developer.md)** - RESTful APIs and GraphQL with Rails
      patterns
    - **[ActiveRecord Expert](agents/specialized/rails/rails-activerecord-expert.md)** - Complex queries and database
      optimization
- **React (2 agents)**
    - **[Component Architect](agents/specialized/react/react-component-architect.md)** - Modern React patterns, hooks,
      and component design
    - **[Next.js Expert](agents/specialized/react/react-nextjs-expert.md)** - SSR, SSG, ISR, and full-stack Next.js
      applications
- **Vue (3 agents)**
    - **[Component Architect](agents/specialized/vue/vue-component-architect.md)** - Vue 3 Composition API and component
      patterns
    - **[Nuxt Expert](agents/specialized/vue/vue-nuxt-expert.md)** - SSR, SSG, and full-stack Nuxt applications
    - **[State Manager](agents/specialized/vue/vue-state-manager.md)** - Pinia and Vuex state architecture
- **NestJS (3 agents)**
    - **[Backend Expert](agents/specialized/nestjs/nestjs-backend-expert.md)** - Enterprise NestJS with Fastify platform,
      modules, dependency injection, and decorators
    - **[Objection.js Expert](agents/specialized/nestjs/nestjs-objection-expert.md)** - Objection.js ORM, Knex migrations,
      complex relations, and query optimization
    - **[Microservices Expert](agents/specialized/nestjs/nestjs-microservices-expert.md)** - Distributed systems with Fastify,
      RabbitMQ, Kafka, gRPC, and saga patterns
- **AdonisJS (2 agents)**
    - **[Backend Expert](agents/specialized/adonisjs/adonisjs-backend-expert.md)** - Comprehensive AdonisJS v6 development
      with IoC container, service layer, and Lucid ORM
    - **[ACL Expert](agents/specialized/adonisjs/adonisjs-acl-expert.md)** - Access control, RBAC, ABAC, and fine-grained
      permission systems

### :globe_with_meridians: Universal Experts (4 agents)

- **[Backend Developer](agents/universal/backend-developer.md)** - Polyglot backend development across multiple
  languages and frameworks
- **[Frontend Developer](agents/universal/frontend-developer.md)** - Modern web technologies and responsive design for
  any framework
- **[API Architect](agents/universal/api-architect.md)** - RESTful design, GraphQL, and framework-agnostic API
  architecture
- **[Tailwind Frontend Expert](agents/universal/tailwind-css-expert.md)** - Tailwind CSS styling, utility-first
  development, and responsive components

### :wrench: Core Team (9 agents)

- **[Code Archaeologist](agents/core/code-archaeologist.md)** - Explores, documents, and analyzes unfamiliar or legacy
  codebases
- **[Code Reviewer](agents/core/code-reviewer.md)** - Rigorous security-aware reviews with severity-tagged reports
- **[Performance Optimizer](agents/core/performance-optimizer.md)** - Identifies bottlenecks and applies optimizations
  for scalable systems
- **[Documentation Specialist](agents/core/documentation-specialist.md)** - Crafts comprehensive READMEs, API specs, and
  technical documentation
- **[Intelligent Search Agent](agents/core/intelligent-search-agent.md)** - Semantic code discovery combining local and
  AI-powered search
- **[Multi-File Refactor](agents/specialized/multi-file-refactor.md)** - Atomic refactoring operations across entire
  codebases
- **[Batch File Processor](agents/specialized/batch-file-processor.md)** - High-volume file operations with parallel
  processing
- **[Code Migration Specialist](agents/specialized/code-migration-specialist.md)** - Framework and version migrations
  with zero downtime
- **[API Security & Pentest Expert](agents/specialized/security/api-security-pentest-expert.md)** - Defensive security
  testing, OWASP Top 10, and vulnerability assessment

**Total: 33 specialized agents** working together to build your projects!

[Browse all agents →](agents/)

## :sparkles: Features

### Core Capabilities

- **Specialized Expertise**: Each agent masters their domain with deep, current knowledge
- **Real Collaboration**: Agents coordinate seamlessly, sharing context and handing off tasks
- **Tailored Solutions**: Get code that matches your exact stack and follows its best practices
- **Parallel Execution**: Multiple specialists work simultaneously for faster delivery

### Advanced Features (v2.0)

- **MultiEdit Operations**: Atomic changes across multiple files
- **MCP Integration**: Exa semantic search and Ref documentation lookup
- **Parallel Processing**: Execute independent operations concurrently
- **Intelligent Routing**: Automatic agent selection based on task
- **Progress Tracking**: Real-time status updates with checkpoints

## :chart_with_upwards_trend: The Impact

- **Ship Faster** - Complete features in minutes, not days
- **Better Code Quality** - Every line follows best practices
- **Learn As You Code** - See how experts approach problems
- **Scale Confidently** - Architecture designed for growth

## :books: Documentation

- [Creating Custom Agents](docs/creating-agents.md) - Build specialists for your needs
- [Best Practices](docs/best-practices.md) - Get the most from your AI team
- [Multi-File Patterns](docs/multi-file-patterns.md) - Advanced patterns for large-scale operations
- [Enhanced Agent Template](templates/enhanced-agent-template.md) - Optimized template for new agents

## :speech_balloon: Join The Community

- ⭐ **Star this repo** to show support
- 🐛 [Report issues](https://github.com/gabrielmaialva33/claude-agents/issues)
- 💡 [Share ideas](https://github.com/gabrielmaialva33/claude-agents/discussions)
- 🎉 [Success stories](https://github.com/gabrielmaialva33/claude-agents/discussions/categories/show-and-tell)

## :memo: License

MIT License - Use freely in your projects!

## :star: Star History

[![Star History Chart](https://api.star-history.com/svg?repos=gabrielmaialva33/claude-agents&type=Date)](https://www.star-history.com/#gabrielmaialva33/claude-agents&Date)
---

<p align="center">
  <strong>Transform Claude Code into an AI development team that ships production-ready features</strong><br>
  <em>Simple setup. Powerful results. Just describe and build.</em>
</p>

### :writing_hand: Author

| [![Gabriel Maia](https://avatars.githubusercontent.com/u/26732067?size=100)](https://github.com/gabrielmaialva33) |
|-------------------------------------------------------------------------------------------------------------------|
| [Gabriel Maia](https://github.com/gabrielmaialva33)                                                               |

<br>

<p align="center"><img src="https://raw.githubusercontent.com/gabrielmaialva33/gabrielmaialva33/master/assets/gray0_ctp_on_line.svg?sanitize=true" /></p>
<p align="center">&copy; 2025-present <a href="https://github.com/gabrielmaialva33/" target="_blank">Maia</a></p>
