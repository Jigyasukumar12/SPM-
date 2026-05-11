# UNIT 4: Project Management aur Control

**Is unit me kya-kya aayega:**

- Management aur control framework
- Data collection methods
- Progress visualization
- Cost monitoring
- Earned Value Analysis (EVA) - IMPORTANT
- Project tracking
- Change control
- Software Configuration Management (SCM)
- Contract management

---

## 📌 Framework for Project Management & Control

> 🔴 **Tier A** | Frequency: 3/4 | Section: C (Always!)

### Definition

**Project management** = Plan banate hain; **Control** = Actual vs planned compare karte hain.

**Management Control Framework** ek systematic structure hota hai processes, tools aur techniques ka jo project performance monitor karte hain, deviations identify karte hain aur corrective actions lete hain project ko on-track rakhne ke liye.

### Key Components

**1. Planning**

- Set baselines (scope, schedule, cost, quality)
- Define metrics and KPIs
- Establish reporting frequency
- Create control thresholds

**2. Monitoring**

- Collect actual performance data
- Measure against baselines
- Track variances
- Identify trends

**3. Controlling**

- Analyze root causes of variances
- Take corrective actions
- Implement preventive measures
- Update forecasts

**4. Reporting**

- Status reports to stakeholders
- Dashboard visualization
- Exception reporting
- Lessons learned documentation

### Control Cycle (Deming Cycle / PDCA)

**Plan:**

- Define objectives and processes
- Set performance standards
- Create detailed plans

**Do:**

- Execute planned activities
- Implement processes
- Collect data

**Check:**

- Measure actual performance
- Compare with standards
- Identify gaps

**Act:**

- Correct deviations
- Improve processes
- Update plans

**Repeat continuously**

### Framework Layers

**Strategic Control:**

- **Level:** Executive, sponsor
- **Frequency:** Monthly/quarterly
- **Focus:** Portfolio alignment, ROI, strategic objectives
- **Metrics:** Business value delivered, NPV, market share
- **Example:** "Are we building right products for market?"

**Tactical Control:**

- **Level:** Project manager, steering committee
- **Frequency:** Weekly/bi-weekly
- **Focus:** Schedule, budget, scope, quality
- **Metrics:** SPI, CPI, defect rates, milestone achievement
- **Example:** "Are we on track for Q3 release?"

**Operational Control:**

- **Level:** Team leads, developers
- **Frequency:** Daily
- **Focus:** Task completion, blockers, immediate issues
- **Metrics:** Story points completed, build success rate, code coverage
- **Example:** "Which tasks finished today? Any blockers?"

### Data Collection Methods

**1. Automated Data Collection**

- **Source:** Tools and systems
- **Examples:**
  - Version control (commits, branches)
  - CI/CD pipelines (build status, test results)
  - Time tracking tools (hours logged)
  - Project management software (task status)
- **Advantages:** Real-time, accurate, no manual effort
- **Disadvantages:** Requires tool integration

**2. Manual Status Reports**

- **Source:** Team members
- **Examples:**
  - Daily standups (verbal updates)
  - Timesheets (hours by task)
  - Progress reports (% complete)
- **Advantages:** Captures qualitative info, flexible
- **Disadvantages:** Time-consuming, subjective

**3. Reviews and Inspections**

- **Source:** Formal reviews
- **Examples:**
  - Code reviews (quality metrics)
  - Sprint reviews (demo of work)
  - Quality audits (compliance checks)
- **Advantages:** In-depth assessment, peer validation
- **Disadvantages:** Resource-intensive

**4. Surveys and Feedback**

- **Source:** Stakeholders
- **Examples:**
  - User satisfaction surveys
  - Team morale assessments
  - Customer feedback
- **Advantages:** Direct stakeholder input
- **Disadvantages:** Response bias, delayed

### Visualizing Progress

**1. Burndown Chart**

- **What:** Shows work remaining over time
- **X-axis:** Time (days/sprints)
- **Y-axis:** Work remaining (story points/tasks)
- **Ideal line:** Straight diagonal from start to zero
- **Actual line:** Real progress
- **Interpretation:**
  - Actual below ideal = Ahead of schedule
  - Actual above ideal = Behind schedule
  - Flat line = No progress (blockers)

**2. Burnup Chart**

- **What:** Shows work completed over time
- **Two lines:**
  - Total scope (may change)
  - Work completed
- **Advantage:** Shows scope changes clearly
- **When scope increases:** Gap widens

**3. Gantt Chart with Progress**

- **What:** Bars showing task duration with % complete shading
- **Visual:** Partially filled bars indicate progress
- **Example:** Task bar 60% filled in green = 60% complete

**4. Dashboard/Scorecard**

- **What:** Single-page view of key metrics
- **Elements:**
  - Traffic lights (Red/Amber/Green)
  - KPI values with trend arrows
  - Charts and graphs
- **Example Metrics:**
  - SPI: 0.95 ↓ (Red)
  - CPI: 1.05 ↑ (Green)
  - Defects: 45 ↓ (Amber)

**5. Milestone Chart**

- **What:** Key deliverables with planned vs actual dates
- **Symbols:**
  - ◇ Planned milestone
  - ◆ Completed milestone
  - ⚠ At-risk milestone

**6. S-Curve**

- **What:** Cumulative cost/work over time
- **Shape:** S-shaped curve (slow start, steep middle, slow end)
- **Uses:** Compare planned vs actual spending
- **Analysis:** If actual above planned = overspending

### Control Thresholds

**Variance Thresholds:**

- **Green:** ±5% variance (acceptable)
- **Amber:** 5-10% variance (monitor closely)
- **Red:** >10% variance (immediate action)

**Escalation Rules:**

- Amber: Team lead handles
- Red: Project manager involved
- > 20%: Escalate to sponsor

**Example:**

- Budget: $100,000
- Actual: $112,000
- Variance: 12% (Red)
- Action: Escalate to sponsor, review spend, identify savings

### Management by Exception

**Principle:** Focus on significant deviations only

**Process:**

1. Define acceptable variance ranges
2. Monitor metrics
3. Flag only out-of-range items
4. Investigate and act on exceptions
5. Routine items proceed without intervention

**Benefits:**

- Efficient use of management time
- Focus on problems, not routine operations
- Empowers team to handle normal variations

**Example:**

- 95 out of 100 tasks on track → Don't report these
- 5 tasks delayed >3 days → Report and address these

![Management Control Framework](diagrams/management_control_framework.svg)

---

## 📌 Earned Value Analysis (EVA)

> 🔴 **Tier A** | Frequency: 4/4 | Section: A + B + C (Numerical Guaranteed!)

### Definition

**Earned Value Analysis (EVA)** is a project performance measurement technique that integrates scope, schedule, and cost to assess project health and forecast future performance.

### Three Core Values

**1. Planned Value (PV) - Budgeted Cost of Work Scheduled**

- **Definition:** How much work should have been done by now (in monetary terms)
- **Formula:** Planned % complete × Budget at Completion (BAC)
- **Also called:** BCWS (Budgeted Cost of Work Scheduled)
- **Example:**
  - BAC = $100,000
  - Planned to be 40% complete by today
  - PV = 0.40 × $100,000 = $40,000

**2. Earned Value (EV) - Budgeted Cost of Work Performed**

- **Definition:** Value of work actually completed (in monetary terms)
- **Formula:** Actual % complete × BAC
- **Also called:** BCWP (Budgeted Cost of Work Performed)
- **Example:**
  - BAC = $100,000
  - Actually 35% complete
  - EV = 0.35 × $100,000 = $35,000

**3. Actual Cost (AC) - Actual Cost of Work Performed**

- **Definition:** How much was actually spent
- **Also called:** ACWP (Actual Cost of Work Performed)
- **Example:**
  - Actually spent = $38,000
  - AC = $38,000

### Key Performance Indicators

**1. Schedule Variance (SV)**

```
SV = EV - PV

Interpretation:
- SV > 0: Ahead of schedule (earned more than planned)
- SV = 0: On schedule
- SV < 0: Behind schedule (earned less than planned)
```

**Example:**

- EV = $35,000
- PV = $40,000
- SV = $35,000 - $40,000 = -$5,000 (Behind schedule)

**2. Cost Variance (CV)**

```
CV = EV - AC

Interpretation:
- CV > 0: Under budget (earned more than spent)
- CV = 0: On budget
- CV < 0: Over budget (spent more than earned)
```

**Example:**

- EV = $35,000
- AC = $38,000
- CV = $35,000 - $38,000 = -$3,000 (Over budget)

**3. Schedule Performance Index (SPI)**

```
SPI = EV / PV

Interpretation:
- SPI > 1.0: Ahead of schedule (e.g., 1.10 = 10% ahead)
- SPI = 1.0: On schedule
- SPI < 1.0: Behind schedule (e.g., 0.90 = 10% behind)
```

**Example:**

- EV = $35,000
- PV = $40,000
- SPI = $35,000 / $40,000 = 0.875 (12.5% behind schedule)

**4. Cost Performance Index (CPI)**

```
CPI = EV / AC

Interpretation:
- CPI > 1.0: Under budget (e.g., 1.10 = getting $1.10 value per $1 spent)
- CPI = 1.0: On budget
- CPI < 1.0: Over budget (e.g., 0.90 = getting $0.90 value per $1 spent)
```

**Example:**

- EV = $35,000
- AC = $38,000
- CPI = $35,000 / $38,000 = 0.921 (Getting $0.92 value per dollar)

### Forecasting Formulas

**5. Estimate at Completion (EAC)**

**Predicts total cost at project completion based on current performance.**

**Method 1: CPI Only Influences (Most Common)**

```
EAC = BAC / CPI

Use when: Current cost performance will continue
```

**Method 2: Both SPI and CPI Influence**

```
EAC = AC + [(BAC - EV) / (CPI × SPI)]

Use when: Both cost and schedule variances affect future work
```

**Method 3: New Estimate**

```
EAC = AC + Bottom-up estimate for remaining work

Use when: Past performance is not indicative (major changes)
```

**Method 4: Atypical Variance**

```
EAC = AC + (BAC - EV)

Use when: Current variance is one-time, won't recur
```

**6. Estimate to Complete (ETC)**

```
ETC = EAC - AC

How much more will be spent to complete project
```

**7. Variance at Completion (VAC)**

```
VAC = BAC - EAC

Interpretation:
- VAC > 0: Will finish under budget
- VAC = 0: Will finish on budget
- VAC < 0: Will finish over budget
```

**8. To-Complete Performance Index (TCPI)**

```
TCPI (based on BAC) = (BAC - EV) / (BAC - AC)

TCPI (based on EAC) = (BAC - EV) / (EAC - AC)

Interpretation:
- TCPI > 1.0: Need to improve efficiency
- TCPI = 1.0: Maintain current performance
- TCPI < 1.0: Can afford to relax
```

### Complete EVA Example

**Given:**

- **Budget at Completion (BAC):** $22,000
- **Earned Value (EV):** $13,000
- **Planned Value (PV):** $14,000
- **Actual Cost (AC):** $15,000

**Calculate: SV, CV, SPI, CPI, EAC (both methods), ETC, VAC**

**Step 1: Variances**

```
SV = EV - PV = $13,000 - $14,000 = -$1,000
Interpretation: $1,000 behind schedule

CV = EV - AC = $13,000 - $15,000 = -$2,000
Interpretation: $2,000 over budget
```

**Step 2: Performance Indices**

```
SPI = EV / PV = $13,000 / $14,000 = 0.929
Interpretation: 93% schedule efficiency (7% behind)

CPI = EV / AC = $13,000 / $15,000 = 0.867
Interpretation: Getting $0.87 value per $1 spent (13% over budget)
```

**Step 3: Estimate at Completion**

**Method 1: CPI Only**

```
EAC = BAC / CPI = $22,000 / 0.867 = $25,375
```

**Method 2: Both SPI and CPI Influence**

```
EAC = AC + [(BAC - EV) / (CPI × SPI)]
    = $15,000 + [($22,000 - $13,000) / (0.867 × 0.929)]
    = $15,000 + [$9,000 / 0.806]
    = $15,000 + $11,166
    = $26,166
```

**Step 4: Estimate to Complete**

```
ETC = EAC - AC = $25,375 - $15,000 = $10,375 (using Method 1)
```

**Step 5: Variance at Completion**

```
VAC = BAC - EAC = $22,000 - $25,375 = -$3,375
Interpretation: Will finish $3,375 over budget
```

**Summary Table:**

| Metric  | Formula   | Value   | Interpretation         |
| ------- | --------- | ------- | ---------------------- |
| **SV**  | EV - PV   | -$1,000 | Behind schedule        |
| **CV**  | EV - AC   | -$2,000 | Over budget            |
| **SPI** | EV / PV   | 0.929   | 7% behind schedule     |
| **CPI** | EV / AC   | 0.867   | 13% over budget        |
| **EAC** | BAC / CPI | $25,375 | Projected total cost   |
| **ETC** | EAC - AC  | $10,375 | Cost to complete       |
| **VAC** | BAC - EAC | -$3,375 | Will overrun by $3,375 |

**Management Actions:**

Based on CPI = 0.867 and SPI = 0.929:

**Immediate Actions:**

1. **Cost Control:**
   - Review all expenditures
   - Identify cost-saving opportunities
   - Reduce scope if possible
   - Negotiate vendor rates

2. **Schedule Recovery:**
   - Add resources to critical path
   - Increase work hours (if sustainable)
   - Parallelize tasks
   - Fast-track activities

3. **Stakeholder Communication:**
   - Inform sponsor of $3,375 projected overrun
   - Present recovery options
   - Request additional budget if justified
   - Reset expectations on delivery date

### EVA with Activity-Level Detail

**Scenario:** Two activities, need to calculate project-level metrics

**Given:**

- **Activity A:**
  - Planned Value: ₹1,80,000
  - Actual Cost: ₹2,00,000
  - % Complete: 100%
- **Activity B:**
  - Planned Value: ₹80,000
  - Actual Cost: ₹1,00,000
  - % Complete: 75%

**Calculate: Project SPI and CPI**

**Solution:**

**Activity A:**

```
PV(A) = ₹1,80,000
AC(A) = ₹2,00,000
EV(A) = 100% × ₹1,80,000 = ₹1,80,000
```

**Activity B:**

```
PV(B) = ₹80,000
AC(B) = ₹1,00,000
EV(B) = 75% × ₹80,000 = ₹60,000
```

**Project Totals:**

```
Total PV = ₹1,80,000 + ₹80,000 = ₹2,60,000
Total AC = ₹2,00,000 + ₹1,00,000 = ₹3,00,000
Total EV = ₹1,80,000 + ₹60,000 = ₹2,40,000
```

**Project Performance:**

```
SPI = Total EV / Total PV = ₹2,40,000 / ₹2,60,000 = 0.923
Interpretation: 7.7% behind schedule

CPI = Total EV / Total AC = ₹2,40,000 / ₹3,00,000 = 0.80
Interpretation: Getting ₹0.80 value per ₹1 spent (20% over budget)
```

**Status:** Project is behind schedule and over budget.

### EVA Benefits

**1. Integrated Measurement:**

- Combines scope, schedule, cost in single framework
- Holistic view of project health

**2. Early Warning:**

- Identifies problems early
- CPI stabilizes after 20% completion (reliable predictor)

**3. Objective Assessment:**

- Quantitative, not subjective
- Data-driven decisions

**4. Forecasting:**

- Predicts final cost and schedule
- Enables proactive management

**5. Stakeholder Communication:**

- Clear, standardized metrics
- Easy to understand trends

### EVA Limitations

**1. Data Accuracy:**

- Depends on accurate % complete estimates
- Garbage in, garbage out

**2. Doesn't Show Root Causes:**

- Tells you there's a problem, not why
- Needs supplementary analysis

**3. Complex for Simple Projects:**

- Overhead not justified for small projects
- Best for projects >$1M, >6 months

**4. Assumes Linear Progress:**

- May not suit iterative/Agile projects
- Works best for waterfall

![Earned Value Analysis](diagrams/earned_value_analysis.svg)

---

## 📌 Software Configuration Management (SCM)

> 🟡 **Tier B** | Frequency: 2/4 | Section: A + B

### Definition

**SCM** is the practice of tracking and controlling changes in software artifacts (code, documents, designs) throughout the project lifecycle to maintain integrity and traceability.

### Four Key Activities

**1. Configuration Identification**

- **What:** Identify items to be controlled
- **How:** Define Configuration Items (CIs)
- **Examples of CIs:**
  - Source code files
  - Executables and libraries
  - Documentation (requirements, design, user manuals)
  - Test cases and scripts
  - Database schemas
  - Configuration files
- **Naming Convention:** Unique identifiers for each CI
- **Baseline:** Approved version of CI at specific point

**2. Configuration Control (Change Control)**

- **What:** Manage changes to CIs
- **Process:**
  1. Submit change request
  2. Impact analysis (cost, schedule, technical)
  3. Change Control Board (CCB) reviews
  4. Approve/reject/defer decision
  5. Implement if approved
  6. Verify change
  7. Update baselines
- **Why:** Prevent unauthorized or harmful changes

**3. Configuration Status Accounting**

- **What:** Record and report status of CIs
- **Information Tracked:**
  - What items exist (inventory)
  - Current version of each
  - Who changed what when why
  - Status (in development, tested, released)
  - Which changes approved/implemented
- **Tools:** Version control systems, databases
- **Reports:** "Which version is in production?", "All changes in Release 2.0"

**4. Configuration Audit**

- **What:** Verify CIs conform to standards
- **Types:**
  - **Functional:** Does CI meet requirements?
  - **Physical:** Does actual match documentation?
- **When:** Before major releases, periodic reviews
- **Output:** Audit report with discrepancies, corrective actions

### Version Control Concepts

**Version:**

- Specific state of CI at point in time
- Example: MyApp v1.0, v1.1, v2.0

**Revision:**

- Minor update to version
- Example: MyApp v1.0.1, v1.0.2

**Baseline:**

- Formally approved version
- Reference point for future changes
- Types:
  - Functional baseline (requirements approved)
  - Allocated baseline (design approved)
  - Product baseline (released product)

**Branch:**

- Parallel development line
- Example: Master branch (production), develop branch (new features), hotfix branch

**Merge:**

- Combine changes from different branches
- Requires conflict resolution if same lines changed

**Tag/Label:**

- Meaningful name for specific version
- Example: "Release_2.0", "Beta_Candidate"

### Tools

**Version Control Systems:**

- **Git:** Distributed, branching model, most popular
- **SVN:** Centralized, linear history
- **Mercurial:** Distributed, simpler than Git

**Build Tools:**

- **Maven, Gradle:** Java projects
- **npm:** JavaScript projects
- Automate compilation, dependency management

**CI/CD Tools:**

- **Jenkins, GitLab CI, GitHub Actions**
- Automated build, test, deploy on commits

**Configuration Databases:**

- **CMDB (Configuration Management Database)**
- Stores all CI metadata, relationships

### SCM Benefits

**1. Traceability:**

- Track every change: who, what, when, why
- Audit trail for compliance

**2. Reproducibility:**

- Rebuild any past version exactly
- Example: Customer reports bug in v1.5 → Recreate v1.5 environment

**3. Concurrent Development:**

- Multiple developers work on different features simultaneously
- Branching and merging

**4. Backup and Recovery:**

- Entire history preserved
- Revert to working version if new changes break system

**5. Release Management:**

- Clear identification of what's in each release
- Simplifies deployment

**6. Quality Assurance:**

- Ensure only tested, approved code in production
- Prevent accidental introduction of bugs

---

## 📌 Change Control

> 🟡 **Tier B** | Frequency: 2/4 | Section: A + C

### Definition

**Change Control** is the formal process to evaluate, approve, and implement changes to project scope, schedule, cost, or deliverables while maintaining project integrity.

### Why Change Control Needed

**Problems Without Change Control:**

- Scope creep (endless additions)
- Chaos (uncontrolled changes)
- Broken baselines (can't measure progress)
- Budget overruns
- Missed deadlines
- Team demoralization

**Benefits of Change Control:**

- Prevents unauthorized changes
- Evaluates impact before implementing
- Maintains project baselines
- Documents decisions and rationale
- Protects project from thrashing

### Change Control Process

**Step 1: Submit Change Request**

- **Who:** Anyone (customer, team, stakeholder)
- **How:** Formal change request form
- **Contents:**
  - Description of change
  - Justification (why needed)
  - Priority (critical, high, medium, low)
  - Submitter information

**Example:**

```
Change Request #CR-045
Submitted by: Product Manager
Date: May 10, 2026
Description: Add export to Excel feature in Reports module
Justification: Customer requirement, competitive necessity
Priority: High
```

**Step 2: Impact Analysis**

- **Who:** Project manager, technical lead
- **Assess:**
  - **Scope:** What deliverables affected?
  - **Schedule:** How many days/weeks delay?
  - **Cost:** Additional budget needed?
  - **Resources:** Extra people or skills?
  - **Quality:** Risks introduced?
  - **Other projects:** Dependencies affected?
- **Output:** Impact assessment report

**Example:**

```
Impact Analysis for CR-045:
- Scope: New feature in Reports module
- Schedule: +2 weeks
- Cost: +$5,000 (developer time, testing)
- Resources: 1 developer, 1 tester for 2 weeks
- Quality: Low risk (isolated module)
- Dependencies: None
- Recommendation: Approve, schedule in Sprint 8
```

**Step 3: Evaluation by Change Control Board (CCB)**

- **Members:**
  - Project manager (chair)
  - Technical lead
  - Business owner/product manager
  - Quality assurance lead
  - Affected stakeholder representatives
- **Meeting Frequency:** Weekly or bi-weekly
- **Agenda:**
  - Review new change requests
  - Assess impact reports
  - Make decisions
  - Prioritize approved changes

**Step 4: Decision**

- **Approve:** Implement change
- **Reject:** Do not implement, document reason
- **Defer:** Postpone to future release
- **Request More Info:** Send back for clarification

**Decision Criteria:**

- Alignment with project objectives
- Business value vs. cost
- Impact on schedule (acceptable delay?)
- Resource availability
- Risk level

**Step 5: Implementation (if Approved)**

- Update project plan (schedule, budget, scope)
- Assign resources
- Develop/test change
- Update documentation
- Communicate to stakeholders

**Step 6: Verification**

- Test that change works as intended
- Ensure no negative side effects
- Get user acceptance

**Step 7: Close Change Request**

- Update change log
- Update baselines
- Communicate completion
- Archive documentation

### Change Request Log

| CR #   | Date   | Submitter | Description  | Priority | Status   | Decision Date | Approved By | Impact (Days/Cost) |
| ------ | ------ | --------- | ------------ | -------- | -------- | ------------- | ----------- | ------------------ |
| CR-045 | May 10 | PM        | Excel export | High     | Approved | May 12        | CCB         | +2 weeks / $5K     |
| CR-046 | May 11 | Customer  | New report   | Medium   | Deferred | May 12        | CCB         | Sprint 10          |
| CR-047 | May 11 | Dev       | Tech debt    | Low      | Rejected | May 12        | CCB         | Not aligned        |

### Types of Changes

**1. Scope Changes:**

- Add/remove features
- Modify requirements
- **Example:** Add mobile app version (was web-only)

**2. Schedule Changes:**

- Extend/compress timeline
- Shift milestones
- **Example:** Move go-live from June to August

**3. Resource Changes:**

- Add/remove team members
- Change skill mix
- **Example:** Add UX designer mid-project

**4. Technical Changes:**

- Change technology stack
- Modify architecture
- **Example:** Switch from MySQL to PostgreSQL

**5. Process Changes:**

- Change methodology
- Modify workflows
- **Example:** Switch from Waterfall to Agile

### Emergency Changes

**When:** Critical production issues
**Process:** Expedited

- Verbal approval from sponsor
- Implement immediately
- Retrospective CCB review within 24 hours
- Document decision

**Example:** Security vulnerability discovered in production → Patch immediately, inform CCB next day

### Change Control Best Practices

**1. Formal Process:**

- Written procedures
- Standard forms
- Clear approval authority

**2. Single Entry Point:**

- All changes through CCB (no backdoor approvals)
- Prevents chaos

**3. Impact Analysis Mandatory:**

- Never approve without understanding impact
- Data-driven decisions

**4. Communicate Decisions:**

- Inform requestor of decision and reason
- Build understanding, not resentment

**5. Track Metrics:**

- Number of changes requested
- Approval rate
- Average cycle time
- Impact on schedule/cost

**6. Review Trends:**

- Many changes = requirements were poor
- High rejection rate = unrealistic expectations
- Learn and improve

---

## 📌 Contract Management

> 🟡 **Tier B** | Frequency: 2/4 | Section: C

### Definition

**Contract Management** is the process of managing agreements with vendors, contractors, and suppliers to ensure deliverables, costs, and timelines are met per contractual obligations.

### Types of Contracts

**1. Fixed Price (Lump Sum)**

- **What:** Vendor delivers for fixed total price
- **Risk:** Vendor bears cost overrun risk
- **Best For:** Well-defined scope, stable requirements
- **Buyer Advantage:** Predictable cost, budget certainty
- **Vendor Risk:** If scope grows or complexity underestimated, vendor loses money
- **Example:** "Build customer portal for $50,000"

**2. Time & Materials (T&M)**

- **What:** Pay for actual time and materials used
- **Risk:** Buyer bears cost overrun risk
- **Best For:** Unclear scope, evolving requirements
- **Buyer Risk:** Unlimited costs if not managed
- **Vendor Advantage:** No risk, paid for all work
- **Controls:** Cap on total hours or cost
- **Example:** "Developer at $100/hour, max 500 hours ($50,000)"

**3. Cost Plus (Cost Reimbursable)**

- **What:** Pay vendor's costs + fixed fee or % profit
- **Risk:** Buyer bears cost risk
- **Best For:** Research, high uncertainty
- **Variants:**
  - **Cost Plus Fixed Fee (CPFF):** Costs + $10,000 fee
  - **Cost Plus Percentage (CPP):** Costs + 10% profit
  - **Cost Plus Incentive Fee (CPIF):** Costs + bonus if meet targets
- **Example:** "Actual costs + $15,000 fee"

**4. Unit Price**

- **What:** Fixed price per unit of work
- **Risk:** Shared (quantity uncertainty)
- **Best For:** Repetitive work, unclear total quantity
- **Example:** "Data migration: $5 per record migrated"

### Contract Life Cycle

**Phase 1: Procurement Planning**

- Identify what to outsource
- Define requirements (SOW - Statement of Work)
- Choose contract type
- Set evaluation criteria

**Phase 2: Vendor Selection**

- **RFP (Request for Proposal):** Formal invitation to vendors
- Receive proposals
- Evaluate proposals against criteria (cost, experience, quality, timeline)
- Negotiate terms
- Award contract

**Phase 3: Contract Execution**

- Kick-off meeting
- Vendor delivers per schedule
- Buyer monitors progress
- Invoice processing and payments

**Phase 4: Contract Monitoring & Control**

- Track deliverables against SLA
- Measure quality (defect rates, performance)
- Issue resolution
- Change requests (contract amendments)
- Performance reviews

**Phase 5: Contract Closure**

- Final deliverable acceptance
- Final payment
- Lessons learned
- Archive documentation
- Release vendor from obligations

### Key Contract Clauses

**1. Scope of Work (SOW):**

- Detailed description of deliverables
- Acceptance criteria
- **Example:** "Develop mobile app with features A, B, C; support iOS 14+, Android 10+"

**2. Payment Terms:**

- Milestone-based payments
- Example: "30% on design approval, 50% on UAT pass, 20% on go-live"
- Payment schedule (Net 30, Net 60)

**3. Timeline and Milestones:**

- Delivery dates
- Penalties for late delivery (liquidated damages)
- **Example:** "$500/day penalty for each day past deadline"

**4. Quality Standards:**

- Acceptance criteria
- Defect limits
- **Example:** "< 5 critical bugs, < 20 medium bugs at UAT"

**5. Intellectual Property (IP):**

- Who owns deliverables?
- **Work for Hire:** Buyer owns all IP
- **License:** Vendor retains IP, buyer gets license

**6. Warranties:**

- Vendor guarantees deliverable works
- **Example:** "90-day warranty, all defects fixed free"

**7. Termination Clause:**

- Conditions for early termination
- **For Cause:** Breach of contract
- **For Convenience:** Buyer can terminate anytime (pay for work done)

**8. Dispute Resolution:**

- Mediation, arbitration, or litigation
- Jurisdiction

**9. Confidentiality (NDA):**

- Protect proprietary information
- Non-disclosure of trade secrets

**10. Liability and Indemnity:**

- Limits on damages
- Insurance requirements

### Managing Vendor Performance

**1. Service Level Agreements (SLAs):**

- Measurable performance targets
- **Examples:**
  - System uptime: 99.9%
  - Response time: < 2 seconds
  - Support response: < 4 hours for critical issues
  - Defect fix: 90% within 3 business days

**2. Key Performance Indicators (KPIs):**

- Metrics to track vendor performance
- **Examples:**
  - On-time delivery rate
  - Defect density (bugs per 1000 LOC)
  - Customer satisfaction score

**3. Performance Reviews:**

- **Frequency:** Monthly or quarterly
- **Agenda:**
  - Review KPIs and SLAs
  - Discuss issues and resolutions
  - Identify improvement areas
  - Plan upcoming work

**4. Incentives and Penalties:**

- **Incentives:** Bonus for early delivery, exceeding quality
- **Penalties:** Liquidated damages for delays, quality failures
- **Example:** "$10,000 bonus if delivered 2 weeks early, $5,000 penalty if 1 week late"

### Contract Challenges

**1. Scope Creep:**

- Vendor delivers more/less than agreed
- **Solution:** Clear SOW, change control process

**2. Communication Gaps:**

- Misunderstandings lead to wrong deliverables
- **Solution:** Regular status meetings, documentation

**3. Quality Issues:**

- Deliverables don't meet standards
- **Solution:** Clear acceptance criteria, testing, warranties

**4. Cost Overruns (T&M contracts):**

- Costs spiral without controls
- **Solution:** Cap total costs, approve time in advance

**5. Delays:**

- Vendor misses deadlines
- **Solution:** Milestone tracking, penalties, contingency plans

**6. IP Disputes:**

- Disagreement on ownership
- **Solution:** Explicit IP clause in contract

### Contract Management Best Practices

**1. Clear, Detailed Contracts:**

- No ambiguity in scope, quality, timeline
- Get legal review

**2. Risk Allocation:**

- Match contract type to risk profile
- Fixed price for low risk, T&M for high uncertainty

**3. Regular Monitoring:**

- Weekly status reviews
- Track against milestones
- Early detection of issues

**4. Relationship Management:**

- Treat vendor as partner, not adversary
- Win-win mindset

**5. Documentation:**

- Record all communications
- Change requests in writing
- Audit trail

**6. Escalation Path:**

- Define who resolves disputes
- Example: PM level → Director level → Legal

**7. Exit Strategy:**

- Plan for contract end or termination
- Knowledge transfer
- Transition to new vendor or in-house

---

## 🎯 PYQ MODEL ANSWERS

### 🎯 PYQ [2021-22] - "What do you mean by Project Management and Control?" (Section A, 2 marks)

**Model Answer:**

Project Management and Control is the systematic process of monitoring project performance against baselines (scope, schedule, cost, quality), identifying variances, and taking corrective actions. It involves data collection (actual progress, costs), visualizing status (dashboards, Gantt charts), analyzing deviations (SPI, CPI), and implementing controls (change management, resource reallocation) to ensure project meets objectives on time and within budget.

---

### 🎯 PYQ [2021-22] - "Define Framework for Management" (Section A, 2 marks)

**Model Answer:**

Framework for Management and Control is the structured system of processes, tools, and techniques used to monitor and control project execution. It includes four components: (1) Planning - set baselines and KPIs, (2) Monitoring - collect actual performance data, (3) Controlling - analyze variances and take corrective actions, (4) Reporting - communicate status to stakeholders. Operates at three levels: strategic (executive), tactical (project manager), operational (team).

---

### 🎯 PYQ [2021-22, 2022-23, 2023-24, 2024-25] - "Discuss about the concept and need of Cost monitoring Earned Value Analysis" OR "Calculate EAC, VAC when given BAC, EV, PV, AC" (Section B/C, 10/7 marks)

**Model Answer:**

**Introduction:**

Earned Value Analysis (EVA) is a project performance measurement technique that integrates scope, schedule, and cost data to provide objective assessment of project health and forecast future performance. It is essential for proactive project management, enabling early problem detection and data-driven decision-making.

**Core Concept:**

EVA compares three key values at any point in time:

**1. Planned Value (PV) - Budgeted Cost of Work Scheduled:**

- Amount of work that should have been completed by now (in monetary terms)
- Formula: Planned % complete × Budget at Completion (BAC)
- Represents the baseline plan
- Example: Project budget $100,000, planned to be 50% complete → PV = $50,000

**2. Earned Value (EV) - Budgeted Cost of Work Performed:**

- Value of work actually completed (in monetary terms)
- Formula: Actual % complete × BAC
- Measures actual progress
- Example: Actually 40% complete → EV = $40,000

**3. Actual Cost (AC) - Actual Cost of Work Performed:**

- Money actually spent to date
- From accounting records
- Example: Spent $45,000 → AC = $45,000

**Performance Metrics:**

**Schedule Performance:**

```
Schedule Variance (SV) = EV - PV
- SV > 0: Ahead of schedule
- SV < 0: Behind schedule

Schedule Performance Index (SPI) = EV / PV
- SPI > 1.0: Ahead (e.g., 1.10 = 10% ahead)
- SPI < 1.0: Behind (e.g., 0.90 = 10% behind)
```

**Cost Performance:**

```
Cost Variance (CV) = EV - AC
- CV > 0: Under budget
- CV < 0: Over budget

Cost Performance Index (CPI) = EV / AC
- CPI > 1.0: Under budget (e.g., 1.10 = getting $1.10 value per $1 spent)
- CPI < 1.0: Over budget (e.g., 0.90 = getting $0.90 value per $1 spent)
```

**Forecasting Formulas:**

**Estimate at Completion (EAC):**
Predicts total project cost at completion

**Method 1: CPI Only Influences (Most Common)**

```
EAC = BAC / CPI

Assumption: Current cost performance will continue
Use when: No major changes expected
```

**Method 2: Both SPI and CPI Influence**

```
EAC = AC + [(BAC - EV) / (CPI × SPI)]

Assumption: Both cost and schedule variances affect future
Use when: Schedule delays cause cost impacts
```

**Variance at Completion (VAC):**

```
VAC = BAC - EAC

- VAC > 0: Will finish under budget
- VAC = 0: Will finish on budget
- VAC < 0: Will finish over budget
```

**Need for Cost Monitoring and EVA:**

**1. Integrated Performance Measurement:**

- **Problem:** Traditional methods track cost and schedule separately
  - "We're on budget" + "We're behind schedule" → Net status unclear
- **EVA Solution:** Integrates both → "We've spent $45K to complete $40K worth of work while $50K should be done" → Clear: over budget AND behind schedule

**2. Early Warning System:**

- **Problem:** Issues detected late (when 80% spent, realize only 60% done)
- **EVA Solution:** CPI stabilizes after 20% completion → Reliable early predictor
- **Example:** At 20% complete, CPI = 0.85 → Alert: Will overrun by 15% if no action

**3. Objective Progress Assessment:**

- **Problem:** Subjective "90% complete" syndrome (tasks always 90% done)
- **EVA Solution:** Quantitative, based on deliverables completed
- **Example:** EV = completed features × budgeted cost → Objective measure

**4. Accurate Forecasting:**

- **Problem:** "We're 50% through timeline, so 50% through budget" → Often wrong
- **EVA Solution:** EAC predicts final cost based on actual performance trend
- **Example:** EAC = $120K (20% overrun) → Allows proactive budget revision

**5. Data-Driven Decisions:**

- **Problem:** Gut-feel decisions ("I think we're okay")
- **EVA Solution:** Quantitative basis for corrective actions
- **Example:** CPI = 0.80 → Need to improve efficiency by 25% OR accept 25% overrun

**6. Stakeholder Communication:**

- **Problem:** Complex status updates confuse stakeholders
- **EVA Solution:** Standard metrics (SPI, CPI) universally understood
- **Example:** Dashboard: SPI = 0.95 (Red), CPI = 1.05 (Green) → Behind schedule, under budget

**7. Trend Analysis:**

- **Problem:** Single-point data doesn't show direction
- **EVA Solution:** Track SPI/CPI over time → Identify improving or degrading trends
- **Example:** CPI decreasing from 1.05 → 1.00 → 0.95 → Warning: trend worsening

**Numerical Example:**

**Given:**

- Budget at Completion (BAC) = $22,000
- Earned Value (EV) = $13,000
- Planned Value (PV) = $14,000
- Actual Cost (AC) = $15,000

**Calculate: SPI, CPI, EAC (both methods), VAC**

**Solution:**

**Step 1: Performance Indices**

```
SPI = EV / PV = $13,000 / $14,000 = 0.929
Interpretation: 93% schedule efficiency → 7% behind schedule

CPI = EV / AC = $13,000 / $15,000 = 0.867
Interpretation: Getting $0.87 value per dollar → 13% over budget
```

**Step 2: Estimate at Completion**

**Method 1: CPI Only Influences**

```
EAC = BAC / CPI = $22,000 / 0.867 = $25,375

Interpretation: If current cost efficiency continues, project will cost $25,375
```

**Method 2: Both SPI and CPI Influence**

```
EAC = AC + [(BAC - EV) / (CPI × SPI)]
    = $15,000 + [($22,000 - $13,000) / (0.867 × 0.929)]
    = $15,000 + [$9,000 / 0.806]
    = $15,000 + $11,166
    = $26,166

Interpretation: If both cost and schedule variances affect future work, project will cost $26,166
```

**Step 3: Variance at Completion**

```
Using Method 1:
VAC = BAC - EAC = $22,000 - $25,375 = -$3,375

Interpretation: Project will overrun budget by $3,375 (15% overrun)
```

**Summary Table:**

| Metric         | Formula   | Value   | Status                    |
| -------------- | --------- | ------- | ------------------------- |
| SPI            | EV / PV   | 0.929   | 7% behind schedule        |
| CPI            | EV / AC   | 0.867   | 13% over budget           |
| EAC (Method 1) | BAC / CPI | $25,375 | Projected total cost      |
| EAC (Method 2) | Complex   | $26,166 | If both variances persist |
| VAC            | BAC - EAC | -$3,375 | Will overrun by 15%       |

**Management Actions Based on EVA Results:**

**Immediate Actions:**

**1. Cost Control (CPI = 0.867):**

- Conduct detailed cost review
- Identify inefficiencies
- Reduce discretionary spending
- Negotiate better vendor rates
- Consider scope reduction if acceptable

**2. Schedule Recovery (SPI = 0.929):**

- Add resources to critical path (if budget allows)
- Increase work hours temporarily
- Fast-track or crash schedule
- Parallelize activities

**3. Stakeholder Communication:**

- Inform sponsor of projected $3,375 overrun
- Present options:
  - Accept overrun and request additional funds
  - Reduce scope to stay in budget
  - Extend timeline to reduce cost (if time-cost trade-off exists)
- Reset expectations on delivery date

**4. Root Cause Analysis:**

- Why CPI low? (Underestimation? Inefficiency? Scope creep?)
- Why SPI low? (Dependencies? Resource shortages? Technical challenges?)
- Address root causes, not just symptoms

**5. Forecasting Updates:**

- Update EAC monthly as new data emerges
- Track if corrective actions improving CPI/SPI
- Adjust forecasts based on trends

**Preventive Measures for Future:**

**1. Improve Estimation:**

- Use historical CPI data for future estimates
- If past projects had CPI = 0.90, budget 10% more

**2. Frequent Monitoring:**

- Calculate EVA weekly or bi-weekly
- Detect problems at 10-20% completion, not 80%

**3. Performance-Based Contracts:**

- Tie vendor payments to EV, not just time spent
- Incentivizes efficiency

**Conclusion:**

Earned Value Analysis is essential for effective cost monitoring because it provides:

- **Integration:** Combines scope, schedule, cost in single framework
- **Objectivity:** Quantitative, not subjective assessments
- **Early Detection:** Problems identified early when corrective action cheaper
- **Forecasting:** Predicts final cost and schedule with reasonable accuracy
- **Communication:** Standard metrics understood by all stakeholders

Without EVA, project managers rely on lagging indicators (final cost) or subjective assessments ("looks good"). With EVA, they have leading indicators (CPI, SPI trends) enabling proactive management. This transforms project control from reactive firefighting to predictive, data-driven decision-making.

In the example, EVA clearly shows project is 7% behind schedule and 13% over budget, with projected 15% cost overrun. This quantifiable insight enables specific corrective actions (cost reduction, schedule compression) and informed stakeholder discussions (request more funds vs. reduce scope), ultimately improving project success probability.

---

### 🎯 PYQ [2022-23, 2023-24, 2024-25] - "You are managing a project which is six months of its execution. You are now reviewing the project status and you have ascertained that the project is behind schedule. The actual cost of Activity A is ₹2,00,000 and that of Activity B is ₹1,00,000. The planned value of these activities is ₹1,80,000 and ₹80,000 respectively. Activity A is 100% complete. However, Activity B is only 75% complete. Calculate the schedule performance index and cost performance index of the project on the review date." (Section C, 7/10 marks)

**Model Answer:**

**Given Data:**

| Activity | Planned Value (PV) | Actual Cost (AC) | % Complete |
| -------- | ------------------ | ---------------- | ---------- |
| A        | ₹1,80,000          | ₹2,00,000        | 100%       |
| B        | ₹80,000            | ₹1,00,000        | 75%        |

**Required:** Calculate SPI and CPI for the project

**Solution:**

**Step 1: Calculate Earned Value (EV) for Each Activity**

```
Earned Value = % Complete × Planned Value
(What's the budgeted cost of work actually completed?)
```

**Activity A:**

```
EV(A) = 100% × ₹1,80,000 = ₹1,80,000
```

**Activity B:**

```
EV(B) = 75% × ₹80,000 = ₹60,000
```

**Step 2: Calculate Project Totals**

```
Total Planned Value (PV) = PV(A) + PV(B)
                         = ₹1,80,000 + ₹80,000
                         = ₹2,60,000

Total Actual Cost (AC) = AC(A) + AC(B)
                       = ₹2,00,000 + ₹1,00,000
                       = ₹3,00,000

Total Earned Value (EV) = EV(A) + EV(B)
                        = ₹1,80,000 + ₹60,000
                        = ₹2,40,000
```

**Summary Table:**

| Activity  | PV            | AC            | % Done | EV            |
| --------- | ------------- | ------------- | ------ | ------------- |
| A         | ₹1,80,000     | ₹2,00,000     | 100%   | ₹1,80,000     |
| B         | ₹80,000       | ₹1,00,000     | 75%    | ₹60,000       |
| **Total** | **₹2,60,000** | **₹3,00,000** | **-**  | **₹2,40,000** |

**Step 3: Calculate Schedule Performance Index (SPI)**

```
SPI = EV / PV
    = ₹2,40,000 / ₹2,60,000
    = 0.923
```

**Interpretation:**

- SPI = 0.923 (or 92.3%)
- **Schedule Efficiency:** Getting 92 paisa of scheduled work done per rupee planned
- **Status:** Project is **7.7% behind schedule**
- **Meaning:** For every ₹1 worth of work planned, only ₹0.92 worth is actually completed

**Step 4: Calculate Cost Performance Index (CPI)**

```
CPI = EV / AC
    = ₹2,40,000 / ₹3,00,000
    = 0.80
```

**Interpretation:**

- CPI = 0.80 (or 80%)
- **Cost Efficiency:** Getting 80 paisa of value per rupee spent
- **Status:** Project is **20% over budget**
- **Meaning:** For every ₹1 spent, only getting ₹0.80 worth of work done

**Step 5: Comprehensive Analysis**

**Schedule Variance (SV):**

```
SV = EV - PV = ₹2,40,000 - ₹2,60,000 = -₹20,000
Interpretation: ₹20,000 worth of work behind schedule
```

**Cost Variance (CV):**

```
CV = EV - AC = ₹2,40,000 - ₹3,00,000 = -₹60,000
Interpretation: ₹60,000 over budget for work completed
```

**Final Results:**

| Metric  | Formula | Value     | Interpretation           |
| ------- | ------- | --------- | ------------------------ |
| **SPI** | EV / PV | **0.923** | **7.7% behind schedule** |
| **CPI** | EV / AC | **0.80**  | **20% over budget**      |
| SV      | EV - PV | -₹20,000  | ₹20K work behind         |
| CV      | EV - AC | -₹60,000  | ₹60K overspent           |

**Project Status Summary:**

**Overall Health:** ⚠ **CRITICAL**

- Behind schedule (SPI = 0.923)
- Significantly over budget (CPI = 0.80)
- Dual problem: slow progress AND cost overruns

**Activity-Level Insights:**

**Activity A:**

- **Schedule:** ✅ 100% complete (on track)
- **Cost:** ❌ Spent ₹2,00,000 for ₹1,80,000 worth of work
- **CPI(A):** 1,80,000 / 2,00,000 = 0.90 (10% over budget)

**Activity B:**

- **Schedule:** ❌ Only 75% complete (should be 100%)
- **Cost:** ❌ Spent ₹1,00,000 for ₹60,000 worth of work
- **CPI(B):** 60,000 / 1,00,000 = 0.60 (40% over budget - **SEVERE**)

**Root Cause:** Activity B is the major problem (25% incomplete, 40% cost overrun)

**Recommended Actions:**

**Immediate Actions:**

**1. For Schedule Recovery (SPI = 0.923):**

- **Focus on Activity B:** 25% still incomplete
- Add resources to complete B quickly
- Identify blockers preventing B's completion
- Consider overtime or additional staff
- Re-estimate time to complete B

**2. For Cost Control (CPI = 0.80):**

- **Investigate Activity B's cost overrun (CPI = 0.60):**
  - Why ₹1,00,000 spent for ₹60,000 worth of work?
  - Underestimation? Rework? Inefficiency? Scope creep?
- Stop unnecessary spending immediately
- Review all future costs with critical eye
- Consider scope reduction if budget is fixed

**3. Stakeholder Communication:**

- **Alert sponsor immediately:** Project is 20% over budget and behind schedule
- **Present forecast:** If CPI = 0.80 continues, final cost will be 25% higher than budget
- **Request decision:**
  - Approve additional budget?
  - Reduce scope?
  - Accept delay?

**4. Forecasting:**
If BAC (Budget at Completion) was ₹X:

```
EAC = BAC / CPI = BAC / 0.80 = 1.25 × BAC
Projected overrun: 25%
```

**Strategic Considerations:**

**Why is Activity B performing so poorly?**
Possible reasons:

- Requirements unclear → Rework
- Team lacks skills → Learning curve
- Technical complexity underestimated
- Dependencies on external parties causing delays
- Poor task breakdown in estimates

**Lessons for Future:**

- More detailed estimation for similar activities
- Allocate contingency budget for uncertain tasks
- More frequent monitoring (weekly vs monthly)
- Earlier intervention when CPI drops below 0.95

**Conclusion:**

The project is in **critical condition** with:

- **SPI = 0.923** → 7.7% behind schedule
- **CPI = 0.80** → 20% over budget

Activity B is the primary concern (75% done, CPI = 0.60). **Urgent corrective action required:**

- Complete Activity B immediately
- Investigate and eliminate cost inefficiencies
- Update stakeholders on projected overrun
- Implement strict cost controls for remaining work

**Answer Box:**

```
┌────────────────────────────────────────┐
│ SPI = 0.923 (7.7% behind schedule)    │
│ CPI = 0.80 (20% over budget)          │
│                                        │
│ Status: Project is behind schedule     │
│         and significantly over budget  │
└────────────────────────────────────────┘
```

---

## 📝 SECTION A QUICK-ANSWER BANK (Unit IV)

| **Question**                                  | **Answer (2 marks)**                                                                                                                                                                                                                                                                                                                                                                          |
| --------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| What is Earned Value Analysis?                | EVA is project performance measurement integrating scope, schedule, cost. Three values: PV (planned work), EV (actual work done), AC (actual cost). Key indices: SPI = EV/PV (schedule efficiency), CPI = EV/AC (cost efficiency). Enables forecasting (EAC, VAC) and early problem detection. Objective, quantitative project health assessment.                                             |
| Define SPI and CPI                            | **SPI (Schedule Performance Index)** = EV / PV. Measures schedule efficiency. SPI > 1 = ahead, < 1 = behind. **CPI (Cost Performance Index)** = EV / AC. Measures cost efficiency. CPI > 1 = under budget, < 1 = over budget. Both are ratios showing performance relative to baseline.                                                                                                       |
| What is Software Configuration Management?    | SCM is tracking and controlling changes in software artifacts (code, docs, designs) to maintain integrity and traceability. Four activities: (1) Configuration Identification - define CIs, (2) Configuration Control - manage changes via CCB, (3) Status Accounting - track versions, (4) Configuration Audit - verify conformance. Tools: Git, SVN.                                        |
| Explain Change Control                        | Change Control is formal process to evaluate, approve, and implement changes to project baselines. Process: Submit request → Impact analysis → CCB evaluation → Decision (approve/reject/defer) → Implementation → Verification → Close. Prevents scope creep, maintains baselines, documents decisions. Essential for project stability.                                                     |
| What is Framework for Management and Control? | Systematic structure of processes, tools, techniques to monitor performance and take corrective actions. Components: (1) Planning - set baselines, KPIs, (2) Monitoring - collect actual data, (3) Controlling - analyze variances, implement corrections, (4) Reporting - communicate status. Three levels: strategic, tactical, operational. Deming PDCA cycle.                             |
| Define EAC and VAC                            | **EAC (Estimate at Completion)** = Forecasted total project cost. Formula: BAC / CPI or AC + [(BAC-EV)/(CPI×SPI)]. Predicts final cost based on current performance. **VAC (Variance at Completion)** = BAC - EAC. Expected budget surplus (positive) or overrun (negative) at project end.                                                                                                   |
| What is Change Control Board (CCB)?           | CCB is formal group that reviews and approves/rejects change requests. Members: PM (chair), technical lead, business owner, QA, stakeholders. Meets weekly/bi-weekly. Evaluates change impact on scope, schedule, cost, quality. Makes decisions: approve, reject, defer. Ensures controlled, documented change process.                                                                      |
| Explain Burndown Chart                        | Burndown Chart visualizes work remaining over time. X-axis: time (days/sprints), Y-axis: work remaining (story points/tasks). Ideal line: diagonal from total work to zero. Actual line shows real progress. Interpretation: Actual below ideal = ahead, above = behind, flat = no progress (blockers). Used in Agile/Scrum.                                                                  |
| What is Configuration Item (CI)?              | CI is any artifact placed under configuration management control. Examples: source code files, executables, documentation, test cases, database schemas, config files. Each CI has unique identifier, version number, baseline status. Tracked in version control system. Changes require formal approval.                                                                                    |
| List Cost Monitoring Techniques               | (1) **Earned Value Analysis** - integrates scope/schedule/cost, (2) **Budget vs Actual Reports** - compare planned and actual spend, (3) **Cost Variance Analysis** - CV = EV - AC, (4) **Trend Analysis** - track spending over time, (5) **Forecasting** - EAC predictions, (6) **S-Curves** - cumulative cost visualization, (7) **Milestone Cost Reviews** - check budget at checkpoints. |

---

## 💡 EXAM ANSWER TIPS - UNIT IV

### For Section A (2 marks):

**EVA concepts:**

- Define metric + formula
- One-line interpretation
- Example: "SPI = EV/PV. Measures schedule efficiency. SPI < 1 = behind."

**SCM/Change Control:**

- Define + list 4 components/steps
- Very concise

### For Section B (7-10 marks):

**Theory questions:**

- Framework: Define + 4 components with brief explanation
- SCM: 4 activities with examples
- Change Control: Process steps with example

### For Section C (7-10 marks) - GUARANTEED EVA NUMERICAL:

**Time allocation: 20-25 minutes**

**Must-do steps:**

1. **Create given data table** (PV, AC, % complete)
2. **Calculate EV** for each activity (% × PV)
3. **Calculate totals** (Total PV, AC, EV)
4. **Calculate SPI** = Total EV / Total PV
5. **Calculate CPI** = Total EV / Total AC
6. **If asked, calculate** EAC, VAC
7. **Write interpretation** for each metric
8. **Box final answers**

**Presentation tips:**

- **Use tables** for calculations
- **Show formulas** before calculating
- **Label everything** clearly (Total PV, Total EV, Total AC)
- **State interpretation** for SPI/CPI (ahead/behind, under/over)
- **Round to 2-3 decimal places** (SPI = 0.923, not 0.9230769)

**Common mistakes to avoid:**

- ❌ Using PV instead of calculating EV (EV = % complete × PV)
- ❌ Forgetting to sum totals before calculating SPI/CPI
- ❌ Calculating per-activity SPI/CPI instead of project-level
- ❌ Wrong EAC formula (EAC = BAC / CPI, not BAC × CPI)
- ❌ Not stating interpretation

**Pro tip:** Even if you forget formulas, write:

- EV = work completed
- SPI = schedule metric (EV vs PV)
- CPI = cost metric (EV vs AC)
- Partial credit guaranteed!

### Formulas to Memorize:

**Core EVA:**

```
EV = % Complete × PV
SPI = EV / PV
CPI = EV / AC
SV = EV - PV
CV = EV - AC
```

**Forecasting:**

```
EAC = BAC / CPI (most common)
EAC = AC + [(BAC - EV) / (CPI × SPI)] (both influence)
VAC = BAC - EAC
ETC = EAC - AC
```

---

## 📊 UNIT IV SUMMARY

**Tier A Topics (Must Master):**

1. ✅ **Earned Value Analysis (EVA)** - GUARANTEED numerical every year
2. ✅ Framework for Management and Control - Theory + concepts
3. ✅ All EVA formulas - SPI, CPI, EAC, VAC

**Tier B Topics (Should Cover):**

1. ✅ Software Configuration Management (SCM) - 4 activities
2. ✅ Change Control - Process steps
3. ✅ Contract Management - Types, clauses
4. ✅ Cost Monitoring techniques
5. ✅ Visualizing Progress - Burndown, dashboard

**Tier C Topics (Low Priority):**

1. Data Collection methods - Brief read
2. Detailed contract clauses - Skim only

**Time Investment:**

- **EVA practice:** 4 hours (solve 7-10 numerical problems)
- **EVA theory:** 2 hours (understand concepts, interpretations)
- **Framework/SCM/Change Control:** 2 hours (theory)
- **Other topics:** 1 hour
- **Total: 9 hours for Unit IV**

**Critical Practice:**

- ✅ Solve ALL EVA numerical from 4 PYQ years
- ✅ Practice with different scenarios (1 activity, 2 activities, given BAC)
- ✅ Memorize all EVA formulas (write on formula sheet before exam)
- ✅ Practice interpretation statements for SPI/CPI
- ✅ Master EAC calculation (both methods)

**Formula Sheet (Write in exam):**

```
EV = % Complete × PV
SPI = EV / PV → > 1 ahead, < 1 behind
CPI = EV / AC → > 1 under budget, < 1 over
EAC = BAC / CPI
VAC = BAC - EAC → > 0 under, < 0 over
```

---

**✅ Unit 4 Notes Complete!**

**EVA numerical is GUARANTEED in Section C every year - master it for easy 7-10 marks!**

Type **'next'** to proceed to **Unit 5 notes** (Staffing in Software Projects - final unit!)
