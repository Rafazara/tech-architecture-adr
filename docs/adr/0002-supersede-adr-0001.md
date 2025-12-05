# ADR-0002: Supersede ADR-0001 (Portuguese Legacy ADR)

> **Supersession ADR**: This document formally supersedes ADR-0001 (Portuguese version) and establishes the canonical English ADR framework.

---

## Metadata

| Field | Value |
|-------|-------|
| **ADR ID** | ADR-0002 |
| **Title** | Supersede ADR-0001 (Portuguese Legacy ADR) |
| **Status** | `Accepted` |
| **Date** | 2025-12-05 |
| **Author** | Architecture Governance Team |
| **Supersedes** | ADR-0001 |

### Extended Metadata

| Field | Value |
|-------|-------|
| **Decision Scope** | Organization-Wide |
| **Reviewer(s)** | Engineering Leadership |
| **Approver(s)** | Architecture Governance Team |
| **Tags** | `governance`, `supersession`, `internationalization`, `meta-adr` |

---

## Stakeholders

| Role | Stakeholder | Interest / Concern |
|------|-------------|--------------------|
| **Decision Maker** | Architecture Governance Team | Framework standardization |
| **Accountable** | Architecture Governance Team | ADR governance compliance |
| **Consulted** | Engineering Leadership | Global team alignment |
| **Informed** | All Engineering Teams | Process awareness |

---

## Context

### Background

The original ADR-0001 (`0001-adotar-adrs.md`) was authored in Portuguese as the foundational meta-ADR establishing the ADR framework for the organization. This decision was appropriate for the initial team composition and regional context.

### Current Situation

As the organization scales globally and adopts English as the standard language for technical documentation, the Portuguese ADR creates:

1. **Accessibility Barriers**: Non-Portuguese-speaking engineers cannot easily understand the foundational governance document.
2. **CI/CD Validation Conflicts**: The enterprise validation workflow expects English section headers.
3. **Documentation Inconsistency**: All subsequent ADRs are in English, creating fragmentation.
4. **Governance Compliance Gap**: International audit and compliance reviews require English documentation.

### Immutability Constraint

Per ADR governance principles, accepted ADRs are **immutable**. The original Portuguese ADR-0001 cannot be modified or deleted. Instead, it must be formally superseded by a new ADR.

---

## Problem Statement

> **How do we transition from the Portuguese legacy ADR-0001 to a canonical English ADR framework while maintaining governance integrity and immutability compliance?**

### Sub-Problems

1. How do we preserve the historical record of the original decision?
2. How do we ensure CI validation passes with English section headers?
3. How do we maintain audit trail integrity during the transition?

---

## Decision Drivers

| # | Driver | Weight | Rationale |
|---|--------|--------|-----------|
| 1 | **Immutability Compliance** | Critical | Must not violate ADR governance rules |
| 2 | **Global Accessibility** | High | English as standard technical language |
| 3 | **CI/CD Compatibility** | High | Validation workflow requires English headers |
| 4 | **Audit Trail Integrity** | High | Preserve complete decision history |
| 5 | **Documentation Consistency** | Medium | All ADRs should follow same language standard |

---

## Options Considered

### Option 0: Status Quo (Keep Portuguese ADR)

**Description**: Maintain the original Portuguese ADR-0001 as the canonical meta-ADR.

| Dimension | Assessment |
|-----------|------------|
| **Pros** | No changes required; preserves original document |
| **Cons** | Accessibility barriers; CI validation failures; inconsistent documentation |
| **Risk Level** | High (blocks global adoption) |

**Verdict**: ❌ Rejected. Incompatible with global scaling and CI requirements.

---

### Option 1: Modify Original ADR (Translate In-Place)

**Description**: Translate the Portuguese ADR-0001 to English directly.

| Dimension | Assessment |
|-----------|------------|
| **Pros** | Simple; single document |
| **Cons** | **Violates immutability principle**; destroys audit trail |
| **Risk Level** | Critical (governance violation) |

**Verdict**: ❌ Rejected. Violates core ADR governance principle.

---

### Option 2: Formal Supersession (Create New English ADR)

**Description**: Create a new ADR that formally supersedes the Portuguese original, establishing the English version as canonical.

| Dimension | Assessment |
|-----------|------------|
| **Pros** | Preserves immutability; maintains audit trail; enables CI compliance |
| **Cons** | Additional document; requires clear supersession reference |
| **Risk Level** | Low (follows governance best practices) |

**Verdict**: ✅ Selected. Proper governance-compliant approach.

---

## Decision

### Selected Option: Option 2 — Formal Supersession

We formally supersede ADR-0001 (`0001-adotar-adrs.md`) with this ADR (ADR-0002) and establish the English ADR framework (`0001-adopt-adrs.md`) as the canonical meta-ADR.

### Decision Statement

> **The original Portuguese ADR-0001 is hereby superseded. The English ADR `0001-adopt-adrs.md` becomes the canonical foundational ADR for the organization's Architecture Decision Records framework.**

### Implementation Actions

| Action | Description |
|--------|-------------|
| **Archive Original** | Move `0001-adotar-adrs.md` to `docs/adr/superseded/` |
| **Update Status** | Mark original as `Superseded` with reference to ADR-0002 |
| **Establish Canonical** | `0001-adopt-adrs.md` serves as the authoritative meta-ADR |
| **Update Index** | Reflect supersession in `docs/adr/README.md` |

---

## Consequences

### Positive Consequences

| Outcome | Impact |
|---------|--------|
| **Global Accessibility** | All engineers can read foundational ADR |
| **CI/CD Compliance** | Validation workflow passes successfully |
| **Documentation Consistency** | Unified English documentation standard |
| **Audit Trail Preserved** | Original Portuguese ADR archived, not deleted |
| **Governance Integrity** | Immutability principle upheld |

### Negative Consequences

| Outcome | Mitigation |
|---------|------------|
| **Additional Document** | Clear supersession chain documented |
| **Historical Fragmentation** | Original preserved in `superseded/` folder |

### Neutral Consequences

| Outcome | Observation |
|---------|-------------|
| **Precedent Set** | Establishes pattern for future ADR supersessions |

---

## Impacts

### Technical Impacts

| Area | Impact | Severity |
|------|--------|----------|
| **CI/CD Pipeline** | Validation now passes | Positive |
| **Repository Structure** | New `superseded/` folder usage | Low |
| **Documentation Index** | Updated to reflect supersession | Low |

### Organizational Impacts

| Area | Impact | Severity |
|------|--------|----------|
| **Global Teams** | Improved accessibility | Positive |
| **Compliance** | English documentation for audits | Positive |
| **Governance** | Immutability principle reinforced | Positive |

---

## Trade-offs

| Trade-off | Accepted Compromise | Justification |
|-----------|---------------------|---------------|
| **Simplicity vs. Governance** | Additional supersession ADR | Governance compliance outweighs simplicity |
| **Single Source vs. History** | Two ADR files for same decision | Audit trail integrity required |
| **Convenience vs. Process** | Formal supersession workflow | Establishes correct precedent |

---

## Implementation Plan

### Phase 1: Immediate (This PR)

| Task | Owner | Deliverable |
|------|-------|-------------|
| Create ADR-0002 (this document) | Architecture Team | Supersession ADR |
| Move `0001-adotar-adrs.md` to `superseded/` | Architecture Team | Archived original |
| Ensure `0001-adopt-adrs.md` is canonical | Architecture Team | English meta-ADR |
| Update README index | Architecture Team | Reflected supersession |

### Phase 2: Validation

| Task | Owner | Deliverable |
|------|-------|-------------|
| CI validation passes | CI/CD | Green build |
| Immutability check passes | CI/CD | Zero violations |

---

## Success Criteria

| Metric | Target | Measurement |
|--------|--------|-------------|
| **CI Validation** | All checks pass | GitHub Actions |
| **Immutability Check** | Zero violations | Workflow output |
| **Documentation Accessibility** | 100% English | Manual review |
| **Audit Trail** | Complete history preserved | Git history + superseded folder |

---

## References

1. **ADR-0001 (Original)**: `docs/adr/superseded/0001-adotar-adrs.md`
2. **ADR-0001 (Canonical)**: `docs/adr/0001-adopt-adrs.md`
3. **Michael Nygard ADR Standard**: https://cognitect.com/blog/2011/11/15/documenting-architecture-decisions
4. **ADR Governance Principles**: Immutability, Traceability, Supersession

---

## Changelog

| Date | Author | Change |
|------|--------|--------|
| 2025-12-05 | Architecture Governance Team | ADR created to supersede Portuguese ADR-0001 |

---

*This ADR formally supersedes the original Portuguese ADR-0001 and establishes the English ADR framework as canonical.*
