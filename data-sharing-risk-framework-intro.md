# A Data-Sharing Risk Framework: share and protect your data at scale

**Be part of developing a new toolkit for fast, confident data-sharing**

National Security Digital Centre is working to support data interoperability across the UK NS community and beyond. We are inviting practitioners to use and further test the decision-making framework outlined below, in order to determine Best Current Practice, and to shape forthcoming guidance. 

**Decision-making and interoperability**

A critical element of interoperability is the way organisations make data-sharing decisions. This is for two reasons:

1) Data-sharing is often delayed or doesn’t happen because of the difficulty of making effective, compliant decisions at pace  
2) Data-sharing can’t be automated if data-sharing decisions aren’t structured and expressed in a way which can be translated into a common standard with shared meaning

The NSDC Data Interoperability Group (DIG) is developing a Data-Sharing Risk Framework (DSRF) as a toolkit which can be used to make decisions explicit, consistent and non-arbitrary. The outcome of using this method is a set of decisions expressed logically in terms of Risk-Relevant Characteristics (RRCs). Decisions like this are easily repeatable (can be made fast), and have a clear meaning which can be implemented in a range of ways – so data can be protected equivalently in many different environments, using different technical implementations.

The DSRF has certain core components, but can be applied in a range of ways. The NSDC is determining Best Current Practice (BCP) principles, which will be used to create guidance and a standardised toolkit that can be easily used by non-experts. This article describes the basic DSRF methodology. Data and policy practitioners in the NS community and beyond are invited to apply the DSRF approach to their data-sharing challenges as ‘early adopters’, and provide feedback to help the DIG produce simple and practical guidance for the wider community.

Further resources are available from the DIG. Please contact NSDC@dsit.gov.uk

© Crown Copyright (DSIT 2025\)  

# Data-Sharing Risk Framework: Overview

## What is a Data-Sharing Risk Framework (DSRF)?
A DSRF is a method to make sure your data-sharing decisions are explicit, consistent and non-arbitrary, so that your data can be widely usable while remaining compliant and under control. Structured, logical decisions related to facts about a data-sharing situation are also essential to automating access controls, and sharing data in complex environments.

## Who needs to use the Data-Sharing Risk Framework? 
You should use the DSRF if you are:

- A data-owner or custodian whose job includes making decisions about whether, and under what circumstances, your organisation will make its data available to others  
- A data-sharing practitioner who develops and applies data-sharing processes and agreements in your organisation  
- A data architect or technician who makes sure data controls and standards are available to implement and assure data-sharing decisions

## What risks does the DSRF manage?  
There is usually an established process or dedicated job roles for managing the risks that data-sharing decisions and controls might fail. These risks *to* the shared data are sometimes called ‘CIA’ risks – they include Confidentiality (making sure no-one has unauthorised access), Integrity (making sure the data doesn’t get corrupted) and Availability (making sure the authorised users can actually get the data). The DSRF methods can be applied to these or any other risks, but the framework is designed primarily for the risks *of* data-sharing, i.e. the reasons why controls are there in the first place. These are Impact, Compliance and Equity (ICE) risks:

- **Impact** risks cover the positive and negative consequences of sharing or not sharing, in terms of e.g. reputation, relationships and of course benefit – is this worth doing?

- **Compliance** risks relate to the rules and obligations that apply to the data, e.g. from legislation or commitments to partners – are we allowed to do this?

- **Equity** risks concern the protection of sources and capabilities, e.g. intellectual property or commercial sensitivities – if we do this, will we ever be able to do it again?

**ICE risks are often managed with case-by-case judgement**  
Usually, when a data-sharing request is received, a data-owner or organisation makes some decisions about what should happen to the data, and labels the data with some instructions. This process is simple to understand and gives clear outcomes. The instructions normally say that:

- A specific body of **data**, can be shared with  
- A specific **user** or recipient, in  
- A specific system or **environment**, for  
- A specific **purpose**

These features apply to all data-sharing situations, and can be abbreviated as **DUE-P** factors.

**Data governance principles require systematic ICE decisions**  
Decisions and policies don’t normally explain why or how the data-handling instructions manage the risks the data-owner is worried about – they just say whether the sharing is allowed in the circumstances that have been described. But if it isn’t made clear which risk the controls are managing and why, it damages our ability to share effectively across boundaries. This is because:

- We can’t tell others exactly what needs to happen to our data in environments with different controls and conditions  
- We might end up trying to handle the same data lots of different ways on the same platform, for no good reason. This gets complicated and expensive  
- It’s hard to explain what should happen to our data if things are different in the future, or when our data is used and changed by others

A lot of data-sharing organisations also find that case-by-case decision-making causes bottlenecks and delays. Decision-makers don’t feel confident that they are appropriately managing the risks, because the relationship between the risk and the outcome is not clear, and they need to be sure the data will be safe. It can take a very long time to get permission to share, and the opportunity to get value or impact from the data can be missed.

**The DSRF relates decisions clearly to ICE risks**  
To make sure data is findable, accessible, interoperable and reusable, data-handling instructions must be related to ICE risks in a way which is:

- Explicit – a decision must be designed to manage or mitigate specific risks  
- Consistent – in the exact same DUE-P situation, with the same risks, data-owners should make the same decisions  
- Non-arbitrary – decisions should be based on objective and accessible facts about the situation, not just whims or preferences

The DSRF approach is aligned with the Risk & Control Stack, which relates controls to risks via Control Objectives. Control Objectives set out what the risk-owner wants to achieve in a DUE-P situation, with regard to particular risks.

## How to build a DSRF

**1\. Specify your ICE risks**

For your organisation’s data, you might list the ICE risks that you are worried about. Here are some examples, but they will vary between organisations and sectors:

- **Impact risks:** reputational damage, unintended consequences by recipients, relationship damage, failure to inform  
- **Compliance risks:** Breach of data protection regulations, unauthorised sharing of another organisation’s data, breach of contract  
- **Equity risks:** Providing commercial advantage to others, loss of intellectual property

**2\. Identify your DUE-P Risk-Relevant Characteristics**

When you are asked to share data, what kind of data are you asked to share with what kind of user, into what kind of environment, for what kind of purpose? The DUE-P factors which make a difference to how the ICE risks show up are the Risk-Relevant Characteristics (RRCs). Each combination of DUE-P RRCs describes a unique **'Scenario'** which engages ICE risks in its own way. Here are some DUE-P factors which might differentiate RRCs, but they can vary between organisations and sectors:

- **Data:** degree of structure or certainty, level of detail or specificity, provenance or source  
- **User:** competence, in terms of data capability or legal responsibility  
- **Environment:** control of users or control of systems, e.g. security tiers  
- **Purpose:** for external expertise, collaboration, or providing advice

Describe your DUE-P Scenario in the terms you think are likely to be 'risk-relevant' for your circumstances - that is, important to the decision you are about to make.

**3\. Assess your ICE Risk Factors for this Scenario**

Consider the extent to which each of your specific ICE risks applies in this Scenario. As you do so, identify the particular factors that are present in this Scenario and that activate the risk - for example, if you have a Compliance risk of 'breach of contract', what is it specifically in this Scenario that would be a potential problem? Could the Scenario involve unapproved use of a commercial dataset? Or perhaps be contrary to terms & conditions? A lot of common ICE risk factors have already been identifed in the development of the DSRF, so you won't have to start from scratch. Is the likelihood and impact of this risk low or high? There might be business principles or top-level policies that help you decide whether to tolerate or mitigate it. Think about what would have to be different in the Scenario to bring the risk down to an acceptable level.

Not all ICE risk factors are relevant to every decision you make, but you should build and maintain the set of factors that affect your decisions across all your DUE-P Scenarios.

**4\. Set your Control Objectives**

If an ICE risk factor needs to be mitigated for your Scenario to be acceptable, the mitigation will involve modifying the DUE-P RRCs. In other words, to change (reduce) the risk, you will naturally have to change the characteristics of the data, the user, the environment or the purpose that are relevant to the risk. You might only need to modify one of the DUE-P factors, you might be able to achieve the risk-reduction by modifying a choice of factors (either the data or the user, for example), or you might need to modify more than one factor in combination. The DSRF has identified a number of common mitigations for DUE-P factors, and you can add more if needed.

For each mitigation, set out what is needed in practice to achieve it. If a risk factor could be mitigated by Users being skilled, for example, set out what skills you need them to have. If a risk factor could be mitigated by Data being sanitised, set out what kind of detail needs to be removed. These conditions are your DUE-P Control Objectives for the Scenario.

**5\. Express your data-sharing decisions in terms of RRCs and Control Objectives**

RRCs are the building blocks of explicit, consistent and non-arbitrary data-sharing decisions. Now, when you make a decision, you can express it in terms of what Control Objectives need to be met to allow a particular data-sharing Scenario, defined by its RRCs. This allows decision-making for situations that haven't happened yet, or which might change.  

As outlined above, traditional data-sharing decisions take the form that:

- A specific body of **data**, can be shared with  
- A specific **user** or recipient, in  
- A specific system or **environment**, for  
- A specific **purpose**

Permission to share any other body of data must be started from scratch, as a separate decision.

Using the DSRF, data-sharing decisions for a Scenario take the form that:

- **Data** with/without specified RRCs, can be shared with  
- **Users** (or entities) with/without specified RRCs, in  
- An **environment** with/without specified RRCs, for  
- A certain kind of **purpose**.

New requests to share can be tested against these criteria. If they meet them, the sharing is allowed without an additional decision. If they don’t, an assessment allows expansion of your DSRF to accommodate more Scenarios. Over time, the need for new decisions will become less and less as your risk framework is established.

**6\. Introducing Archetypes**

As you consider more Scenarios, you will likely find that there are clusters of common ICE factors that apply to certain DUE-P RRCs. If you have multiple Scenarios that require a particular Data Control Objective because of the same risk, you could identify broader categories of RRC that these Scenarios have in common. This allows you to develop a business principle that certain kinds of Scenario engage certain key risks, which might be tolerated, or mitigated in a particular way. These clusters of Scenarios with common risk profiles are called **'Archetypes'**.

Most organisations have a small number of common DUE-P Archetypes – usually fewer than 10. DUE-P Archetypes might correspond to different points in your data lifecycle, or different data products. This reduces the number of risk-management decisions you need to make, because Control Objectives can often apply at Archetype level, to any Scenario that fits the archetype. Over time, you can both aggregate Scenarios and group them into Archetypes, so that you end up with the minimum necessary number of explicit, consistent and non-arbitrary decisions across your whole organisation, and even across multiple organisations.

## How will this benefit me?  
Using the framework, you set the conditions for data access in terms of things that need to be true of the world for you to have managed specific risks. This means:

- Anyone can implement your decision accurately by making the same things true, even if they are using different mechanisms or controls  
- It’s easier to reach agreement on handling the same data the same way, by comparing risks and previous decisions. This makes data management simpler and cheaper  
- You can set conditions for access that apply in different circumstances, such as an emergency or when your data has been mixed with other people’s data. You won’t get asked to make new decisions every time.

A DSRF also helps organisations make decisions more quickly and confidently. Firstly, decision-makers can see how risks have been managed in similar situations previously, and focus on any important differences. 

Secondly, in traditional data-sharing, by saying ‘yes’ the decision-maker is affirming that ICE and other risks have definitely been managed when this data is shared with this user for this purpose. That feels like a big responsibility, and the decision-maker needs proof that everything is in place before they can say yes to sharing. Using the DSRF, the decision-maker is agreeing to share IF certain specific conditions are true – the decision-maker does not also have to show or guarantee that they are currently true. That shares the burden of responsibility and means that decision-making itself is not delayed by security or accreditation processes that can be done separately, or by others.

## How to put a DSRF into practice

**Data-sharing policies and processes**  
The DSRF toolkit gives you a way to express your decisions about data-sharing clearly and explicitly, in a way which others can understand even if they don’t have the same data-management systems and labels as you do. Using a DSRF, you can systematically:

* Describe your dataset or data product in terms of its RRCs  
* Describe your requirements for the recipient user and environment in terms of their RRCs  
* Use simple logic to state what needs to happen for different combinations of RRCs, or if the RRCs change

Of course, there is more to the process of data-sharing than the decisions themselves. Your organisation will have processes or policies for:

* Who is allowed to make the decision  
* What people should do to request or get a new data-sharing decision  
* Where and how the decision is recorded

You will also need to explain and communicate any new process you put in place to use the DSRF – but most people in your organisation won’t need to know all the details of your DUE-P Scenarios, or how many Archetypes you have created, for example. It might not be necessary or appropriate to share all the details of the ICE risk factors you are managing – you can protect the details if you need to.  You can adapt and implement the DSRF approach in whichever way is most appropriate for you.

**Making access happen**  
A DSRF helps you make more consistent decisions, more quickly, by mapping your decisions explicitly to risks via RRCs. It doesn’t force you to implement your decisions in any particular way. 

If you want to automate data-access, RRCs give you the kind of granular, objective information that you need for this. There are several ways you could do it, such as:

* A function to automatically translate RRC-based decisions into the controls or handling instructions that you or your customers already use and understand, such as classifications or the [Traffic Light Protocol](https://www.ncsc.gov.uk/collection/board-toolkit/principle-e-assurance-and-oversight/understanding-the-cyber-security-threat#section_3) (keeping the risk assessment for future reference).  
* Work with your customers to create improved handling instructions or tools that are better suited to the way you want your data to be treated – this might make it easier to ensure a good fit with your RRC-based decisions.  
* Directly represent some or all RRCs as attributes of data, users and environments for attribute-based access control – this gives maximum accuracy and flexibility, but it means more technical and business change up front.

If you’re not ready or able to automate data-access, you can manually convert your RRC-based decisions into the controls you already use. You might not get the full benefits of automation, in terms of speed or efficiency – but you will have much better information about why you made the decision. This means you can be more rigorous and consistent in your data-sharing, improve your data-sharing processes, and have the information you need to automate the sharing when you are ready.

