© Crown Copyright (DCMS 2026) 

# Understanding the DSRF Data Model

## Data-sharing decisions for fast digital collaboration ##

The purpose of the Data-Sharing Risk Framework (DSRF) is to help organisations make data-sharing decisions that are explicit, consistent, non-arbitrary and ultimately automatable – enabling controlled but dynamic data exploitation at speed and scale. To do this, the DSRF separates the reusable structured logic of a decision from the administrative process used to approve it.

**Decision Records and Decision Patterns**

When an organisation uses the DSRF, two distinct outputs are produced.

*Decision Record*

A Decision Record (DR) captures the organisation-specific aspects of a decision, such as:
- business justification
- impact assessments
- approvals
- supporting evidence
- governance requirements
  
Different organisations may record different information in their Decision Records, and can design a variety of workflows or business processes to create and govern them.

*Decision Pattern*

A Decision Pattern (DP) contains the reusable policy logic that determines whether data-sharing (or data access) is allowed in a particular situation, based on the contemporary context. Decision Patterns take the same form wherever the DSRF is used, so there is compatibility across organisations and platforms with different local processes.

The Decision Pattern is the key reusable entity in the DSRF. It defines:
- the Scenario being assessed
- the associated Risk Profile
- the Risk Factors that apply
- whether those risks are tolerated or mitigated
- the Mitigations required
- the Control Objectives that must be achieved

A Scenario is a risk context defined in terms of Data, User, Environment and Purpose. It can be specific to one organisation’s data, or be agreed across multiple organisations. A Scenario can have many Decision Patterns over time as policy evolves, but only one Decision Pattern should be active for that Scenario at any one time, so there is no ambiguity in whether data can currently be accessed by a particular user or not.

**Not just a sharing agreement**

It is true that data-sharing between public bodies feels difficult because it takes a long time to create and sign off inter-agency agreements and MOUs. However, speeding up and streamlining the business process, to improve and increase point-to-point exchange or pooling of data, still won’t deliver a scalable data ecosystem. This is because there is no foundational, general body of knowledge about what makes it OK for certain data to be accessed under certain conditions.

*Lookup Error!*

In the UK and other jurisdictions, there is no codified body of regulation that sets out “the rules” for all kinds of data-sharing, nor is it possible to pre-empt all conceivable data-sharing scenarios and the non-compliance risks involved. Regulations that apply in different contexts are not necessarily integrated or consistent – there is always a historical patchwork of controls introduced for different purposes and at different times. 

This means we can’t rationalise data access by sorting entities into classes according to ontological relationships, i.e. kinds of things that are like other things – as a car, for example, is a type of vehicle. A rule which applies to one set of data might not apply to all of its sub-sets – rules or risks that apply to vehicles as a class might not apply to cars.

It is sometimes assumed that the DSRF is a taxonomy or classification framework for entities. In fact, the DSRF uses classifications, sets and hierarchies to describe risk relationships, not ontological ones. It helps organisations discover and learn about risk-alike categories that are often implicit, buried deep in rules and obligations.

The DSRF is concerned with whether sets behave similarly with respect to Impact, Compliance and Equity (ICE) risks within a particular Data, User, Environment and Purpose (DUE-P) context. A shared Risk-Relevant Characteristic (RRC) therefore represents a risk-equivalent set, not merely (or even necessarily) an ontologically related set. Organisations don’t generally know how to classify all their data into risk-alike sets until they have worked through the ICE risks that apply to different Scenarios, because superficial similarity of e.g. source, structure or content is not necessarily indicative of shared RRCs.

The aim of the DSRF is not to build an ontological classification of entities in the world. The aim of DSRF risk taxonomy is to identify the smallest number of categories needed to make explicit, consistent and non-arbitrary risk decisions about those entities in a scalable way.

**Sovereignty and confidence**

In an increasingly interconnected world, it is difficult to keep track of exactly what is happening to our data as it is shared, fused and consumed by AI models as well as people and databases. Traditional MOUs and agreements cover an act of sharing and stipulate onward use, but can’t keep pace with the mutation of data through a digital ecosystem – which leads to data not being shared at all, severe limits on its use, or, of course, to unmanaged risk.

By using the DSRF, organisations are building a model that identifies risk-based sets and the control objectives that apply to them, using the objective Risk-Relevant Characteristics that are observable in any current conditions. This means data owners can be more confident to share, knowing that their ICE risks can continue to be managed downstream of the original sharing decision, even as their data is fused and mutated into other products.

As agentic AI takes off, DSRF models can provide guardrails to shape how agents consume and use data across an ecosystem.

**Policy learning through machine reasoning**

The DSRF is not designed to allow data-sharing judgements to be made by machines, or without human intervention. But as the repository of approved Decision Patterns grows, it can become a collective policy-learning system. It would not merely answer whether sharing is permitted. It could explain why, show what would need to change, reveal where similar situations are treated differently, suggest where categories should be merged or differentiated, and help organisations learn from one another while preserving local authority. 

Insights from application of machine reasoning to the body of Decision Patterns could include:
- Detecting rules violations and semantic anomalies within an organisation’s decisions
- Suggesting candidate treatments and mitigations based on precedent
- Rationalising decision logic through merging and differentiating Decision Patterns, de-activating redundant Decision Patterns or disused Archetypes
- Answering operational questions such as “what is happening to my data?”, “what is being shared with these recipients?”
- Cross-organisational policy comparison – identify differences in risk appetite and treatment
- Counterfactual reasoning – what would need to change for sharing to become permissible?
- Dependency mapping – when a Decision Pattern changes, what is the impact on related DPs using the same components?
- Identifying emergent risks and concept drift

## Decision Patterns and architectural patterns ##

DSRF Decision Patterns provide Control Objectives for access, based on the RRCs of the Scenario. The framework doesn’t mandate how these Control Objectives should be fulfilled, i.e. how data architects choose to ensure that access is granted only in compliance with these conditions. It is likely though, that the best solutions will differ from traditional data access controls, and take advantage of data-centric approaches such as Zero Trust Architecture.

**Data labels and controls**

Traditionally, data labels state the conditions for access to the data. But the DSRF allows different access outcomes for the same data, depending on the risk context and varying over time. This suggests that access outcomes should be calculated from data labels, not imprinted on data labels. 

If access controls are carried directly on the data:
- Changes to control decisions require relabelling of the data
- Introducing conditional (if/then) access controls makes labels ‘heavy’
- There’s a risk of labels becoming inconsistent or out of date as policy changes are made

The DSRF doesn’t mandate any specific labelling approach, but it is designed to make access responsive to changing circumstances, enabling controlled data exploitation at speed and scale. This outcome is more difficult to achieve if data is labelled as though access outcomes are fixed at source. 

**Zero trust – separating the decision from the data**

Zero-trust principles move away from keeping data in secure containers (assuming that no containers are truly secure) and control access at the data level. In zero-trust architecture, there is a ‘policy decision point’ (PDP) which has the information to determine whether a given user can access certain data, and a ‘policy enforcement point’ (PEP) which implements the decision and gives or denies access.

DSRF Decision Patterns should be held away from the data, at the PDP. As Decision Patterns change, or conditions change, the PDP will make different determinations about data access without any relabelling of the data.

## Achieving data-sharing transformation ##
The DSRF therefore provides more than a faster route to approving individual sharing agreements. By separating local assurance from reusable Decision Patterns, it creates a structured body of risk knowledge that can be applied consistently as data, users, purposes and environments change. Its risk-based categories support policy learning without reducing nuanced judgements to a fixed taxonomy, while its Control Objectives can inform dynamic, zero-trust access decisions without binding policy to the data itself. Together, these features provide a foundation for organisations to retain authority over their decisions while collaborating more confidently, learning from precedent and managing data responsibly across an evolving digital ecosystem.

© Crown Copyright (DCMS 2026) 
