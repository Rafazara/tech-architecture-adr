# Architecture Decision Records (ADRs)

## What Are ADRs?

Architecture Decision Records (ADRs) are documents that capture important architectural decisions along with their context and consequences. Each ADR describes a significant technical decision, the alternatives considered, the rationale for the choice, and the expected impacts.

The concept was introduced by Michael Nygard and has become a widely adopted practice in the software industry for establishing technical governance and preserving institutional memory.

## Why Do We Use ADRs?

The adoption of ADRs as the organization's official standard aims to solve common challenges in engineering teams:

| Challenge | How ADRs Help |
|-----------|---------------|
| **Decisions lost in chats and meetings** | Formal and persistent record in versioned repository |
| **Lack of institutional memory** | Queryable history independent of personnel turnover |
| **Slow onboarding** | New members understand the "why" behind decisions quickly |
| **Inconsistent decisions** | Standardized process promotes structured analysis |
| **Audit difficulties** | Complete traceability with Git (author, date, revisions) |

---

## Directory Structure

```
docs/adr/
├── README.md                 # This file - index and usage guide
├── 0000-template.md          # Official template for new ADRs
├── 0001-*.md                 # Active ADRs (sequential numbering)
├── 0002-*.md
├── ...
└── superseded/               # Superseded or discontinued ADRs
    ├── 0003-*.md
    └── ...
```

| Directory/File | Description |
|----------------|-------------|
| `docs/adr/` | Main directory containing all active ADRs |
| `0000-template.md` | Official template - copy this file to create new ADRs |
| `NNNN-title.md` | Individual ADRs with 4-digit sequential numbering |
| `superseded/` | ADRs that have been superseded by more recent decisions |

---

## Active ADRs

| Number | Title | Date | Status |
|--------|-------|------|--------|
| [0001](0001-adotar-adrs.md) | Adopt Architecture Decision Records | 2025-12-04 | Accepted |

---

## How to Create a New ADR

### Step 1: Assess the Need

Before creating an ADR, evaluate whether the decision meets the criteria:

- [ ] Impacts the architecture of one or more systems
- [ ] Affects multiple teams or components
- [ ] Is difficult to reverse after implementation
- [ ] Involves significant trade-offs
- [ ] Establishes a technical standard or convention

> **Note**: Trivial or easily reversible decisions do not require an ADR.

### Step 2: Determine the Next Number

Check the last ADR created and use the next sequential number:

```bash
ls docs/adr/*.md | Sort-Object | Select-Object -Last 1
```

### Step 3: Create the File

Copy the template to a new file with the correct naming convention:

```bash
cp docs/adr/0000-template.md docs/adr/NNNN-descriptive-title.md
```

**Naming convention**:
- 4-digit numeric prefix (e.g., `0002`, `0015`, `0123`)
- Title in kebab-case (words separated by hyphens)
- `.md` extension
- Example: `0002-adopt-kubernetes-for-orchestration.md`

### Step 4: Complete the Content

Edit the file following the template guidelines:

1. Replace `[NUMBER]` with the ADR number
2. Complete all required sections
3. Remove instructional comments
4. Ensure the rationale is clear and objective

### Step 5: Submit for Review

Create a Pull Request with the new ADR:

```bash
git checkout -b adr/NNNN-descriptive-title
git add docs/adr/NNNN-descriptive-title.md
git commit -m "docs(adr): add ADR-NNNN - Decision Title"
git push origin adr/NNNN-descriptive-title
```

### Step 6: Review and Approval

- Add appropriate reviewers (Tech Leads, Architects, stakeholders)
- Respond to comments and iterate as needed
- After approval, merge to the main branch
- Update the Active ADRs table in this README

---

## The `superseded/` Directory

The `superseded/` directory stores ADRs that have been **superseded** by more recent decisions. This structure preserves the complete decision history while keeping the main directory focused on current decisions.

### When to Move an ADR to `superseded/`

An ADR should be moved to `superseded/` when:

1. **A new decision supersedes it**: A subsequent decision invalidates or significantly updates the original decision.

2. **The technology/approach was abandoned**: The organization decided to discontinue the technology or standard established in the ADR.

3. **The context changed drastically**: Business, regulatory, or technical changes rendered the decision obsolete.

### How to Supersede an ADR

1. **Create the new ADR** that supersedes the previous one, referencing it in the "Supersedes" section

2. **Update the original ADR**:
   - Change the status to `Superseded`
   - Fill in the "Superseded By" field with a link to the new ADR

3. **Move the file** to the `superseded/` directory:
   ```bash
   git mv docs/adr/0003-old-decision.md docs/adr/superseded/
   ```

4. **Update this README**:
   - Remove from the "Active ADRs" table
   - Optionally, add to a "Superseded ADRs" section

5. **Commit and Push**:
   ```bash
   git commit -m "docs(adr): supersede ADR-0003 with ADR-0010"
   git push
   ```

### Why We Preserve Superseded ADRs

- **Historical context**: Understand why decisions were made in the past
- **Organizational learning**: Avoid repeating mistakes or revisiting already-solved discussions
- **Audit**: Maintain complete trail for compliance and governance
- **Reference**: Superseded ADRs may still contain valuable insights

---

## ADR Lifecycle

```
┌─────────────┐     ┌─────────────┐     ┌─────────────┐
│  Proposed   │────▶│ In Review   │────▶│  Accepted   │
└─────────────┘     └─────────────┘     └──────┬──────┘
                                               │
                           ┌───────────────────┴───────────────────┐
                           │                                       │
                           ▼                                       ▼
                    ┌───────────────┐                       ┌─────────────┐
                    │ Discontinued  │                       │ Superseded  │
                    └───────────────┘                       └─────────────┘
                                                                   │
                                                                   ▼
                                                            ┌─────────────┐
                                                            │ superseded/ │
                                                            └─────────────┘
```

| Status | Description |
|--------|-------------|
| **Proposed** | ADR in preparation, not yet submitted for review |
| **In Review** | ADR in review process via Pull Request |
| **Accepted** | ADR approved and in effect |
| **Discontinued** | ADR still valid but not recommended for new projects |
| **Superseded** | ADR invalidated by a subsequent decision; moved to `superseded/` |

---

## Best Practices

### ✅ Do

- Write ADRs at the time of the decision, not after implementation
- Be objective and base arguments on technical evidence
- Document all options considered, even rejected ones
- Include negative consequences and trade-offs explicitly
- Reference previous ADRs when there is a relationship
- Keep the README updated with new ADRs

### ❌ Avoid

- Creating ADRs for trivial or easily reversible decisions
- Editing already-accepted ADRs (create a new one that supersedes)
- Omitting risks or negative consequences
- Using ambiguous language or undocumented jargon
- Leaving ADRs in "Proposed" status indefinitely

---

## References

- [Documenting Architecture Decisions - Michael Nygard](https://cognitect.com/blog/2011/11/15/documenting-architecture-decisions)
- [ADR GitHub Organization](https://adr.github.io/)
- [Architecture Decision Records in Action - InfoQ](https://www.infoq.com/articles/architecture-decision-records/)

---

## Contributing

To suggest improvements to this process or the ADR template, open an issue or submit a Pull Request with the proposed changes.
