© Crown Copyright (DCMS 2026) 

# The DSRF Data Model: Core Elements and Relationships # 
The Data-Sharing Risk Framework (DSRF) is designed to ensure that data-sharing decisions are **explicit, consistent and non-arbitrary**. The data model provides a common structure that can be applied in different organisations and business contexts while preserving the same decision-making logic.

The key principle is that **risks are assessed in the context of a complete data-sharing Scenario**, not in relation to individual characteristics in isolation.

The DSRF data model has specific core components:
- **Scenarios** describe combinations of Data, Users, Environments and Purposes.
- **RRCs** describe the characteristics that define those Scenarios.
- **Archetypes** group similar Scenarios through shared patterns of risk.
- **Risk Profiles** record the risks that apply in a particular context.
- **Risk Factors** identify the specific concerns behind those risks.
- **Mitigations** describe how those concerns can be managed.
- **Control Objectives** describe the outcomes that must be achieved.
- **Decision Patterns** combine these elements into a reusable decision.
- **Decision Records** provide the organisation-specific governance and audit trail.

Together, these concepts enable data-sharing decisions to be expressed in a form that is transparent, repeatable, interoperable and ultimately capable of supporting automation.

# The Core Structure #
At the centre of the DSRF model is the **Decision Pattern**.

A Decision Pattern is the reusable description of a data-sharing decision. It links together:

- a **Scenario**
- the associated **Risk Profile**
- the **Mitigations** required to manage risks
- the **Control Objectives** that must be achieved

A Decision Record may be linked to a Decision Pattern to capture organisation-specific approvals, justifications and governance information, but these are not part of the reusable policy enforcement logic.
 
<img width="973" height="225" alt="image" src="https://github.com/user-attachments/assets/f636354e-bc5d-4e6b-8146-0c20841e1fc2" />


### Scenarios

A **Scenario** represents a particular combination of:

- Data
- User
- Environment
- Purpose

(DUE-P).

A Scenario is defined by its **Definitive Risk-Relevant Characteristics (D-RRCs)**.

These D-RRCs identify the sets of Data, Users, Environments and Purposes that share common risk behaviour. The complete combination of D-RRCs uniquely defines the Scenario. 

*Constraint*

A Scenario must always be defined by a complete DUE-P combination.
Risk assessments must not be attached directly to individual D-RRCs.

### Risk-Relevant Characteristics (RRCs)

An **RRC** is a governed description of a real characteristic that may be relevant to data-sharing risk in some DUE-P context.

The DSRF distinguishes between:

**Definitive RRCs (D-RRCs)**
These define Scenarios and determine which Decision Pattern applies. 

**Macro RRCs**
These describe broader categories or supersets of D-RRCs and are used to define Archetypes. 

*Constraint*

An RRC does not itself determine risk.

The same RRC may be associated with different risks (or none) in different Scenarios.

### Archetypes

An **Archetype** groups together Scenarios (or potential Scenarios) that exhibit similar patterns of risk.

An Archetype consists of:

- a combination of Macro RRCs
- a partial Risk Profile
- associated mitigations

Archetypes are intended to promote consistency and reduce duplication of risk-assessment effort. 

*Constraint*

Archetypes provide guidance but do not constitute complete decisions.

A Scenario may belong to more than one Archetype provided the resulting risk profiles are compatible.

### Risk Profiles

A **Risk Profile** records the risks that are relevant in a particular context.

Two types are used:
	
- Partial Risk Profiles, associated with Archetypes
- Complete Risk Profiles, associated with Decision Patterns

Risk Profiles provide the link between Scenarios and the risk-management logic applied to them.

*Constraint*

Every active Decision Pattern must have exactly one complete Risk Profile, including the associated Mitigations and Control Objectives sufficient to determine data access.

### ICE Risks and Risk Factors

The DSRF identifies three categories of risk:

- Impact
- Compliance
- Equity
(ICE)

A **Risk Factor** is a specific concern that contributes to one or more ICE risks. Examples include the presence of specific contractual restrictions, sensitive information, or sub-optimal data quality.

Risk Factors belong to the Risk Profile of a Scenario. They are assessed as relevant or irrelevant and either tolerated or mitigated. 

*Critical Constraint*

Risk Factors apply to Scenarios, not to individual RRCs.

This is one of the most important rules in the DSRF methodology. Risk emerges from the combination of Data, User, Environment and Purpose characteristics, not from any single characteristic considered alone.

### Mitigations

A **Mitigation** is a change to one of the DUE-P dimensions intended to affect a Risk Factor.

Each Mitigation targets one of:
- Data
- User
- Environment
- Purpose

The same Mitigation may be used to manage multiple Risk Factors. Likewise, a Risk Factor may require multiple Mitigations. 

*Constraint*

Mitigations must be linked to specific Risk Factors through the Risk Profile rather than attached directly to Scenarios or RRCs.

### Control Objectives

A **Control Objective** describes the outcome that must be achieved for a Mitigation to be effective. In other words, a Mitigation describes what kind of change is required; a Control Objective describes what success looks like.

Control Objectives define what must be true, not how it is achieved. Different organisations may implement the same Control Objective in different ways. 

Control Objectives may also be decomposed into smaller component objectives.

*Constraint*

Every Mitigation used in an active Decision Pattern should be supported by one or more Control Objectives.

### Decision Patterns

The **Decision Pattern** is the key reusable policy object in the DSRF.

A Decision Pattern consists of:
- a Scenario
- a Complete Risk Profile
- the associated Mitigations
- the required Control Objectives

A Decision Pattern defines the conditions under which data-sharing may occur. 

*Constraints*

- A Scenario may have many Decision Patterns over time.
- Only one Decision Pattern may be active for a Scenario at any given point in time.
- Decision Patterns must remain traceable through versioning and supersession relationships. 

### Use Cases

A **Use Case** is a real example of Data, Users, Environments and Purposes that satisfies the D-RRC definitions of a Scenario, and which may therefore use the Decision Pattern.

Use Cases demonstrate how Decision Patterns are applied in practice. 

## DSRF layered logical model

The elements of the DSRF conceptual model and the relationships between them can be presented as a simplified Entity Relationship diagram.

<img width="978" height="547" alt="image" src="https://github.com/user-attachments/assets/a389234f-7dc7-4b81-8485-7beecfcf1b8e" />

## Notes on interpretation

### Taxonomy of risk-alike sets

In the DSRF, taxonomy serves risk management, not the other way around.

Traditional classification schemes focus on whether one thing is a subtype or subset of another. For example:
```
1     Long-haired dogs
2         ⊂
3     Long-haired animals
```
This relationship may be useful for organising information, but it does not automatically mean that the two categories should be treated the same way for data-sharing purposes.

A set described by an RRC remains valid only while its members can be treated as risk-alike. If a subset is found to exhibit different risk behaviour, that distinction becomes risk-relevant and should be reflected in the model through differentiation of the RRCs or Decision Patterns.

For example:
```
1     Long-haired animals
```
may initially be a valid D-RRC if data about all long-haired animals can be shared under the same conditions.
However, if the organisation discovers that:
```
1     Long-haired cats
```
represents data that can be shared in a particular Scenario while:
```
1     Long-haired dogs
```
does not, then "long-haired animals" is no longer a sufficiently precise risk category for that context.

The DSRF should then differentiate that category into more specific D-RRCs, and potentially treat the broader category as a Macro RRC if there remains a partial risk profile that can usefully be applied to all long-haired animals in certain DUE-P contexts. 

This principle underpins several aspects of the DSRF:

- Risk Factors apply to Scenarios, not to individual RRCs.
- D-RRCs are refined when they cease to represent risk-alike sets.
- Macro RRCs allow multiple D-RRCs with similar risk behaviour to be grouped together.
- Archetypes describe common risk patterns across groups of Scenarios.
- Decision Patterns are based on risk equivalence rather than taxonomic hierarchy.

## Lifecycle and traceability

The DSRF is designed to support continuous policy evolution.

As organisations develop new Scenarios and gain experience from real-world use cases, they may:

- create new Decision Patterns
- revise existing Decision Patterns
- merge similar Decision Patterns
- split overly broad Decision Patterns
- refine Archetypes
- update RRC definitions
- extend Risk Factor libraries

For this reason, key entities within the model support lifecycle management, including:

- versioning
- validity periods
- supersession relationships
- historical traceability

This ensures that organisations can understand not only what a decision is today, but also how and why it has changed over time.

## Essential DSRF Integrity Rules

To ensure that the DSRF methodology is being applied correctly, the following rules must always be maintained:
1.	A Scenario is defined by a complete combination of D-RRCs across DUE-P.
2.	Risk Factors apply to Scenarios, not to individual RRCs.
3.	Every active Decision Pattern must have exactly one complete Risk Profile.
4.	Only one Decision Pattern may be active for a Scenario at any point in time.
5.	Archetypes contain partial Risk Profiles and do not constitute Decision Patterns (if an Archetype’s Risk Profile is complete, it thereby becomes a Decision Pattern)
6.	Mitigations target DUE-P dimensions and are linked to Risk Factors via the Risk Profile.
7.	Control Objectives define outcomes, not implementation methods.
8.	Decision Patterns, RRCs, Risk Factors and Control Objectives must be versioned and traceable over time.
9.	Scenarios may belong to multiple Archetypes only if the resulting risk profiles are compatible.
10.	Decision Records are separate from Decision Patterns and may vary between organisations. 
11.	D-RRCs represent risk-equivalent sets, not merely taxonomic sets.
12.	Taxonomic relationships do not imply Decision Pattern inheritance.

In summary, the DSRF data model ensures that data-sharing decisions are based on the risks that arise in a complete DUE-P Scenario, expressed through reusable Decision Patterns, and governed through explicit relationships between Risk Profiles, Risk Factors, Mitigations and Control Objectives. This structure allows different organisations to implement the framework in their own way while preserving consistent decision-making logic. 

© Crown Copyright (DCMS 2026) 
