# ADR-[NUMBER]: [Descriptive Decision Title]

<!--
================================================================================
USAGE INSTRUCTIONS
================================================================================
1. Copy this template to a new file: NNNN-descriptive-title.md
2. Replace [NUMBER] with the next sequential number (e.g., 0001, 0002)
3. Complete all sections following the guidance in brackets
4. Remove instructional comments after completion
5. Submit for review via Pull Request per governance process
================================================================================
-->

---

## Metadata

| Field               | Value                                                                |
|---------------------|----------------------------------------------------------------------|
| **Status**          | [Proposed \| Accepted \| Superseded \| Discontinued \| Rejected]     |
| **Created**         | [YYYY-MM-DD]                                                         |
| **Last Updated**    | [YYYY-MM-DD]                                                         |
| **Supersedes**      | [Link to previous ADR, if applicable, or "N/A"]                      |
| **Superseded By**   | [Link to successor ADR, if applicable, or "N/A"]                     |

> **⚠️ Immutable Record**: This ADR is an immutable historical record. If the decision changes in the future, a new ADR must be created, referencing this document as **Superseded**.

---

## Stakeholders

| Role               | Name / Team                                                           |
|--------------------|-----------------------------------------------------------------------|
| **Decision Maker** | [Name of the individual with final approval authority]                |
| **Contributors**   | [Names or teams that contributed to the analysis and elaboration]     |
| **Reviewers**      | [Names or teams responsible for technical review and validation]      |

---

## Context

### Business Context

[Describe the business scenario that motivated this decision. Include:

- Related strategic or operational objectives
- Stakeholder requirements and expectations
- Applicable regulatory, contractual, or compliance constraints
- Expected impact on products, customers, or revenue
- Business assumptions made for this analysis]

### Technical Context

[Describe the current technical scenario that underpins this decision. Include:

- Current state of the architecture or existing solution
- Technical limitations or identified technical debt
- Events or changes that triggered the need for a decision
- Technical dependencies and relevant integrations
- Technical assumptions made for this analysis]

---

## Problem Statement

[Define clearly and objectively the problem or challenge this decision intends to solve. Be specific and measurable whenever possible. The problem must be understandable by any technical member of the organization, regardless of project context.]

---

## Decision Drivers

[List the main factors that influence and drive this decision. Prioritize according to relevance to the organization. The final decision must be clearly linked to these drivers.]

| # | Driver | Description | Weight |
|---|--------|-------------|--------|
| 1 | [Driver Name] | [Description of the factor and its importance] | [High \| Medium \| Low] |
| 2 | [Driver Name] | [Description of the factor and its importance] | [High \| Medium \| Low] |
| 3 | [Driver Name] | [Description of the factor and its importance] | [High \| Medium \| Low] |
| N | [Driver Name] | [Description of the factor and its importance] | [High \| Medium \| Low] |

<!--
Common driver examples:
- Scalability and performance
- Implementation and maintenance cost (TCO)
- Time-to-market
- Regulatory compliance (GDPR, SOX, PCI-DSS)
- Developer experience (DX)
- Skill availability within the team
- Integration with existing systems
- Security and data privacy
- Resilience and availability
- Observability and operability
-->

---

## Options Considered

### Option 1: [Option Name]

[Detailed description of the option, including technical approach, technologies involved, and implementation model.]

| Pros | Cons |
|------|------|
| [Advantage 1] | [Disadvantage 1] |
| [Advantage 2] | [Disadvantage 2] |
| [Advantage N] | [Disadvantage N] |

| Aspect | Assessment |
|--------|------------|
| **Estimated Effort** | [1–2 weeks \| 1 month \| 3 months \| >3 months] |
| **Technical Risk** | [Low \| Medium \| High \| Critical] |
| **Driver Alignment** | [Low \| Medium \| High] |

---

### Option 2: [Option Name]

[Detailed description of the option, including technical approach, technologies involved, and implementation model.]

| Pros | Cons |
|------|------|
| [Advantage 1] | [Disadvantage 1] |
| [Advantage 2] | [Disadvantage 2] |
| [Advantage N] | [Disadvantage N] |

| Aspect | Assessment |
|--------|------------|
| **Estimated Effort** | [1–2 weeks \| 1 month \| 3 months \| >3 months] |
| **Technical Risk** | [Low \| Medium \| High \| Critical] |
| **Driver Alignment** | [Low \| Medium \| High] |

---

### Option 3: [Option Name]

[Detailed description of the option, including technical approach, technologies involved, and implementation model.]

| Pros | Cons |
|------|------|
| [Advantage 1] | [Disadvantage 1] |
| [Advantage 2] | [Disadvantage 2] |
| [Advantage N] | [Disadvantage N] |

| Aspect | Assessment |
|--------|------------|
| **Estimated Effort** | [1–2 weeks \| 1 month \| 3 months \| >3 months] |
| **Technical Risk** | [Low \| Medium \| High \| Critical] |
| **Driver Alignment** | [Low \| Medium \| High] |

<!-- Add more options as needed, following the same format -->

---

## Decision

**Selected Option**: [Name of the Chosen Option]

### Rationale

[Justify the selection of the chosen option, explicitly linking to the identified Decision Drivers. Explain why this option was considered superior to the alternatives. Be objective and base the argument on technical and business criteria.]

| Driver | How the Decision Addresses It |
|--------|------------------------------|
| [Driver 1] | [Explanation of how the chosen option satisfies this driver] |
| [Driver 2] | [Explanation of how the chosen option satisfies this driver] |
| [Driver N] | [Explanation of how the chosen option satisfies this driver] |

---

## Consequences

### Positive Consequences

- [Expected benefit 1 from implementing this decision]
- [Expected benefit 2 from implementing this decision]
- [Expected benefit N from implementing this decision]

### Negative Consequences

- [Accepted negative impact 1 as part of this decision]
- [Accepted negative impact 2 as part of this decision]
- [Accepted negative impact N as part of this decision]

### Identified Risks

| Risk | Probability | Impact | Severity | Mitigation |
|------|-------------|--------|----------|------------|
| [Risk description 1] | [Low \| Medium \| High] | [Low \| Medium \| High] | [P×I] | [Mitigation strategy] |
| [Risk description 2] | [Low \| Medium \| High] | [Low \| Medium \| High] | [P×I] | [Mitigation strategy] |
| [Risk description N] | [Low \| Medium \| High] | [Low \| Medium \| High] | [P×I] | [Mitigation strategy] |

---

## Impacts

### Technical Impacts

| Area | Impact Description |
|------|-------------------|
| **Architecture** | [Describe changes to system architecture, components, or integrations] |
| **Infrastructure** | [Describe changes to servers, cloud, networks, or environments] |
| **Code** | [Describe changes to codebases, libraries, or dependencies] |
| **Data** | [Describe changes to data models, databases, or data flows] |
| **Security** | [Describe security implications, authentication, or authorization] |
| **Observability** | [Describe changes to logging, monitoring, or alerting] |

### Organizational Impacts

| Area | Impact Description |
|------|-------------------|
| **Affected Teams** | [List teams or areas impacted by this decision] |
| **Training** | [Describe training needs or new skill development requirements] |
| **Processes** | [Describe changes to processes, workflows, or ceremonies] |
| **Documentation** | [Describe needs for updating technical or business documentation] |
| **Communication** | [Describe the communication plan for stakeholders] |

---

## Trade-offs

[Explicitly list the trade-offs the organization is accepting by adopting this decision. Be transparent about what is being sacrificed in favor of other benefits.]

| What We Are Prioritizing | What We Are Giving Up | Justification |
|--------------------------|----------------------|---------------|
| [Priority 1] | [Sacrifice 1] | [Why this trade-off is acceptable] |
| [Priority 2] | [Sacrifice 2] | [Why this trade-off is acceptable] |
| [Priority N] | [Sacrifice N] | [Why this trade-off is acceptable] |

---

## Implementation Plan

### Implementation Phases

| Phase | Description | Owner | Estimated Duration | Deliverables |
|-------|-------------|-------|-------------------|--------------|
| 1 | [Description of phase 1 activities] | [Team/Person] | [1–2 weeks \| 1 month \| etc.] | [Artifacts delivered] |
| 2 | [Description of phase 2 activities] | [Team/Person] | [1–2 weeks \| 1 month \| etc.] | [Artifacts delivered] |
| N | [Description of phase N activities] | [Team/Person] | [1–2 weeks \| 1 month \| etc.] | [Artifacts delivered] |

### Dependencies

| Dependency | Description | Status | Owner |
|------------|-------------|--------|-------|
| [Dependency 1] | [Description] | [Pending \| In Progress \| Completed] | [Owner] |
| [Dependency 2] | [Description] | [Pending \| In Progress \| Completed] | [Owner] |
| [Dependency N] | [Description] | [Pending \| In Progress \| Completed] | [Owner] |

### Rollback Plan

[Describe the rollback plan in case the implementation encounters critical issues.]

**Rollback Trigger Criteria**:

- [Criterion 1 indicating the need for rollback]
- [Criterion 2 indicating the need for rollback]

**Execution Steps**:

1. [Rollback step 1]
2. [Rollback step 2]
3. [Rollback step N]

**Estimated Rollback Time**: [Duration]

---

## Success Criteria

[Define objective and measurable metrics that will indicate whether the decision was successful after implementation.]

| Criterion | Metric | Current Baseline | Target | Evaluation Timeframe |
|-----------|--------|------------------|--------|---------------------|
| [Criterion 1] | [How it will be measured] | [Current value] | [Target value] | [When it will be evaluated] |
| [Criterion 2] | [How it will be measured] | [Current value] | [Target value] | [When it will be evaluated] |
| [Criterion N] | [How it will be measured] | [Current value] | [Target value] | [When it will be evaluated] |

---

## References

[List all sources, documents, articles, RFCs, or other ADRs that support or complement this decision.]

- [Reference Title 1](URL or document path)
- [Reference Title 2](URL or document path)
- [Reference Title N](URL or document path)

### Related ADRs

| ADR | Title | Relationship |
|-----|-------|--------------|
| [ADR-XXXX](link) | [ADR Title] | [Supersedes \| Complements \| Depends On] |
| [ADR-YYYY](link) | [ADR Title] | [Supersedes \| Complements \| Depends On] |

---

## Revision History

| Version | Date | Author | Change Description |
|---------|------|--------|-------------------|
| 1.0 | [YYYY-MM-DD] | [Name] | Initial version |
| 1.1 | [YYYY-MM-DD] | [Name] | [Change description] |

---

## Validation Checklist

<!--
Remove this checklist after completion and full validation of the ADR.
-->

- [ ] All required sections have been completed
- [ ] The problem statement is clearly defined and understandable
- [ ] Decision drivers are prioritized with weights defined
- [ ] At least 2 options were considered with pros and cons
- [ ] The decision rationale is linked to the drivers
- [ ] Risks have been identified with severity and mitigation plans
- [ ] Trade-offs are explicit and justified
- [ ] The implementation plan is feasible with assigned owners
- [ ] The rollback plan is documented
- [ ] Success criteria are measurable with baselines
- [ ] Relevant stakeholders have been included as reviewers
- [ ] The document has been reviewed by at least one technical peer
