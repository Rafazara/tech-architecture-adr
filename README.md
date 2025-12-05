# Architecture Decision Records (ADR) Repository Template

[![ADR Validation](https://github.com/your-org/tech-architecture-adr/actions/workflows/adr-validation.yml/badge.svg)](https://github.com/your-org/tech-architecture-adr/actions/workflows/adr-validation.yml)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

> **Enterprise-Grade ADR Framework** — A production-ready template for implementing Architecture Decision Records following the Michael Nygard standard with Big Tech governance extensions.

---

## What is This Repository?

This repository provides a **complete, battle-tested framework** for implementing Architecture Decision Records (ADRs) in your organization. It includes:

- 📋 **Comprehensive ADR Template** — Enterprise-grade template with all necessary sections
- 📖 **Meta-ADR (ADR-0001)** — Documents the decision to adopt ADRs (use as reference)
- 📚 **Operational Guide** — Complete README with governance, workflow, and best practices
- ⚙️ **CI/CD Validation** — GitHub Actions workflow for automated compliance checking
- 🏗️ **Directory Structure** — Ready-to-use folder organization

---

## Quick Start

### Option 1: Use as GitHub Template

1. Click **"Use this template"** button on GitHub
2. Create your new repository
3. Customize the template for your organization

### Option 2: Clone and Adapt

```bash
# Clone the repository
git clone https://github.com/your-org/tech-architecture-adr.git my-adr-repo

# Navigate to the directory
cd my-adr-repo

# Remove Git history and initialize fresh
rm -rf .git
git init
git add .
git commit -m "Initial ADR repository setup"
```

### Option 3: Copy Individual Files

Copy only what you need into your existing repository's `docs/adr/` directory:

```bash
mkdir -p docs/adr
cp path/to/template/docs/adr/0000-template.md docs/adr/
cp path/to/template/docs/adr/README.md docs/adr/
```

---

## Repository Structure

```
.
├── README.md                           # This file
├── docs/
│   └── adr/
│       ├── README.md                   # ADR index and operational guide
│       ├── 0000-template.md            # Canonical ADR template
│       └── 0001-adopt-adrs.md          # Meta-ADR documenting ADR adoption
└── .github/
    └── workflows/
        └── adr-validation.yml          # CI/CD validation workflow
```

---

## Philosophy & Principles

### Why ADRs Matter

Traditional documentation answers **"what"** and **"how"**. ADRs answer **"why"**.

> "The decision itself is important, but the rationale and context that led to it are equally valuable—if not more so."
> — Michael Nygard

### Core Principles

| Principle | Description |
|-----------|-------------|
| **Immutability** | Accepted ADRs are never modified; changes require new ADRs |
| **Traceability** | Clear lineage from problem → decision → consequences |
| **Discoverability** | Engineers find relevant ADRs within 60 seconds |
| **Low Friction** | Creating an ADR takes < 30 minutes for simple decisions |
| **Version Control** | ADRs live with the code, reviewed via PRs |

### The Nygard Model

This framework implements the Michael Nygard ADR format (2011), enhanced with:

- **Enterprise metadata** (stakeholders, tags, decision scope)
- **Structured options analysis** (including Option 0: Status Quo)
- **Risk and impact assessment**
- **Implementation and rollback planning**
- **Success criteria with measurable outcomes**

---

## Who Is This For?

### Primary Audiences

| Role | Benefit |
|------|---------|
| **Software Architects** | Documented rationale for architectural decisions |
| **Engineering Managers** | Governance framework for technical decision-making |
| **Tech Leads** | Template for team-level technical documentation |
| **Platform Teams** | Standard for organization-wide technical standards |
| **New Hires** | Onboarding resource for understanding historical decisions |

### Organization Maturity

| Stage | Recommendation |
|-------|----------------|
| **Startup (< 20 engineers)** | Start with minimal ADRs; adopt full framework as you scale |
| **Growth (20-100 engineers)** | Implement full framework; critical for preserving institutional knowledge |
| **Enterprise (100+ engineers)** | Essential for governance, compliance, and architectural consistency |

---

## When to Use ADRs

### Create an ADR When...

✅ Adopting a new technology, framework, or platform
✅ Selecting an architectural pattern (microservices, event sourcing, etc.)
✅ Making breaking API changes
✅ Establishing security architecture decisions
✅ Defining data architecture or retention policies
✅ Choosing infrastructure approaches (cloud provider, Kubernetes, etc.)
✅ Deprecating or migrating away from existing technology

### Do NOT Create an ADR When...

❌ Fixing bugs
❌ Minor refactoring (unless it changes architecture)
❌ Routine dependency updates
❌ Configuration changes
❌ Easily reversible decisions

**Heuristic**: If you'll need to explain "why" to someone in 6 months, create an ADR.

---

## ADR Lifecycle

```
┌──────────┐    Approved    ┌──────────┐
│ Proposed │───────────────▶│ Accepted │
└──────────┘                └────┬─────┘
      │                          │
      │ Declined                 │ Replaced
      ▼                          ▼
┌──────────┐                ┌────────────┐
│ Rejected │                │ Superseded │
└──────────┘                └────────────┘
```

### Status Values

| Status | Meaning |
|--------|---------|
| **Proposed** | Under review; open for feedback |
| **Accepted** | Approved and in effect (**IMMUTABLE**) |
| **Superseded** | Replaced by newer ADR |
| **Discontinued** | No longer applicable |
| **Rejected** | Reviewed and declined |

### Immutability Rule

> **Once an ADR is Accepted, its content cannot be changed.**
> To modify a decision, create a new ADR that supersedes the original.

This ensures audit trail integrity and reference stability.

---

## Governance

### Decision Authority

| ADR Scope | Approver |
|-----------|----------|
| Organization-wide | CTO / VP Engineering / Architecture Owner |
| Team-wide | Tech Lead / Engineering Manager |
| Project-specific | Project Architect / Senior Engineer |

### Review Requirements

- **Minimum**: 1 technical reviewer
- **Recommended**: 2 reviewers for significant decisions
- **Required for org-wide**: Architecture review board or designated approver

### SLAs

| Stage | Target |
|-------|--------|
| Initial review | 48 hours |
| Feedback resolution | 72 hours |
| Final approval | 24 hours |

---

## CI/CD Validation

The included GitHub Actions workflow validates:

| Check | Description |
|-------|-------------|
| **Naming Convention** | Files follow `NNNN-descriptive-slug.md` format |
| **Required Sections** | Metadata, Context, Decision, Consequences present |
| **Metadata Completeness** | ADR ID, Status, Date, Author fields filled |
| **Status Values** | Only valid statuses (Proposed, Accepted, etc.) |
| **Immutability** | Accepted ADRs cannot be modified |
| **Supersession Chains** | References to superseded ADRs are valid |

### Workflow Location

```
.github/workflows/adr-validation.yml
```

### Customization

Modify the workflow to match your organization's requirements:

```yaml
# Adjust required sections
REQUIRED_SECTIONS=(
  "## Metadata"
  "## Context"
  "## Decision"
  "## Consequences"
)

# Add custom validations as needed
```

---

## Template Overview

The included template (`docs/adr/0000-template.md`) provides:

### Required Sections

| Section | Purpose |
|---------|---------|
| **Metadata** | ID, status, dates, stakeholders |
| **Context** | Business and technical background |
| **Problem Statement** | Clear articulation of the challenge |
| **Decision** | What was decided |
| **Consequences** | Positive, negative, and neutral outcomes |

### Optional Sections (Recommended)

| Section | Purpose |
|---------|---------|
| **Decision Drivers** | Prioritized criteria for evaluation |
| **Options Considered** | All alternatives including status quo |
| **Rationale** | Why this option was selected |
| **Risks & Mitigations** | Potential issues and how to address them |
| **Implementation Plan** | Phases and ownership |
| **Success Criteria** | Measurable outcomes |

### Enterprise Extensions

| Section | Purpose |
|---------|---------|
| **Decision Scope** | Team, Project, Organization-wide |
| **Stakeholder Matrix** | RACI-style responsibility assignment |
| **Rollback Plan** | How to reverse if needed |
| **Long-term Implications** | 2-5 year impact assessment |

---

## Tools & Resources

### Recommended Tools

| Tool | Purpose | Link |
|------|---------|------|
| **adr-tools** | CLI for ADR management | [GitHub](https://github.com/npryce/adr-tools) |
| **Log4brains** | ADR management with web UI | [GitHub](https://github.com/thomvaill/log4brains) |
| **VS Code** | Markdown editing with preview | [VS Code](https://code.visualstudio.com/) |

### References

1. **Michael Nygard** — [Documenting Architecture Decisions](https://cognitect.com/blog/2011/11/15/documenting-architecture-decisions)
2. **ThoughtWorks** — [Lightweight Architecture Decision Records](https://www.thoughtworks.com/radar/techniques/lightweight-architecture-decision-records)
3. **ADR GitHub Organization** — [adr.github.io](https://adr.github.io/)
4. **MADR Template** — [Markdown Any Decision Records](https://adr.github.io/madr/)

---

## Customization Guide

### Step 1: Organization Details

Update placeholders throughout:

```bash
# Replace organization references
find . -type f -name "*.md" -exec sed -i 's/your-org/my-company/g' {} \;
find . -type f -name "*.md" -exec sed -i 's/Architecture Governance Team/Your Team Name/g' {} \;
```

### Step 2: Template Sections

Review `docs/adr/0000-template.md` and adjust:

- Add organization-specific sections
- Remove sections that don't apply
- Modify examples to match your technology stack

### Step 3: Governance Rules

Update `docs/adr/README.md`:

- Define your approval matrix
- Set appropriate SLAs
- Customize review requirements

### Step 4: CI/CD Workflow

Modify `.github/workflows/adr-validation.yml`:

- Adjust required sections
- Add custom validations
- Configure notifications

---

## Contributing

Contributions to improve this template are welcome!

### How to Contribute

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

### Areas for Contribution

- Additional template sections
- Alternative CI/CD platforms (GitLab CI, Azure DevOps)
- Localization (translations)
- Tool integrations
- Documentation improvements

---

## License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.

---

## Acknowledgments

- **Michael Nygard** — Creator of the ADR concept and format
- **ThoughtWorks** — Popularizing ADRs through Technology Radar
- **ADR Community** — adr.github.io contributors
- **Industry Practitioners** — Engineers who have refined ADR practices

---

## Support

For questions or issues:

- 📖 Check the [FAQ](docs/adr/README.md#faq) in the operational guide
- 🐛 Open an [issue](https://github.com/your-org/tech-architecture-adr/issues) for bugs or suggestions
- 💬 Discuss in [Discussions](https://github.com/your-org/tech-architecture-adr/discussions)

---

*Built with ❤️ for engineering teams who value documented decisions.*
