# WGL Requirements Working Session
## Polished Question & Context Options

---

# SLIDE 3: OBJECTIVE

## Question 1

**Current:** Is it to maximize utilization?

| # | Question Options |
|---|------------------|
| 1 | Is the goal to maximize use of internal workforce before leveraging external resources? |
| 2 | Is prioritizing full use of existing staff a key planning objective? |
| 3 | Is workforce utilization a primary driver, or is it one of several factors? |
| 4 | Do you aim to fully utilize internal capacity before considering overtime or contractors? |
| 5 | How important is it to maximize use of your current workforce vs. other objectives? |

**Current Context:** If yes, model prioritizes regular hours → OT → contractors, regardless of cost

| # | Context Options |
|---|-----------------|
| 1 | Model will exhaust internal capacity before leveraging external resources — cost becomes secondary |
| 2 | Drives preference for internal workforce even when external options may be cheaper |
| 3 | Creates hierarchy: regular hours first, then overtime, then contractors — independent of cost |
| 4 | Cost efficiency may be sacrificed to maximize internal resource utilization |
| 5 | Prioritizes "use what we have" over "find the cheapest option" |

---

## Question 2

**Current:** Is it to ensure SLAs are met by work type?

| # | Question Options |
|---|------------------|
| 1 | Are there service level targets by work type that must be met? |
| 2 | Do specific work types have completion commitments that drive planning? |
| 3 | Is meeting service level agreements a primary planning objective? |
| 4 | Are there defined performance targets (e.g., % on-time) by work type? |
| 5 | How do service level commitments influence how you allocate capacity? |

**Current Context:** If yes, model penalizes missed deadlines heavily — may accept higher cost to meet SLAs

| # | Context Options |
|---|-----------------|
| 1 | Model will prioritize meeting commitments even if it means higher cost |
| 2 | SLA compliance becomes a constraint — cost optimization happens within that boundary |
| 3 | Missed deadlines carry significant weight — model may use premium resources to avoid them |
| 4 | Trade-off shifts toward coverage over cost when SLAs are at risk |
| 5 | Defines which work "must" get done vs. which work "should" get done |

---

## Question 3

**Current:** Are costs factored in for planning?

| # | Question Options |
|---|------------------|
| 1 | Does cost influence how you make capacity decisions today? |
| 2 | Is cost a factor in planning, or is it primarily about getting work done? |
| 3 | When making trade-offs, do you consider the cost of different options? |
| 4 | Is budget a constraint you plan around, or is it managed separately? |
| 5 | How does cost factor into decisions about overtime vs. contractors vs. deferral? |

**Current Context:** If no, model ignores cost — may use expensive options freely. If yes, model balances cost vs. coverage

| # | Context Options |
|---|-----------------|
| 1 | Determines whether model optimizes for cost or treats all capacity options equally |
| 2 | If cost matters, model will prefer cheaper options; if not, model focuses only on coverage |
| 3 | Defines whether "get it done" or "get it done efficiently" is the goal |
| 4 | Shapes how model chooses between overtime, contractors, and deferral |
| 5 | Without cost input, model cannot distinguish between a $50/hr and $100/hr option |

---

## Question 4

**Current:** When demand exceeds capacity, what matters most — cost control or getting work done?

| # | Question Options |
|---|------------------|
| 1 | When capacity is tight, what takes priority — controlling spend or completing work? |
| 2 | If you can't do everything, do you prioritize coverage or cost? |
| 3 | What's more acceptable — higher cost or deferred work? |
| 4 | When trade-offs are needed, is the bias toward "stay in budget" or "get it done"? |
| 5 | How do you balance cost control against work completion when resources are stretched? |

**Current Context:** Determines whether model prioritizes coverage or spend

| # | Context Options |
|---|-----------------|
| 1 | Sets the fundamental trade-off: pay more to complete work, or defer work to control cost |
| 2 | Defines model behavior when no perfect solution exists |
| 3 | Guides whether model leans toward overtime/contractors or toward deferral |
| 4 | Determines if "all work done at higher cost" beats "some work deferred at lower cost" |
| 5 | Shapes the objective function weighting between cost and unmet demand |

---

## Question 5

**Current:** Is there a priority order among work types? (e.g., EMER > SERV > MATN)

| # | Question Options |
|---|------------------|
| 1 | How do you prioritize across work types when capacity is constrained? |
| 2 | Is there a defined hierarchy for which work gets done first? |
| 3 | When you can't do everything, which work types take precedence? |
| 4 | Are certain order types always prioritized over others? |
| 5 | What determines which work gets deferred first when resources are tight? |

**Current Context:** Determines which work gets deferred first when capacity is tight

| # | Context Options |
|---|-----------------|
| 1 | Model will defer lower-priority work before touching higher-priority work |
| 2 | Establishes the "sacrifice order" when demand exceeds capacity |
| 3 | Ensures critical work is protected while allowing flexibility on deferrable work |
| 4 | Defines explicit priority rules vs. leaving it to cost/penalty trade-offs |
| 5 | Prevents model from deferring emergency work to save cost on backlog |

---

# SLIDE 4: PARAMETERS — DEMAND

## Question 1

**Current:** How is historical demand adjusted to come up with input for planning?

| # | Question Options |
|---|------------------|
| 1 | Where does demand input come from — historical actuals, current backlog, or forecast? |
| 2 | How do you estimate future demand for planning purposes? |
| 3 | Is demand based on historical patterns, and if so, how are adjustments made? |
| 4 | What's the basis for the demand numbers you plan against? |
| 5 | How confident are you in the demand forecast — is it firm or directional? |

**Current Context:** Determines demand accuracy — bad forecast = plan won't match reality

| # | Context Options |
|---|-----------------|
| 1 | Model output is only as good as the demand input — garbage in, garbage out |
| 2 | Informs whether model should plan to exact numbers or build in buffer |
| 3 | Affects confidence level in the plan — precise forecast vs. rough estimate |
| 4 | Determines if scenarios should stress-test demand variability |
| 5 | Shapes how tightly model can optimize vs. how much flexibility to preserve |

---

## Question 2

**Current:** How is work completion time by work type determined to calculate demand in hours?

| # | Question Options |
|---|------------------|
| 1 | How are standard job durations determined for each work type? |
| 2 | Where do the "hours per job" estimates come from? |
| 3 | Are job durations based on historical averages, standards, or estimates? |
| 4 | How often are duration estimates reviewed and updated? |
| 5 | Do durations vary by complexity, location, or technician experience? |

**Current Context:** Affects capacity math — wrong durations = over/under scheduling

| # | Context Options |
|---|-----------------|
| 1 | Duration accuracy directly impacts capacity calculations — 20% error means 20% wrong |
| 2 | Understated durations lead to overcommitment; overstated durations leave capacity unused |
| 3 | Model matches hours of demand to hours of supply — both must be calibrated |
| 4 | Determines whether "100 jobs" translates to 200 hours or 400 hours |
| 5 | Feeds directly into feasibility — can the workforce actually complete the plan? |

---

## Question 3

**Current:** How is seasonality accounted for in planning? (e.g., higher emergency work in winter)

| # | Question Options |
|---|------------------|
| 1 | Does demand fluctuate by season, and if so, how is that reflected in planning? |
| 2 | Are there predictable peaks and valleys throughout the year? |
| 3 | How do you account for seasonal variation — e.g., winter emergencies, summer construction? |
| 4 | Is seasonal demand built into forecasts, or handled reactively? |
| 5 | Which work types have the most pronounced seasonality? |

**Current Context:** Determines if model sees peaks/valleys — affects when OT/contractors are needed

| # | Context Options |
|---|-----------------|
| 1 | Model can pre-position capacity for known peaks instead of reacting |
| 2 | Without seasonality, model may recommend flat staffing that fails during peaks |
| 3 | Enables proactive contractor procurement vs. last-minute scramble |
| 4 | Shapes overtime authorization timing — planned vs. reactive |
| 5 | Allows model to shift deferrable work away from peak periods |

---

## Question 4

**Current:** How is programmatic work (e.g., physical meter read every 3 years) taken into account in the planning process?

| # | Question Options |
|---|------------------|
| 1 | How is scheduled/programmatic work incorporated into capacity planning? |
| 2 | Is there planned work (inspections, replacements, etc.) that can be scheduled flexibly? |
| 3 | What portion of demand is predictable and can be shifted vs. must be done when it arrives? |
| 4 | How do you balance programmatic work against reactive/emergency work? |
| 5 | Can planned programs be accelerated or deferred based on capacity? |

**Current Context:** Predictable demand that can be shifted — gives model flexibility to smooth peaks

| # | Context Options |
|---|-----------------|
| 1 | Programmatic work is a lever — model can use it to fill valleys or defer during peaks |
| 2 | Provides flexibility to balance workload across periods |
| 3 | Distinguishes "must do now" from "must do this year" |
| 4 | Allows model to optimize timing, not just assignment |
| 5 | If rigid, programmatic work becomes a constraint; if flexible, it becomes an opportunity |

---

## Question 5

**Current:** What is the planning horizon? (monthly, quarterly, annual?)

| # | Question Options |
|---|------------------|
| 1 | How far ahead do you plan capacity — weeks, months, quarters? |
| 2 | What's the typical planning cycle for workforce capacity? |
| 3 | Is planning done monthly with annual outlook, or some other cadence? |
| 4 | How far into the future do you need visibility on capacity gaps? |
| 5 | Does the planning horizon differ by work type or decision type? |

**Current Context:** Determines how far ahead the model plans and optimizes

| # | Context Options |
|---|-----------------|
| 1 | Short horizon = reactive planning; long horizon = strategic planning |
| 2 | Affects granularity — monthly buckets vs. weekly buckets |
| 3 | Determines whether model can recommend actions that take time to implement |
| 4 | Shapes trade-off between precision (near-term) and flexibility (long-term) |
| 5 | Informs how many periods the model optimizes across |

---

## Question 6

**Current:** How far in advance is demand known?

| # | Question Options |
|---|------------------|
| 1 | How much lead time do you have on incoming work? |
| 2 | Is demand known weeks ahead, or does it arrive day-of? |
| 3 | What percentage of work is scheduled vs. reactive? |
| 4 | How does visibility differ by work type — emergencies vs. planned work? |
| 5 | At what point does demand become "locked" for planning purposes? |

**Current Context:** Affects ability to plan proactively vs. react

| # | Context Options |
|---|-----------------|
| 1 | More lead time = more opportunity to optimize; less lead time = more reactive |
| 2 | Determines how much capacity should be reserved for unplanned work |
| 3 | Shapes whether model plans to specific jobs or to expected volumes |
| 4 | Affects feasibility of contractor pre-procurement |
| 5 | Informs how often the plan needs to be re-run and updated |

---

# SLIDE 5: PARAMETERS — SUPPLY

## Question 1

**Current:** To what extent is non-productive time already factored into average job duration by work type?

| # | Question Options |
|---|------------------|
| 1 | Do job durations include travel, admin, and breaks — or just wrench time? |
| 2 | Is non-productive time built into job estimates or tracked separately? |
| 3 | How is the gap between "clock hours" and "productive hours" accounted for? |
| 4 | What utilization rate do you assume for planning — 100%, 80%, 70%? |
| 5 | Where does non-productive time show up — in job duration or in available hours? |

**Current Context:** If not factored, model will overestimate available capacity

| # | Context Options |
|---|-----------------|
| 1 | Determines whether 8 hours on the clock means 8 hours of work or 6 hours |
| 2 | Critical for realistic capacity — missing this creates a 20-30% error |
| 3 | If in job duration, capacity math is straightforward; if separate, model needs utilization factor |
| 4 | Avoids over-scheduling technicians and creating unachievable plans |
| 5 | Must be consistent — double-counting utilization understates capacity |

---

## Question 2

**Current:** Is efficiency rates factored into job duration by work type and is it considered different by internal vs. external?

| # | Question Options |
|---|------------------|
| 1 | Do job durations vary by who performs the work — internal vs. contractor? |
| 2 | Are some technicians faster than others, and is that reflected in planning? |
| 3 | Is there an efficiency factor applied by grade, experience, or resource type? |
| 4 | How do contractor productivity assumptions compare to internal staff? |
| 5 | Are durations "standard" or adjusted based on who's assigned? |

**Current Context:** Affects true capacity consumed — wrong efficiency = wrong assignments

| # | Context Options |
|---|-----------------|
| 1 | If contractors are slower, assigning them work consumes more capacity than expected |
| 2 | Model may over-assign to less efficient resources, creating backlogs |
| 3 | Enables model to make smarter trade-offs between resource types |
| 4 | Determines whether one hour of contractor time equals one hour of employee time |
| 5 | Calibration matters — current Click settings assume contractors are 2-3x more productive |

---

## Question 3

**Current:** Is planning done at the jurisdiction or yard level?

| # | Question Options |
|---|------------------|
| 1 | At what geographic level is capacity planning performed? |
| 2 | Is planning done centrally, by jurisdiction, by district, or by yard? |
| 3 | Can resources be shared across geographic boundaries for planning purposes? |
| 4 | How do you define the "unit" for capacity planning — what level of granularity? |
| 5 | Are there geographic constraints on where technicians can be assigned? |

**Current Context:** Determines if model can share resources across areas or not

| # | Context Options |
|---|-----------------|
| 1 | Finer granularity = more precise but less flexibility to balance across areas |
| 2 | If resources are pooled, model can shift capacity to where it's needed |
| 3 | If resources are fixed to locations, model is constrained by local capacity |
| 4 | Affects how shortages in one area can be addressed by surplus in another |
| 5 | Shapes whether cross-district assignment is a lever or not |

---

## Question 4

**Current:** How is headcount data maintained — is it reliable and current?

| # | Question Options |
|---|------------------|
| 1 | Where does headcount data come from, and how current is it? |
| 2 | Is the roster updated in real-time, or is there lag? |
| 3 | How confident are you in headcount numbers by grade and location? |
| 4 | How are leaves, vacancies, and temporary changes reflected? |
| 5 | What's the source of truth for "who's available"? |

**Current Context:** Bad data = wrong capacity calculations

| # | Context Options |
|---|-----------------|
| 1 | Model assumes headcount is accurate — variance creates over/under capacity |
| 2 | Stale data means model plans for people who aren't there |
| 3 | Affects confidence in plan feasibility |
| 4 | Determines if model needs buffer for headcount uncertainty |
| 5 | Data quality directly impacts model reliability |

---

## Question 5

**Current:** Are there different skill levels within a grade that affect productivity?

| # | Question Options |
|---|------------------|
| 1 | Within a grade, are there meaningful productivity differences between technicians? |
| 2 | Is a Grade 6A with 10 years' experience equivalent to a new Grade 6A? |
| 3 | Are there skill tiers within grades that affect what work can be assigned? |
| 4 | How do you account for experience differences in planning? |
| 5 | Is grade sufficient for planning, or is more granularity needed? |

**Current Context:** May need finer granularity than just grade

| # | Context Options |
|---|-----------------|
| 1 | If significant variation exists, grade-level planning may mask capacity gaps |
| 2 | Model may need sub-grade segmentation for accuracy |
| 3 | Affects eligibility matrix — who can realistically do what |
| 4 | Determines if "10 Grade 6A techs" is interchangeable or requires nuance |
| 5 | Impacts efficiency factors — one size may not fit all within a grade |

---

## Question 6

**Current:** Can technicians work across districts, or are they fixed to one?

| # | Question Options |
|---|------------------|
| 1 | Are technicians assigned to a fixed district, or can they work across boundaries? |
| 2 | How flexible is geographic assignment in practice? |
| 3 | Is cross-district movement a planning lever you use today? |
| 4 | What drives district assignment — policy, union, logistics, or preference? |
| 5 | If one district is short and another has slack, can you rebalance? |

**Current Context:** Determines flexibility to balance workload across geography

| # | Context Options |
|---|-----------------|
| 1 | If fixed, model must solve each district independently — no load balancing |
| 2 | If flexible, model can shift resources to where demand is highest |
| 3 | Defines whether district boundaries are hard constraints or soft preferences |
| 4 | Affects overtime/contractor needs — flexibility reduces reliance on external capacity |
| 5 | Shapes whether geographic mismatch creates artificial shortages |

---

# SLIDE 6: PARAMETERS — ELIGIBILITY & COSTS

## Question 1

**Current:** Where does certification/OQ data come from? Is it current?

| # | Question Options |
|---|------------------|
| 1 | Where is technician certification data maintained, and how current is it? |
| 2 | Is OQ/certification data integrated with planning systems, or managed separately? |
| 3 | How quickly are new certifications or expirations reflected in planning data? |
| 4 | What's the source of truth for "who is qualified for what"? |
| 5 | How do you track expiring certifications for planning purposes? |

**Current Context:** Stale data = compliance risk (unqualified tech assigned)

| # | Context Options |
|---|-----------------|
| 1 | Model relies on eligibility data — if wrong, it may assign unqualified techs |
| 2 | Safety and compliance depend on accurate, current certification data |
| 3 | Stale data can either over-restrict (missing new certs) or under-restrict (missing expirations) |
| 4 | Determines if eligibility is reliable or needs manual validation |
| 5 | Affects trust in model output — "can this person actually do this job?" |

---

## Question 2

**Current:** Do contractors have the same certifications as internal?

| # | Question Options |
|---|------------------|
| 1 | Are contractor qualifications equivalent to internal technicians? |
| 2 | Is there work that contractors cannot do due to certification gaps? |
| 3 | How is contractor eligibility defined — by individual or by contract? |
| 4 | Do you verify contractor certifications, or assume parity? |
| 5 | Are there work types where internal staff is required regardless of contractor qualifications? |

**Current Context:** May limit which work can go to contractors

| # | Context Options |
|---|-----------------|
| 1 | If contractors lack certain certs, those work types must stay internal |
| 2 | Affects how much flexibility contractors provide as a capacity lever |
| 3 | Model needs contractor eligibility matrix, not just employee eligibility |
| 4 | Shapes realistic contractor utilization — not all work can be outsourced |
| 5 | May require different contractor pools for different work types |

---

## Question 3

**Current:** Are cost rates (OT, contractor) available, or do we use relative weights?

| # | Question Options |
|---|------------------|
| 1 | Are actual cost rates available for overtime and contractor labor? |
| 2 | Can we use real dollar costs, or do we need proxy weights? |
| 3 | Is cost data accessible for planning, or is it managed by finance separately? |
| 4 | How are overtime and contractor costs structured — hourly, daily, fixed? |
| 5 | Do cost rates vary by grade, work type, or contractor? |

**Current Context:** If no cost data, model uses priority weights instead of dollars

| # | Context Options |
|---|-----------------|
| 1 | Real costs enable true cost optimization; weights enable preference ordering |
| 2 | Without costs, model can still prioritize but cannot quantify savings |
| 3 | Determines whether outputs show dollar impact or relative improvement |
| 4 | Affects whether finance can validate model recommendations |
| 5 | Shapes objective function — minimize dollars vs. minimize "penalty points" |

---

## Question 4

**Current:** Is there a cost difference between grades for the same work?

| # | Question Options |
|---|------------------|
| 1 | Does it cost more to have a higher grade perform work a lower grade could do? |
| 2 | Is labor cost a factor in deciding which grade to assign? |
| 3 | Are you indifferent to grade assignment as long as the work gets done? |
| 4 | How significant are cost differences between grades? |
| 5 | Should the model prefer lower-cost grades when multiple are eligible? |

**Current Context:** Affects whether model prefers one grade over another

| # | Context Options |
|---|-----------------|
| 1 | If costs differ, model will prefer lower-cost grades for eligible work |
| 2 | If costs are equal, model optimizes on other factors (availability, efficiency) |
| 3 | May drive "right-sizing" — don't use a Grade 8 for Grade 5 work |
| 4 | Enables trade-off: higher grade finishes faster but costs more |
| 5 | Without cost difference, grade preference becomes a policy choice, not optimization |

---

# SLIDE 7: CONSTRAINTS

## Question 1

**Current:** Are there any work types that cannot go to contractors?

| # | Question Options |
|---|------------------|
| 1 | Are there work types that must be performed by internal employees only? |
| 2 | Do union rules or policies restrict contractor usage for certain work? |
| 3 | Which work types, if any, are off-limits for contractors? |
| 4 | Is contractor eligibility defined by work type, or is it universal? |
| 5 | Are there safety or compliance reasons that require internal staff for certain jobs? |

**Current Context:** If yes, those jobs can ONLY be filled by internal resources + OT — limits flexibility

| # | Context Options |
|---|-----------------|
| 1 | Contractor-ineligible work reduces capacity options — only internal or overtime |
| 2 | Model must recognize this constraint to avoid infeasible assignments |
| 3 | Increases pressure on internal workforce for restricted work types |
| 4 | May drive higher overtime for contractor-ineligible work during peaks |
| 5 | Defines hard boundary on contractor utilization |

---

## Question 2

**Current:** Are there deadlines by work type or priority?

| # | Question Options |
|---|------------------|
| 1 | Are there defined completion timeframes by work type or priority? |
| 2 | What makes work "overdue" — is it days, weeks, or does it vary? |
| 3 | Which work types have strict deadlines vs. flexible completion windows? |
| 4 | How long can different priority levels wait before they become a problem? |
| 5 | Are deadlines regulatory, customer-driven, or internal policy? |

**Current Context:** Defines when work MUST be done — tighter deadlines = less flexibility to defer

| # | Context Options |
|---|-----------------|
| 1 | Tight deadlines constrain deferral — work must be done or flagged as missed |
| 2 | Shapes how model treats time — strict periods vs. rolling windows |
| 3 | Determines SLA/penalty structure by work type |
| 4 | Affects how much flexibility model has to smooth workload across periods |
| 5 | Distinguishes "must do this month" from "must do this quarter" |

---

## Question 3

**Current:** Are there constraints on when certain work types can be performed during the year?

| # | Question Options |
|---|------------------|
| 1 | Are there seasonal windows when certain work must or cannot be done? |
| 2 | Do any work types have calendar-based restrictions? |
| 3 | Is there work that can only be performed in certain months? |
| 4 | How do weather or seasonal conditions affect what work can be scheduled? |
| 5 | Are there blackout periods when certain work is not performed? |

**Current Context:** Creates seasonal windows — model must fit work into allowed periods or defer

| # | Context Options |
|---|-----------------|
| 1 | Calendar constraints reduce scheduling flexibility |
| 2 | Model must front-load or back-load work around restricted windows |
| 3 | May create artificial peaks before/after blackout periods |
| 4 | Affects how demand is distributed across the planning horizon |
| 5 | Distinguishes hard calendar rules from weather-driven preferences |

---

## Question 4

**Current:** What is the maximum overtime allowed? (% of regular hours)

| # | Question Options |
|---|------------------|
| 1 | Is there a cap on overtime, and if so, what is it? |
| 2 | What's the maximum overtime allowed — by policy, union, or practice? |
| 3 | Is the overtime limit per person, per grade, or overall? |
| 4 | Is the overtime cap a hard rule or a guideline? |
| 5 | How is overtime managed today — pre-approved budgets or case-by-case? |

**Current Context:** Caps flexibility — if 20% max, model must use contractors or defer beyond that

| # | Context Options |
|---|-----------------|
| 1 | Overtime cap determines how much internal flex exists before external capacity is needed |
| 2 | Lower cap = more contractor dependency; higher cap = more internal flex |
| 3 | Hard cap constrains model; soft cap incurs penalty but allows exceptions |
| 4 | Affects feasibility — can demand be met within overtime limits? |
| 5 | Shapes trade-off between overtime fatigue/cost and contractor cost |

---

## Question 5

**Current:** Is there a limit to contractor availability?

| # | Question Options |
|---|------------------|
| 1 | Is contractor capacity unlimited, or is there a ceiling? |
| 2 | How many contractor hours can you realistically procure? |
| 3 | Does contractor availability vary by skill, location, or season? |
| 4 | Are there lead times to secure contractor capacity? |
| 5 | What constrains contractor usage — availability, cost, or policy? |

**Current Context:** If unlimited, model can always buy capacity. If limited, must plan ahead.

| # | Context Options |
|---|-----------------|
| 1 | Unlimited contractors = demand can always be met (at a cost) |
| 2 | Limited contractors = model must respect availability ceiling |
| 3 | Affects whether contractor hours are a real constraint or just a cost |
| 4 | Shapes proactive procurement vs. reactive hiring |
| 5 | Determines if contractor scarcity can cause unmet demand |

---

## Question 6

**Current:** Which of these rules are absolute (cannot violate) vs. preferences (try to avoid)?

| # | Question Options |
|---|------------------|
| 1 | Which constraints are hard rules vs. soft preferences? |
| 2 | For each rule, what happens if it's violated — is it unacceptable or just undesirable? |
| 3 | Are there rules you'd break in an emergency but not under normal circumstances? |
| 4 | How do you distinguish "must follow" from "should follow" in planning? |
| 5 | What's negotiable when capacity is tight, and what's non-negotiable? |

**Current Context:** Hard rules limit options; soft rules give model flexibility with penalty

| # | Context Options |
|---|-----------------|
| 1 | Hard constraints eliminate options; soft constraints penalize but allow exceptions |
| 2 | Too many hard rules = infeasible solutions; too few = unacceptable outcomes |
| 3 | Determines model flexibility during peak/crisis periods |
| 4 | Shapes whether model has room to find creative solutions |
| 5 | Distinguishes safety/compliance rules from operational preferences |

---

## Question 7

**Current:** Are there union rules that affect scheduling or assignments?

| # | Question Options |
|---|------------------|
| 1 | Are there union rules that constrain who can do what or when? |
| 2 | Do collective bargaining agreements affect work assignments or overtime? |
| 3 | Are there contractual limits on contractor usage? |
| 4 | How do union rules influence how work is distributed? |
| 5 | Are there seniority or rotation rules that affect scheduling? |

**Current Context:** May add constraints on who can do what, when, or how much

| # | Context Options |
|---|-----------------|
| 1 | Union rules become hard constraints — model cannot violate |
| 2 | May restrict flexibility on overtime, assignments, or contractor mix |
| 3 | Affects feasibility — some solutions may violate labor agreements |
| 4 | Model must be configured to respect contractual boundaries |
| 5 | Distinguishes management preferences from negotiated requirements |

---

# SLIDE 8: DECISIONS

## Question 1

**Current:** Are these the levers you pull today: overtime, contractors, defer work?

| # | Question Options |
|---|------------------|
| 1 | When capacity falls short, what actions do you take — overtime, contractors, deferral? |
| 2 | Are these the primary levers you use to balance supply and demand? |
| 3 | How do you close capacity gaps today? |
| 4 | When demand exceeds capacity, what options do you consider? |
| 5 | Is this the complete set of levers, or are we missing something? |

**Current Context:** Confirms we've captured the right decision variables

| # | Context Options |
|---|-----------------|
| 1 | Model can only optimize levers we've defined — missing levers = incomplete solution |
| 2 | Validates that model decisions match real-world options |
| 3 | Ensures recommendations are actionable |
| 4 | Confirms scope of what model controls vs. what's fixed |
| 5 | Identifies gaps before building vs. after |

---

## Question 2

**Current:** Are there other levers we're missing? (e.g., cross-district movement, shift changes)

| # | Question Options |
|---|------------------|
| 1 | Are there other ways you flex capacity that we haven't mentioned? |
| 2 | Do you use cross-district assignments, shift adjustments, or other mechanisms? |
| 3 | What levers do you wish you could pull but currently can't? |
| 4 | Are there capacity options that are available but rarely used? |
| 5 | What's in your toolkit beyond overtime, contractors, and deferral? |

**Current Context:** May need to add decision variables

| # | Context Options |
|---|-----------------|
| 1 | Additional levers expand solution space — more options for model to consider |
| 2 | Missing levers may require model enhancements |
| 3 | Some levers may be out of scope for this phase but noted for future |
| 4 | Ensures model reflects full range of operational flexibility |
| 5 | Identifies quick wins vs. longer-term enhancements |

---

## Question 3

**Current:** Is contractor usage truly a decision, or is it always last resort?

| # | Question Options |
|---|------------------|
| 1 | Is contractor usage a proactive choice or a reactive fallback? |
| 2 | Are contractors planned into capacity, or only used when internal options fail? |
| 3 | How do you view contractors — as a flexible resource or as a last resort? |
| 4 | Would you use contractors proactively if it reduced overtime? |
| 5 | Is there a preference to avoid contractors even if they're cost-effective? |

**Current Context:** Affects how model treats contractors — option vs. fallback

| # | Context Options |
|---|-----------------|
| 1 | If proactive, model can optimize across internal and contractor capacity |
| 2 | If last resort, model prioritizes internal options regardless of cost |
| 3 | Shapes objective function — contractors as equal option vs. high-penalty option |
| 4 | Determines if contractor usage is a cost trade-off or a policy constraint |
| 5 | Affects model behavior during normal periods vs. peak periods |

---

## Question 4

**Current:** Who makes the final call on overtime authorization?

| # | Question Options |
|---|------------------|
| 1 | Who has authority to approve overtime — planners, supervisors, or management? |
| 2 | Is overtime a planning decision or an operational decision? |
| 3 | How far in advance is overtime authorized? |
| 4 | Are there approval thresholds that affect when overtime can be used? |
| 5 | Does the approval process constrain how overtime is planned? |

**Current Context:** Determines if OT is a planning decision or operational decision

| # | Context Options |
|---|-----------------|
| 1 | If planning decision, model can recommend OT as part of the plan |
| 2 | If operational, model may need to treat OT as constrained or last-resort |
| 3 | Affects how actionable model recommendations are |
| 4 | Shapes whether OT is proactive (planned) or reactive (day-of) |
| 5 | Determines ownership of OT decisions |

---

## Question 5

**Current:** Can work be shifted between periods, or must it be done when scheduled?

| # | Question Options |
|---|------------------|
| 1 | Can work be moved between periods to balance capacity, or is timing fixed? |
| 2 | How flexible is the timing of work — can it slide forward or back? |
| 3 | Is there work that can be pulled forward or pushed to smooth demand? |
| 4 | What determines whether work can be rescheduled? |
| 5 | How much flexibility exists to shift non-urgent work across periods? |

**Current Context:** Determines if model can smooth demand across time

| # | Context Options |
|---|-----------------|
| 1 | If flexible, model can balance workload across periods — reducing peaks |
| 2 | If fixed, model must solve each period independently |
| 3 | Enables load-leveling — shift work from peak periods to slack periods |
| 4 | Affects feasibility — rigid timing creates artificial constraints |
| 5 | Distinguishes work with hard deadlines from work with soft timing |

---

# SLIDE 9: OUTPUTS

## Question 1

**Current:** What decisions do you need to make from these outputs?

| # | Question Options |
|---|------------------|
| 1 | What actions will you take based on model output? |
| 2 | How will you use the plan — for staffing, budgeting, scheduling? |
| 3 | What decisions are you trying to support with this model? |
| 4 | Who needs to act on this information, and what do they need to decide? |
| 5 | What's the outcome you're driving toward with these outputs? |

**Current Context:** Ensures we produce actionable information

| # | Context Options |
|---|-----------------|
| 1 | Output must support real decisions — otherwise it's just reporting |
| 2 | Shapes format, granularity, and content of model outputs |
| 3 | Determines what's essential vs. nice-to-have |
| 4 | Connects model to action — not just insight |
| 5 | Informs how outputs are presented and to whom |

---

## Question 2

**Current:** What level of detail do you need? (monthly, weekly, by district, by grade?)

| # | Question Options |
|---|------------------|
| 1 | At what level of detail do you need to see the plan? |
| 2 | Should outputs be monthly or weekly? By district, by grade, or aggregated? |
| 3 | What granularity is actionable for your planning process? |
| 4 | Do different stakeholders need different levels of detail? |
| 5 | Is there a summary view and a detailed view needed? |

**Current Context:** Determines model granularity

| # | Context Options |
|---|-----------------|
| 1 | Higher granularity = more precision but more complexity |
| 2 | Model granularity should match decision granularity |
| 3 | Too detailed = noise; too aggregated = not actionable |
| 4 | May need roll-up views for management and detail views for planners |
| 5 | Affects model size and solve time |

---

## Question 3

**Current:** Do you need to compare scenarios? (e.g., "what if 2 more techs?")

| # | Question Options |
|---|------------------|
| 1 | Do you need to run and compare multiple scenarios? |
| 2 | Would "what-if" analysis be valuable — e.g., different headcount assumptions? |
| 3 | How important is scenario comparison to your planning process? |
| 4 | What scenarios would you want to test? |
| 5 | Is the goal a single optimal plan, or options to choose from? |

**Current Context:** Confirms scenario capability is needed

| # | Context Options |
|---|-----------------|
| 1 | Scenario analysis enables sensitivity testing and option comparison |
| 2 | Supports business cases — "if we add 2 techs, we reduce OT by X%" |
| 3 | Determines if model is run once or iteratively |
| 4 | Shapes user interface and workflow |
| 5 | Enables proactive planning vs. single-point forecast |

---

## Question 4

**Current:** Who consumes these outputs? (planners only, or also management, finance?)

| # | Question Options |
|---|------------------|
| 1 | Who are the audiences for model output? |
| 2 | Beyond planners, who needs to see or act on this information? |
| 3 | Do different stakeholders need different views or formats? |
| 4 | How will outputs be shared — reports, dashboards, presentations? |
| 5 | What level of detail does each audience need? |

**Current Context:** May need different views for different audiences

| # | Context Options |
|---|-----------------|
| 1 | Different audiences = different views, formats, and granularity |
| 2 | Planners need detail; management needs summary; finance needs cost |
| 3 | Shapes output design and delivery mechanism |
| 4 | May require multiple report formats |
| 5 | Determines communication and rollout needs |

---

## Question 5

**Current:** How do you track actuals vs. plan today?

| # | Question Options |
|---|------------------|
| 1 | How do you compare what happened vs. what was planned? |
| 2 | Is there a process to track plan accuracy and variance? |
| 3 | What metrics do you use to measure planning effectiveness? |
| 4 | How is feedback incorporated to improve future plans? |
| 5 | What does "good planning" look like when you evaluate results? |

**Current Context:** Informs how outputs should be structured for comparison

| # | Context Options |
|---|-----------------|
| 1 | Enables closed-loop planning — plan, execute, measure, improve |
| 2 | Shapes output format to align with actuals tracking |
| 3 | Supports continuous improvement and model calibration |
| 4 | Determines success metrics for the model |
| 5 | Informs whether variance analysis should be built into outputs |

---

# END OF OPTIONS
