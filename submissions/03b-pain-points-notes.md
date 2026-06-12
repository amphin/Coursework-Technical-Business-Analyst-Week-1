## Pain points

| Pain point ID | Process | Evidence source | Note |
|---|---|---|---|
| PP-01 | Agent picks up delinquent case | SN-053, recovery activity tracker data | Cases find themselves pending callback indefinitely, due a lack of enforcement for follow-up (62% of current cases are marked to require follow-up). |
| PP-02 | Return account progress | SN-111 | Information is often incomplete and outdated because status updates must be manually re-keyed between systems, increasing administrative effort and the risk of error. |
| PP-03 | Is account status information coherent? | SN-015 | A  consideration that is required in the context of the current state of data inconsistency which contributes to operational value leakage and agent frustration. |
| PP-04 | Provide information on account status | SN-047, FA-06 | This is the primary factor in duplicate contact and customer frustration, resulting from incomplete data, as incomplete case histories and missed follow-ups reduce visibility into previous interactions. |
| PP-05 | Review case workload | SN-080, FA-03 | Managers lack visibility into the pipeline, which is particularly important when an estimated 38% of cases are straightforward and potentially suitable for self-service. |
| PP-06 | Update balance and payments received | SN-112, FA-09 | Agent effort in updating case progress is not applied consistently, creating uncertainty around payment status and activity data that supports approximately £8m of monthly recoveries. |

## Automation opportunities

| Automation opportunity | Opportunity name | Description | Pain point(s) addressed |
|---|---|---|---|
| OP-01 | Follow-up management | Automatically generate callback reminders, overdue follow-up alerts and ownership notifications to ensure customer contact actions are completed on time. | PP-01 |
| OP-02 | Synchronisation of case activity | Automatically synchronise customer interactions, status updates and payment activity between the legacy collections system, spreadsheets and communication channels to reduce manual reconciliation and inconsistent records. | PP-02, PP-03, PP-06 |
| OP-03 | Self-serve account summary | Provide customers with a self-service view of outstanding balances, repayment options, case progress and recent account activity, enabling them to understand their situation and take action without contacting an agent. | PP-04 |
| OP-04 | Management dashboards | Provide real-time visibility of case volumes, queue status, overdue actions and workflow bottlenecks to support operational decision-making. | PP-05 |
| OP-05 | Rules-based routing | Automatically identify and route straightforward cases to self-service journeys while escalating complex, vulnerable or specialist cases to agents. | PP-05 |

## Traceability table

| Stakeholder concern | Likely process area affected | Possible metric or evidence source | Likely deliverable | Priority JTBD | Automation opportunity |
|---|---|---|---|---|---|
| Agents spend a significant amount of time reconciling information across speadsheets, email trails and the legacy collections system. | Case workflow and customer contact | Financial assumptions | As-Is process map | JTBD-04 | OP-02 |
| Managers lack visibility into case progress | Case monitoring and reporting | Stakeholder interview notes | As-Is process map and JTBDs | JTBD-04 | OP-04 |
| Delayed actions and failed collections contribute to an estimated 15% revenue loss | Case workflow and customer contact | Financial assumptions | ROI model | JTBD-04 | OP-01 |
| Straightforward cases consume agent time despite requiring limited judgement. | Customer servicing and case triage | Delinquent account data | To-Be process map and automation opportunity assessment | JTBD-09 | OP-05 |
| Customers lack visibility of case progress and next steps, leading to repeat contact and reduced confidence in the recovery process. | Customer communications and case status management | Stakeholder interview notes | JTBDs and To-Be process map | JTBD-02 | OP-03 |
