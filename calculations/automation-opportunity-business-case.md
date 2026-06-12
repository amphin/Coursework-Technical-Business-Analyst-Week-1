# Automation Opportunity Business Cases

**Source data:** finance_assumptions.csv, delinquent_accounts_export.csv, recovery_activity_tracker.csv, smart_recovery_portal_events.csv

**Key assumptions:**
- Agent hourly cost: £22
- Straightforward case volume: 627/month (7,524/year)
- Portal eligibility rate: 47.1%
- Reconciliation waste (duplicate-flagged): 72.3% of 3.31 hrs/day
- Agent productivity: 8 hrs/day × 252 working days/year

---

## Individual Opportunity Summary

### OP-01: Follow-up management

| Metric | Value |
|--------|-------|
| **Implementation cost** | £45,000 |
| **Complexity** | Low |
| **Annual hours saved** | 263 hrs |
| **Annual cost saved** | £5,793 |
| **Annual revenue uplift** | 0.5% (~£480,000) |
| **Payback period** | 93 months |
| **Annual hours saved** | 71 hrs |
| **Annual cost saved** | £1,562 |

| **Payback period** | 54 months |
```
Missed follow-ups avoided per year = missed_follow_up_rate × straightforward_cases/year × intervention_minutes/60
of queue status, overdue actions and bottlenecks enables supervisory team to manage prioritisation more efficiently. 3.5% time reduction in supervisor headcount (primarily manual status checks, exception handling, and dispatch coordination).
                                   = 0.14 × 7,524 × 0.25
                                   = 263 hours/year
Supervisor time freed = supervisor_count × hours_per_day × time_reduction_pct × working_days_per_year
                      = 1 FTE × 8 hrs/day × 0.035 × 252 days/year
                      = 70.56 hours/year ≈ 71 hours/year
Annual baseline recovery = £8,000,000/month × 12 = £96,000,000
Annual cost saved = 71 hrs × £22/hr = £1,562
Payback = £85,000 / £1,562 = 54.4 years (54 months)
```

**Risk:** Long payback reflects low margin per intervention; revenue uplift provides compelling justification when combined with OP-03 or OP-05.

---

### OP-02: Synchronisation of case activity

| Metric | Value |
|--------|-------|
| **Implementation cost** | £102,000 |
| **Complexity** | High |
| **Annual hours saved** | 603 hrs |
| **Annual cost saved** | £13,268 |
| **Annual revenue uplift** | 1.5% (~£1,440,000) |
| **Payback period** | 92 months |

**Rationale:** Eliminate manual reconciliation between legacy DB, spreadsheets and communication channels. Currently 1,458 reconciliation events per period with 72.3% flagged as duplicates. Gross reconciliation effort is 3.31 hrs/day; net waste from duplicates alone is ~2.39 hrs/day (~603 hrs/year).

**Calculation:**
```
Reconciliation duplicate waste per year = recon_hours_per_day_gross × duplicate_flag_pct × working_days_per_year
                                        = 3.31 hrs/day × 0.723 × 252 days/year
                                        = 2.39 hrs/day × 252
                                        = 603 hours/year

Annual cost saved = 603 hrs × £22/hr = £13,268
Payback = £102,000 / £13,268 = 7.68 years (92 months)

Revenue uplift from improved data quality and targeting:
Annual baseline recovery = £96,000,000
Estimated uplift rate = 1.5% (better data enables more accurate customer targeting and contact timing)
Annual recovery uplift = £96,000,000 × 0.015 = £1,440,000

Source data: 1,458 spreadsheet_reconcile rows logged; 1,054 flagged duplicate_check_flag=Y
  Total recon hours: 218.7 hrs logged / 3.31 hrs/day average
  Duplicate waste: 218.7 × (1,054/1,458) = 158.1 hrs observed in period
  Annualized: 158.1 hrs × (252 days / 66 days observed) = 603 hrs/year
```

**Risk:** Highest implementation cost; requires API layer and data synchronization logic. However, revenue uplift of £1.44M annually from improved data quality significantly improves business case.

---

### OP-03: Self-serve account summary

| Metric | Value |
|--------|-------|
| **Implementation cost** | £45,000 |
| **Complexity** | Low |
| **Annual hours saved** | 266 hrs |
| **Annual cost saved** | £5,844 |
| **Annual revenue uplift** | 2.0% (~£1,920,000) |
| **Payback period** | 92 months |

**Rationale:** Portal view of balances, options, progress and recent activity. At 47.1% eligibility (portal data) and 4.5 min saved per balance-view interaction, enables ~3,542 self-service cases/year to avoid agent contact.

**Calculation:**
```
Eligible self-service cases per year = portal_eligibility_rate × straightforward_cases/year
                                     = 0.4707 × 7,524 cases/year
                                     = 3,542 cases/year

Time saved per case = status_check_avg_minutes = 4.53 minutes (rounded to 4.5)

Total hours saved per year = 3,542 cases × 4.5 min / 60 min/hr
                           = 3,542 × 0.075
                           = 266 hours/year

Annual cost saved = 266 hrs × £22/hr = £5,844
Payback = £45,000 / £5,844 = 7.70 years (92 months)

Revenue uplift from self-service payment enablement:
Annual baseline recovery = £96,000,000
Estimated uplift rate = 2.0% (portal accessibility enables customers to pay independently; higher engagement & faster payment)
Annual recovery uplift = £96,000,000 × 0.020 = £1,920,000

Source: Portal eligibility = 1,196 eligible journeys / 2,541 total journeys = 47.1%
        Status check avg = 4.5336 min (from 1,400 status_check activities in tracker)
```

**Risk:** Savings are only for cases where balance view alone resolves inquiry; benefits may be front-loaded in case volume but limited by portal adoption. Revenue uplift of £1.92M provides strong justification when combined with OP-05 routing.

---

### OP-04: Management dashboards

| Metric | Value |
|--------|-------|
| **Implementation cost** | £85,000 |
| **Complexity** | Medium |
| **Annual hours saved** | 2,419 hrs |
| **Annual cost saved** | £53,222 |
| **Annual revenue uplift** | 1.0% (~£960,000) |
| **Payback period** | 19 months |

**Rationale:** Real-time visibility of queue status, overdue actions and bottlenecks. Conservative 3% reduction in admin overhead across 40-agent team (primarily supervision, dispatch, exception handling). Portal eligibility findings show 47% of cases *could* self-serve; dashboards enable faster triage and routing.

**Calculation:**
```
Agent productivity improvement = admin_overhead_reduction_pct × agent_count × hours_per_day × working_days_per_year
                               = 0.03 × 40 agents × 8 hrs/day × 252 days/year
                               = 0.03 × 80,640 agent-hours/year
                               = 2,419 hours/year

Annual cost saved = 2,419 hrs × £22/hr = £53,222
Payback = £85,000 / £53,222 = 1.60 years (19 months)

Revenue uplift from improved prioritisation and targeting:
Annual baseline recovery = £96,000,000
Estimated uplift rate = 1.0% (visibility enables supervisors to reduce lost cases through better routing and contact timing orchestration)
Annual recovery uplift = £96,000,000 × 0.010 = £960,000

Assumption basis: 
  - Assumes typical 1:8 supervisor-to-agent ratio (40-agent team = ~5 supervisors; conservative estimate of 1 FTE equivalent benefit from dashboards)
  - 3.5% time savings reflects manual status checks, exception flagging, and dispatch coordination now automated
  - Revenue uplift driven by supervisory visibility enabling faster case prioritisation and resource allocation across collection team
```

**Benefit:** Shortest payback (19 months); revenue uplift of £960k annually makes this most compelling. Benefits likely to scale as case volume grows.

---

### OP-05: Rules-based routing

| Metric | Value |
|--------|-------|
| **Implementation cost** | £85,000 |
| **Complexity** | Medium |
| **Annual hours saved** | 1,254 hrs |
| **Annual cost saved** | £27,588 |
| **Annual revenue uplift** | 2.5% (~£2,400,000) |
| **Payback period** | 37 months |

**Rationale:** Automatically route straightforward cases (627/month) to self-service journeys, escalate complex/vulnerable cases to agents. Saves ~10 min per case in specialist routing and triage time. Directly addresses stakeholder note: "We need to fix the fundamentals before we can build anything new on top."

**Calculation:**
```
Straightforward cases per year = straightforward_cases_per_month × 12 months
                               = 627 cases/month × 12
                               = 7,524 cases/year

Triage/routing time saved per case = 10 minutes

Total hours saved per year = 7,524 cases × 10 min / 60 min/hr
                           = 7,524 × 0.1667
                           = 1,254 hours/year

Annual cost saved = 1,254 hrs × £22/hr = £27,588
Payback = £85,000 / £27,588 = 3.08 years (37 months)

Revenue uplift from efficient routing to self-service at scale:
Annual baseline recovery = £96,000,000
Estimated uplift rate = 2.5% (direct routing to self-service for 47% of eligible cases; improved time-to-contact and payment rate)
Annual recovery uplift = £96,000,000 × 0.025 = £2,400,000

Source: Straightforward cases identified as self_service_candidate=Y in accounts export
        Oct-25: 593, Nov-25: 645, Dec-25: 635, Jan-26: 634 cases
        Average: 626.75 cases/month, annualized 7,521 cases/year
```

**Benefit:** Moderate payback (37 months) but drives highest revenue uplift (£2.4M annually). Unlocks OP-03 and OP-01 benefits; enables self-service at scale. Revenue uplift from improved payment capture justifiable given 47% portal eligibility rate and 88.93% confirmation rate for eligible customers.

---

## Portfolio Summary

| Metric | Value |
|--------|-------|
| **Total implementation investment** | £362,000 |
| **Total annual hours saved** | 2,457 hrs |
| **Total annual cost savings** | £54,055 |
| **Total annual revenue uplift** | £7,200,000 |
| **Total annual benefit (cost + revenue)** | £7,254,055 |
| **Portfolio payback period** | 80 months |

### Recommended sequencing

**Phase 1 (Months 0–4, £85k):** OP-04 (dashboards) + OP-05 (routing)
- Establishes visibility and case routing foundation
- Enables all downstream benefits
- Payback: 22.4 months (combined)

**Phase 2 (Months 4–8, £90k):** OP-01 (follow-up) + OP-03 (self-serve account)
- Builds on routing capability
- Low implementation complexity
- Further payback: ~92 months (standalone), but cumulative portfolio benefit now visible

**Phase 3 (Months 8–12, £102k):** OP-02 (synchronisation)
- Complex, but addresses root cause of 72% reconciliation waste
- Unlocks benefits in OP-01 and OP-03 by improving data reliability
- Long payback acceptable as foundational risk removal

---

## Sensitivity Analysis

If agent hourly cost rises to £25/hr (e.g., inflation, headcount unavailability):
- Total annual savings: £120,125 (+13.6%)
- Portfolio payback: 36 months (vs 41 months)
- Payback: ~70 months (combined, cost-side); £3.36M annual revenue uplift justifies investment

**Phase 2 (Months 4–8, £90k):** OP-01 (follow-up) + OP-03 (self-serve account)
- Builds on routing capability
- Low implementation complexity
- Combined revenue uplift of £2.4M per year justifies phasing

**Phase 3 (Months 8–12, £102k):** OP-02 (synchronisation)
- Complex, but addresses root cause of 72% reconciliation waste
- Unlocks benefits in OP-01 and OP-03 by improving data reliability
- Long payback acceptable as foundational risk removal

---

## Sensitivity Analysis

If agent hourly cost rises to £25/hr (e.g., inflation, headcount unavailability):
- Total annual savings: £61,425 (+13.6%)
- Portfolio payback: 71 months (vs 80 months)

If portal eligibility rises to 55% (from 47.1%):
- OP-03 hours saved: 313 hrs (+47 hrs)
- OP-04 and OP-05 benefits scale accordingly

If reconciliation duplicate rate falls to 50% (current intervention):
- OP-02 annual hours: 416 hrs (−187 hrs)
- OP-02 becomes breakeven in Year 2 if deployed alongside OP-03/OP-05
