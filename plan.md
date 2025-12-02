# WGL Workforce Capacity Planning Model
## Requirements Working Session

---

# Slide 1: Agenda

**Objective:** Align on model requirements and validate assumptions

| Time | Topic |
|------|-------|
| 5 min | Model Overview |
| 10 min | Objective: What are we trying to achieve? |
| 15 min | Parameters: What information feeds the model? |
| 15 min | Constraints: What rules must be followed? |
| 10 min | Decisions: What does the model determine? |
| 5 min | Outputs & Next Steps |

---

# Slide 2: Model Overview

**Workforce Capacity Planning Model**

```
┌─────────────────────────────────────────────────────────────────────────┐
│  OBJECTIVE                                                              │
│  What are we trying to achieve?                                         │
└─────────────────────────────────────────────────────────────────────────┘
                                    │
                                 USING
                                    ▼
┌─────────────────────────────────────────────────────────────────────────┐
│  PARAMETERS                                                             │
│  What information feeds the model?                                      │
└─────────────────────────────────────────────────────────────────────────┘
                                    │
                              SUBJECT TO
                                    ▼
┌─────────────────────────────────────────────────────────────────────────┐
│  CONSTRAINTS                                                            │
│  What rules must be followed?                                           │
└─────────────────────────────────────────────────────────────────────────┘
                                    │
                              BY DECIDING
                                    ▼
┌─────────────────────────────────────────────────────────────────────────┐
│  DECISIONS                                                              │
│  What does the model determine?                                         │
└─────────────────────────────────────────────────────────────────────────┘
                                    │
                              TO PRODUCE
                                    ▼
┌─────────────────────────────────────────────────────────────────────────┐
│  OUTPUTS                                                                │
│  What does the model produce?                                           │
└─────────────────────────────────────────────────────────────────────────┘
```

---

# Slide 3: Objective

**What are we trying to achieve?**

| Question | How It Influences Trade-offs |
|----------|------------------------------|
| Is it to maximize utilization? | If yes, model prioritizes regular hours → OT → contractors, regardless of cost |
| Is it to ensure SLAs are met by work type? | If yes, model penalizes missed deadlines heavily — may accept higher cost to meet SLAs |
| Are costs factored in for planning? | If no, model ignores cost — may use expensive options freely. If yes, model balances cost vs. coverage |
| When demand exceeds capacity, what matters most — cost control or getting work done? | Determines whether model prioritizes coverage or spend |
| Is there a priority order among work types? (e.g., EMER > SERV > MATN) | Determines which work gets deferred first when capacity is tight |

---

# Slide 4: Parameters — Demand

**What work needs to get done?**

| Question | How It Influences Trade-offs |
|----------|------------------------------|
| How is historical demand adjusted to come up with input for planning? | Determines demand accuracy — bad forecast = plan won't match reality |
| How is work completion time by work type determined to calculate demand in hours? | Affects capacity math — wrong durations = over/under scheduling |
| How is seasonality accounted for in planning? (e.g., higher emergency work in winter) | Determines if model sees peaks/valleys — affects when OT/contractors are needed |
| How is programmatic work (e.g., physical meter read every 3 years) taken into account in the planning process? | Predictable demand that can be shifted — gives model flexibility to smooth peaks |
| What is the planning horizon? (monthly, quarterly, annual?) | Determines how far ahead the model plans and optimizes |
| How far in advance is demand known? | Affects ability to plan proactively vs. react |

---

# Slide 5: Parameters — Supply

**Who is available to do the work?**

| Question | How It Influences Trade-offs |
|----------|------------------------------|
| To what extent is non-productive time already factored into average job duration by work type? | If not factored, model will overestimate available capacity |
| Is efficiency rates factored into job duration by work type and is it considered different by internal vs. external? | Affects true capacity consumed — wrong efficiency = wrong assignments |
| Is planning done at the jurisdiction or yard level? | Determines if model can share resources across areas or not |
| How is headcount data maintained — is it reliable and current? | Bad data = wrong capacity calculations |
| Are there different skill levels within a grade that affect productivity? | May need finer granularity than just grade |
| Can technicians work across districts, or are they fixed to one? | Determines flexibility to balance workload across geography |

---

# Slide 6: Parameters — Eligibility & Costs

**Who can do what? What are the cost drivers?**

| Question | How It Influences Trade-offs |
|----------|------------------------------|
| Where does certification/OQ data come from? Is it current? | Stale data = compliance risk (unqualified tech assigned) |
| Do contractors have the same certifications as internal? | May limit which work can go to contractors |
| Are cost rates (OT, contractor) available, or do we use relative weights? | If no cost data, model uses priority weights instead of dollars |
| Is there a cost difference between grades for the same work? | Affects whether model prefers one grade over another |

---

# Slide 7: Constraints

**What rules must be followed?**

| Question | How It Influences Trade-offs |
|----------|------------------------------|
| Are there any work types that cannot go to contractors? | If yes, those jobs can ONLY be filled by internal resources + OT — limits flexibility |
| Are there deadlines by work type or priority? | Defines when work MUST be done — tighter deadlines = less flexibility to defer |
| Are there constraints on when certain work types can be performed during the year? | Creates seasonal windows — model must fit work into allowed periods or defer |
| What is the maximum overtime allowed? (% of regular hours) | Caps flexibility — if 20% max, model must use contractors or defer beyond that |
| Is there a limit to contractor availability? | If unlimited, model can always buy capacity. If limited, must plan ahead |
| Which of these rules are absolute (cannot violate) vs. preferences (try to avoid)? | Hard rules limit options; soft rules give model flexibility with penalty |
| Are there union rules that affect scheduling or assignments? | May add constraints on who can do what, when, or how much |

---

# Slide 8: Decisions

**What does the model determine?**

| Question | How It Influences Trade-offs |
|----------|------------------------------|
| Are these the levers you pull today: overtime, contractors, defer work? | Confirms we've captured the right decision variables |
| Are there other levers we're missing? (e.g., cross-district movement, shift changes) | May need to add decision variables |
| Is contractor usage truly a decision, or is it always last resort? | Affects how model treats contractors — option vs. fallback |
| Who makes the final call on overtime authorization? | Determines if OT is a planning decision or operational decision |
| Can work be shifted between periods, or must it be done when scheduled? | Determines if model can smooth demand across time |

---

# Slide 9: Outputs

**What does the model produce?**

| Question | How It Influences Trade-offs |
|----------|------------------------------|
| What decisions do you need to make from these outputs? | Ensures we produce actionable information |
| What level of detail do you need? (monthly, weekly, by district, by grade?) | Determines model granularity |
| Do you need to compare scenarios? (e.g., "what if 2 more techs?") | Confirms scenario capability is needed |
| Who consumes these outputs? (planners only, or also management, finance?) | May need different views for different audiences |
| How do you track actuals vs. plan today? | Informs how outputs should be structured for comparison |

---

# Slide 10: Out of Scope (This Phase)

| Topic | Why Out of Scope |
|-------|------------------|
| Hiring decisions | Planners don't control hiring — 2 classes/year set by HR |
| Headcount changes | Fixed input, not a decision variable for planners |
| Attrition modeling | Follow-up discussion — may add in future phase |
| Promotions between grades | Future enhancement |

**Follow-up Question:**
- Do you account for expected turnover when planning? If so, how?

---

# Slide 11: Next Steps

| Action | Owner | Timeline |
|--------|-------|----------|
| Consolidate feedback from this session | PwC | This week |
| Provide data samples (demand, headcount, costs) | WGL | Next week |
| Refine model assumptions based on feedback | PwC | Next week |
| Follow-up session to review updated model | Joint | TBD |

---

# Appendix: Questions Summary

| Component | Question |
|-----------|----------|
| **Objective** | Is it to maximize utilization? |
| **Objective** | Is it to ensure SLAs are met by work type? |
| **Objective** | Are costs factored in for planning? |
| **Objective** | When demand exceeds capacity, what matters most — cost control or getting work done? |
| **Objective** | Is there a priority order among work types? |
| **Demand** | How is historical demand adjusted to come up with input for planning? |
| **Demand** | How is work completion time by work type determined to calculate demand in hours? |
| **Demand** | How is seasonality accounted for in planning? |
| **Demand** | How is programmatic work taken into account in the planning process? |
| **Demand** | What is the planning horizon? |
| **Demand** | How far in advance is demand known? |
| **Supply** | To what extent is non-productive time already factored into average job duration? |
| **Supply** | Is efficiency factored into job duration, different by internal vs. external? |
| **Supply** | Is planning done at the jurisdiction or yard level? |
| **Supply** | How is headcount data maintained? |
| **Supply** | Are there different skill levels within a grade? |
| **Supply** | Can technicians work across districts? |
| **Eligibility** | Where does certification data come from? Is it current? |
| **Eligibility** | Do contractors have the same certifications as internal? |
| **Costs** | Are cost rates available, or do we use relative weights? |
| **Costs** | Is there a cost difference between grades for the same work? |
| **Constraint** | Are there any work types that cannot go to contractors? |
| **Constraint** | Are there deadlines by work type or priority? |
| **Constraint** | Are there constraints on when certain work types can be performed during the year? |
| **Constraint** | What is the maximum overtime allowed? |
| **Constraint** | Is there a limit to contractor availability? |
| **Constraint** | Which rules are absolute vs. preferences? |
| **Constraint** | Are there union rules that affect scheduling? |
| **Decisions** | Are these the levers you pull today: overtime, contractors, defer work? |
| **Decisions** | Are there other levers we're missing? |
| **Decisions** | Is contractor usage truly a decision, or always last resort? |
| **Decisions** | Who makes the final call on overtime authorization? |
| **Decisions** | Can work be shifted between periods? |
| **Outputs** | What decisions do you need to make from these outputs? |
| **Outputs** | What level of detail do you need? |
| **Outputs** | Do you need to compare scenarios? |
| **Outputs** | Who consumes these outputs? |
| **Outputs** | How do you track actuals vs. plan today? |
| **Out of Scope** | Do you account for expected turnover when planning? |
