# JTBD and Prioritisation Template

Use this template after reviewing the stakeholder notes.

## Step 1: Group the evidence

<!-- 
Suggested theme labels:
- duplicate work
- missed follow-up
- poor visibility
- customer friction
- financial credibility
- change resistance 
-->

## Step 2: Build an evidence table

| Stakeholder | Quote or observation | Theme | Business impact | Confidence |
|---|---|---|---|---|
| Christopher Richards, Collections Agent | *"The collections database does not sync with the email tracker, so agents often re-contact customers who were already promised callbacks."* | Duplicated work | Wasted agent attention and increased re-contact rate | High |
| Lawrence Bennett, Finance Analyst | *"Cases sit in “awaiting callback” status for months because the promised date was never recorded."* | Delayed or missed follow-up | Recovery opportunities are missed | High |
| Compliance Liaison | *"A case marked “resolved” in one system might be “in progress” in another."* | Poor account-status visibility | Weak control over case progression | High |
| Robert Quinn, Process Improvement Lead | *"Customers get transferred between departments and have to repeat their entire situation each time."* | Customer friction | Lower trust from customers and more repeat contacts | Medium |
| Daniel Farmer, Finance Analyst | *"The finance team cannot forecast recovery revenue because they do not trust the activity data."* | Lack of confidence in the numbers | Unreliable reporting and forecasting | Medium |
| Thomas Wright, Operations Manager | *"Agents are afraid to try new things because they were burned by the last system update."* | Change resistance or distrust | Lower adoption risk | Medium |


## Step 3: Write JTBD statements

<!-- 
Use the structure:

**When** ...  
**I want to** ...  
**So that** ...

Minimum coverage:
- customer
- agent
- operations manager
- finance partner 

## JTBD table
-->

| JTBD ID | Actor | Statement | Evidence link | Portal relevance | Priority |
|---|---|---|---|---|---|
| JTBD-01 | Customer | "When I want to resolve my debt, I want to understand what I owe and what options are available, so that I can make informed decisions about it." | SN-065 | High | High |
| JTBD-02 | Customer | "When I interact with the debt recovery process, I want to track progress and prior communications, so that I do not have to repeat information or chase updates." | SN-047 | High | High |
| JTBD-03 | Agent | "When handling a case, I want all relevant information available in one place, so that I can resolve issues without searching across systems. " | SN-087 | Medium | High |
| JTBD-04 | Agent | "When progressing a case, I want confidence that previous actions have already been completed, so that I do not risk duplicating work. " | SN-038 | Medium | High |
| JTBD-05 | Operations Manager | "When managing debt recovery operations, I want straightforward cases identified and prioritised appropriately, so that they are resolved quickly." | SN-003 | Medium | High |
| JTBD-06 | Operations Manager | "When overseeing performance, I want visibility of the pipeline and case progression, so that I can identify bottlenecks and intervene early." | SN-080 | Low | High |
| JTBD-07 | Finance partner | "When forecasting recovery revenue, I want reliable activity data, so that I can make accurate financial projections." | SN-070 | Low | Medium |
| JTBD-08 | Finance partner | "When reviewing operational performance, I want timely reporting, so that decisions are based on current information." | SN-048 | Low | Medium |
| JTBD-09 | Compliance liaison | "When evaluating automation opportunities, I want high-risk and specialist cases clearly identified, so that customers receive appropriate treatment and regulatory obligations are met." | SN-039 | High | High |
| JTBD-10 | Compliance liaison | "When overseeing debt recovery processes, I want systems to remain synchronised and auditable, so that customer information remains consistent across channels." | SN-062 | High | High |

<!-- SN-065: "Customers would pay more readily if they understood exactly what they owe and could see options." -->
<!-- SN-047: We are exposed to complaint risk because customers cannot track what we have told them. -->
<!-- SN-087: We are paying agents to hunt for information that should already be on the screen. -->
<!-- SN-038: The biggest win will be when agents stop checking whether work was already done. -->
<!-- SN-034: Agents are ready for better tools; they are tired of workarounds. -->
<!-- SN-003: Simple cases that could be resolved in minutes take days because they get stuck in the wrong queue. -->
<!-- SN-080: No one has visibility of what is actually in the pipeline or how long cases typically take. -->
<!-- SN-070: The finance team cannot forecast recovery revenue because they do not trust the activity data. -->
<!-- SN-048: Reporting takes so long that by the time we see the numbers, they are already out of date. -->
<!-- SN-039: We do not have a way to identify which cases are straightforward versus which require specialist handling. -->
<!-- SN-062: Every new tool we add makes the job harder because it adds another place where data can get out of sync. -->

## Step 4: Top 3 justification

For each of your top 3 JTBDs, write:
- why it matters now
- which evidence supports it
- how it should influence Phase 1

| JTBD | Why it matters now | Supporting evidence | Influence on Phase 1 |
|---|---|---|---|
| **JTBD-02**: "When I interact with the debt recovery process, I want to track progress and prior communications, so that I do not have to repeat information or chase updates." | Customers are less likely to abandon recovery journeys if there is clear evidence of case progression. | SN-047: "We are exposed to complaint risk because customers cannot track what we have told them." | Investigating how contacts are logged by agents to identify causes of duplicated work. |
| **JTBD-04**: "When progressing a case, I want confidence that previous actions have already been completed, so that I do not risk duplicating work." | Duplicate effort is a recurring operational issue that increases handling time and reduces capacity. | SN-038: "The biggest win will be when agents stop checking whether work was already done." | Investigate how actions, callbacks, and customer contacts are recorded. Identify where agents must manually verify activity and where duplicate work is generated. |
| **JTBD-09**: "When evaluating automation opportunities, I want high-risk and specialist cases clearly identified, so that customers receive appropriate treatment and regulatory obligations are met." | Defining appropriate boundaries between standard and specialist cases avoids dumping cases from the portal to agents. | "SN-039: “We do not have a way to identify which cases are straightforward versus which require specialist handling." | Identify how cases are currently categorised and prioritised. Determine whether reliable criteria exist to distinguish between standard and specialist cases.|

## Quality check

Ask yourself:
- Does this describe a need instead of a feature?
- Would the job still exist if the screen or tool changed?
- Can I point to real evidence behind the priority?
