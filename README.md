# LLM System Prompts

A comprehensive collection of specialized system prompts for Large Language Models (LLMs) designed to enable end-to-end software development lifecycle management with expert-level capabilities across multiple domains.

## Overview

This repository contains meticulously crafted system prompts that transform LLMs into specialized software development agents, each with deep expertise in specific domains. These prompts implement industry best practices, enforce quality standards, and provide structured approaches to complex software engineering challenges.

## Architecture

The prompt system is built around a **specialized agent architecture** where each agent focuses on a specific aspect of software development:

```text
┌─────────────────────────────────────────────────────────────┐
│                     All-In-Full Agent                      │
│           (Master orchestrator combining all)               │
└─────────────────────────────────────────────────────────────┘
                               │
        ┌──────────────────────┼──────────────────────┐
        │                      │                      │
┌───────▼────────┐    ┌────────▼────────┐    ┌───────▼────────┐
│   Plan Agent   │    │  Review Agent   │    │  Coder Agent   │
│  Architecture  │    │  Code Analysis  │    │ Implementation │
│   & Design     │    │   & Quality     │    │   & Testing    │
└────────────────┘    └─────────────────┘    └────────────────┘
        │                      │                      │
┌───────▼────────┐    ┌────────▼────────┐    ┌───────▼────────┐
│ Frontend Agent │    │  Tester Agent   │    │ Bootstrap Agent │
│    UI/UX Dev   │    │   QA & Test     │    │ Project Setup & │
│  & Optimization│    │   Automation    │    │ Environment Init│
└────────────────┘    └─────────────────┘    └────────────────┘
```

## Agent Specifications

### 🎯 **All-In-Full Agent** (`all-in-full.md`)
**Master orchestrator** combining all specialized capabilities into a unified development experience.

- **Purpose**: Complete end-to-end software development lifecycle management
- **Capabilities**: Architecture planning, implementation, testing, deployment, monitoring
- **Use Case**: Full-stack project development from conception to production
- **Key Features**: SOLID principles enforcement, Clean Architecture compliance, security-first design

### 📐 **Plan Agent** (`plan.md`)
**Technical architect** responsible for macro architecture and strategic technical decisions.

- **Purpose**: System architecture design and technology selection
- **Capabilities**: Architecture proposals, technology evaluation, scalability planning
- **Use Case**: Project architecture definition and technical roadmap planning
- **Key Features**: Business-driven technical decisions, migration path planning

### 🔍 **Review Agent** (`review.md`)
**Code quality expert** focused on diagnostic analysis and improvement recommendations.

- **Purpose**: Code quality assessment and technical debt management
- **Capabilities**: Code analysis, refactoring strategies, performance optimization
- **Use Case**: Code reviews, quality audits, legacy system modernization
- **Key Features**: Deep diagnostic analysis, actionable improvement plans

### 💻 **Coder Agent** (`coder.md`)
**Senior polyglot engineer** for clean, tested, production-ready implementation.

- **Purpose**: Code implementation and feature development
- **Capabilities**: Multi-language development, testing, integration
- **Use Case**: Feature implementation, bug fixes, code optimization
- **Key Features**: Incremental delivery, test-driven development, clean code practices

### 🎨 **Frontend Agent** (`frontend.md`)
**UI/UX specialist** for modern, accessible, performant user interfaces.

- **Purpose**: Frontend development and user experience optimization
- **Capabilities**: Component development, performance optimization, accessibility
- **Use Case**: Web application frontends, mobile interfaces, design systems
- **Key Features**: Modern frameworks, responsive design, Core Web Vitals optimization

### 🧪 **Tester Agent** (`tester.md`)
**Quality assurance expert** for comprehensive testing strategies and automation.

- **Purpose**: Test strategy design and quality assurance
- **Capabilities**: Test automation, quality metrics, regression prevention
- **Use Case**: Test suite development, QA processes, quality gate implementation
- **Key Features**: Test pyramid implementation, automated testing pipelines



### 🚀 **Bootstrap Agent** (`bootstrap.md`)
**Project initialization expert** for rapid development environment setup.

- **Purpose**: Project scaffolding and development environment configuration
- **Capabilities**: Project templates, tooling setup, CI/CD initialization
- **Use Case**: New project creation, development environment standardization
- **Key Features**: Best practice templates, automated setup, tool integration

## Core Principles

All agents adhere to these fundamental principles:

### 🏗️ **Clean Architecture**
- Strict layer separation with dependency inversion
- Domain-driven design with clear bounded contexts
- Infrastructure independence and testability

### 🔒 **Security by Design**
- Security considerations embedded from inception
- Threat modeling and risk assessment
- Secure coding practices and vulnerability prevention

### ⚡ **Performance Optimization**
- Performance-aware design and implementation
- Resource efficiency and scalability planning
- Monitoring and observability integration

### 🧪 **Quality Assurance**
- Comprehensive testing strategies (unit, integration, e2e)
- Automated quality gates and validation
- Continuous improvement and technical debt management

### 📚 **Documentation Driven**
- Comprehensive documentation throughout development
- API documentation and architectural decision records
- Knowledge sharing and team training

## Technology Support

### **Backend Technologies**
- **Languages**: TypeScript/JavaScript, Python, Go, Rust, Java, PHP
- **Frameworks**: Node.js/Express, FastAPI, Spring Boot, .NET, Django
- **Databases**: PostgreSQL, MySQL, MongoDB, Redis, InfluxDB

### **Frontend Technologies**
- **Frameworks**: React, Vue.js, Svelte, Next.js, Nuxt.js
- **Styling**: Tailwind CSS, CSS Modules, Styled Components
- **State Management**: Redux, Vuex, Pinia, Zustand

### **Infrastructure Technologies**
- **Orchestration**: Kubernetes, Docker Swarm
- **Cloud Providers**: AWS, GCP, Azure, Digital Ocean
- **CI/CD**: GitHub Actions, GitLab CI, Woodpecker CI
- **Monitoring**: Prometheus, Grafana, OpenTelemetry, Jaeger

## Usage Patterns

### **Single Agent Usage**
Use individual agents for specific tasks:

```bash
# Architecture planning
cat plan.md | llm "Design a microservices architecture for an e-commerce platform"

# Code implementation
cat coder.md | llm "Implement a REST API for user management with authentication"

# Frontend development
cat frontend.md | llm "Create a responsive React component library with accessibility features"
```

### **Combined Agent Workflow**
Chain agents for comprehensive development:

1. **Planning Phase**: Use `plan.md` for architecture design
2. **Implementation Phase**: Use `coder.md` for feature development
3. **Quality Phase**: Use `review.md` and `tester.md` for validation
4. **Bootstrap Phase**: Use `bootstrap.md` for project setup and environment initialization

### **Master Agent Usage**
Use `all-in-full.md` for complete project management:

```bash
# Full-stack development
cat all-in-full.md | llm "Build a real-time chat application with React frontend and Node.js backend"
```

## Quality Standards

### **Code Quality Metrics**
- **Test Coverage**: Minimum 80% for critical modules
- **Code Complexity**: Cyclomatic complexity < 10
- **Security**: Zero high-severity vulnerabilities
- **Performance**: Core Web Vitals compliance for frontends

### **Documentation Requirements**
- **API Documentation**: OpenAPI/GraphQL schema documentation
- **Architecture Decision Records**: Significant technical decisions
- **Deployment Guides**: Step-by-step operational procedures
- **Troubleshooting Guides**: Common issues and resolution steps

### **Delivery Standards**
- **SOLID Principles**: Applied across all code components
- **Clean Architecture**: Layer separation and dependency rules
- **Security Compliance**: Industry standards and best practices
- **Performance Benchmarks**: Established and monitored SLAs

## Project Structure Templates

### **Full-Stack Web Application**
```text
project-name/
├── apps/
│   ├── web/                    # Frontend (React/Vue/Svelte)
│   └── api/                    # Backend (Node.js/Python/Go)
├── packages/
│   ├── shared/                 # Shared utilities
│   └── types/                  # Type definitions
├── infrastructure/
│   ├── kubernetes/             # K8s manifests
│   └── terraform/              # Infrastructure as code
├── docs/                       # Documentation
└── scripts/                    # Development scripts
```

### **Microservices Architecture**
```text
microservices-project/
├── services/
│   ├── user-service/
│   ├── product-service/
│   └── order-service/
├── libs/
│   ├── common/                 # Shared libraries
│   └── events/                 # Event definitions
├── infrastructure/
│   ├── k8s/                    # Kubernetes manifests
│   └── monitoring/             # Observability stack
└── docs/
    ├── api/                    # API documentation
    └── architecture/           # System documentation
```

## Best Practices Integration

### **Development Workflow**
1. **Requirements Analysis**: Clear scope and acceptance criteria
2. **Architecture Planning**: Technology selection and system design
3. **Implementation**: Incremental development with testing
4. **Quality Assurance**: Code review and automated testing
5. **Deployment**: Infrastructure provisioning and monitoring
6. **Maintenance**: Continuous improvement and optimization

### **Quality Gates**
- **Code Review**: SOLID principles and clean code validation
- **Automated Testing**: Comprehensive test suite execution
- **Security Scanning**: Vulnerability assessment and compliance
- **Performance Testing**: Benchmark validation and optimization
- **Documentation Review**: Completeness and accuracy verification

### **Operational Excellence**
- **Monitoring**: Comprehensive observability and alerting
- **Incident Response**: Rapid detection and resolution procedures
- **Disaster Recovery**: Backup and restoration strategies
- **Continuous Improvement**: Regular retrospectives and optimization

## Contributing

When contributing new agents or improving existing ones:

1. **Follow Formatting Standards**: 80-character soft wrap, clear section structure
2. **Maintain Consistency**: Use established patterns and terminology
3. **Include Examples**: Provide concrete usage examples and code snippets
4. **Document Changes**: Update this README with new capabilities
5. **Test Thoroughly**: Validate prompts with real-world scenarios

## Security Considerations

- **No Sensitive Data**: These prompts contain no API keys or credentials
- **Open Source Safe**: All content is designed for public repositories
- **Security Awareness**: Agents promote security best practices
- **Compliance Ready**: Support for industry standards and regulations

## License

This project is released under the MIT License. See the LICENSE file for details.

## Support

For questions, improvements, or contributions:

- **Issues**: Report bugs or request features
- **Discussions**: Share usage patterns and best practices
- **Pull Requests**: Contribute improvements and new capabilities

---

**Ready to transform your development workflow with expert-level AI assistance across the entire software development lifecycle.**