# Architecture Decision Records (ADR) Template

[![Validate ADRs](https://github.com/Rafazara/tech-architecture-adr/actions/workflows/adr-validation.yml/badge.svg)](https://github.com/Rafazara/tech-architecture-adr/actions/workflows/adr-validation.yml)

> A generic and reusable template for implementing Architecture Decision Records in technology organizations.

---

## About This Repository

This repository provides a **complete, ready-to-use template** for Architecture Decision Records (ADRs), designed to be adopted by any organization seeking to establish technical governance and structured documentation of architectural decisions.

### What Are ADRs?

Architecture Decision Records are documents that capture significant technical decisions along with their context, alternatives considered, and consequences. They serve as institutional memory, facilitate onboarding of new members, and promote transparency in architecture decisions.

### Why Use This Template?

| Benefit | Description |
|---------|-------------|
| **Ready to use** | Complete structure with template, examples, and automation |
| **Generic and neutral** | No dependencies on specific technologies or processes |
| **Standards-based** | Follows industry best practices (Michael Nygard, ThoughtWorks) |
| **Automated** | Includes CI workflow for ADR validation |
| **Documented** | Complete usage and contribution guides |

---

## Template Contents

This repository includes all artifacts needed to implement ADRs:

### Official Template

File `docs/adr/0000-template.md` with complete structure and explanatory comments for each section. Includes:

- Metadata and stakeholders
- Context, problem statement, and decision drivers
- Options considered with pros and cons
- Decision and rationale
- Consequences, impacts, and trade-offs
- Implementation plan and success criteria

### Meta-ADR

File `docs/adr/0001-adotar-adrs.md` serving as a real example that documents the decision to adopt ADRs itself. Can be adapted to each organization's reality.

### Index and Guide

File `docs/adr/README.md` with:

- Table of active ADRs
- Step-by-step guide for creating new ADRs
- Lifecycle and status explanation
- Best practices and conventions

### Validation Workflow

File `.github/workflows/adr-validation.yml` with GitHub Actions that:

- Runs automatically on Pull Requests
- Validates existence of numbered ADRs
- Checks basic structure (required sections)
- Provides clear feedback in case of errors

---

## Repository Structure

```text
tech-architecture-adr/
│
├── README.md                              # This file
│
├── .github/
│   └── workflows/
│       └── adr-validation.yml             # CI validation workflow
│
└── docs/
    └── adr/
        ├── README.md                      # ADR index and usage guide
        ├── 0000-template.md               # Official template for new ADRs
        ├── 0001-adotar-adrs.md            # Meta-ADR: decision to adopt ADRs
        └── superseded/                    # Superseded/discontinued ADRs
```

| Directory/File | Purpose |
|----------------|---------|
| `docs/adr/` | Main directory for active ADRs |
| `docs/adr/superseded/` | Archive for ADRs superseded by subsequent decisions |
| `.github/workflows/` | Validation automation via GitHub Actions |

---

## How to Use as a Template in Another Project

### Option 1: Use as GitHub Template

1. Click the **"Use this template"** button at the top of the repository
2. Define the name of the new repository
3. Clone the created repository
4. Customize according to the organization's needs

### Option 2: Copy Structure Manually

1. **Clone or download this repository**

   ```bash
   git clone https://github.com/Rafazara/tech-architecture-adr.git
   cd tech-architecture-adr
   ```

2. **Copy the structure to your project**

   ```bash
   # Copy the docs/adr folder to your repository
   cp -r docs/adr /path/to/your/project/docs/

   # Copy the validation workflow
   cp -r .github /path/to/your/project/
   ```

3. **Customize the Meta-ADR**
   - Edit `docs/adr/0001-adotar-adrs.md` to reflect your organization's context
   - Adjust stakeholders, dates, and implementation plan

4. **Configure the workflow** (if needed)
   - Adjust triggers or validations in `.github/workflows/adr-validation.yml`

### Option 3: Incorporate into Existing Monorepo

For existing repositories, add only the necessary files:

```bash
# Create directory structure
mkdir -p docs/adr/superseded
mkdir -p .github/workflows

# Download essential files
curl -o docs/adr/0000-template.md https://raw.githubusercontent.com/Rafazara/tech-architecture-adr/main/docs/adr/0000-template.md
curl -o docs/adr/README.md https://raw.githubusercontent.com/Rafazara/tech-architecture-adr/main/docs/adr/README.md
curl -o .github/workflows/adr-validation.yml https://raw.githubusercontent.com/Rafazara/tech-architecture-adr/main/.github/workflows/adr-validation.yml
```

---

## First Steps After Adoption

1. **Review the template** (`docs/adr/0000-template.md`) and adjust if needed for the organization's context

2. **Adapt the Meta-ADR** (`docs/adr/0001-adotar-adrs.md`) with specific information:
   - Actual stakeholders
   - Current organizational context
   - Adjusted implementation plan

3. **Communicate the new process** to technical teams

4. **Start documenting** architectural decisions following the template

---

## Contributing

Contributions are welcome! To suggest improvements:

1. Open an issue describing the suggestion
2. Or submit a Pull Request with the proposed changes

---

## References

- [Documenting Architecture Decisions - Michael Nygard](https://cognitect.com/blog/2011/11/15/documenting-architecture-decisions)
- [ADR GitHub Organization](https://adr.github.io/)
- [Lightweight Architecture Decision Records - ThoughtWorks Tech Radar](https://www.thoughtworks.com/radar/techniques/lightweight-architecture-decision-records)

---

## License

This template is made available for free use. Adapt according to your organization's licensing policies.
