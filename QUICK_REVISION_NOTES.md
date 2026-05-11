# 📚 QUICK REVISION NOTES - SOFTWARE PROJECT MANAGEMENT (BOE068)

**Last-Minute Exam Preparation Guide**  
**Time Required: 4-6 hours for complete revision**

---

## 🎯 EXAM PATTERN (2024-25 - LATEST)

| Section | Questions | Marks/Q | Selection | Total |
|---------|-----------|---------|-----------|-------|
| **A** | 7 | 2 | ALL | 14 |
| **B** | 5 | 7 | Any 3 | 21 |
| **C** | 5 (Q3-Q7) | 7 | Any 1 part from each | 35 |
| **Total** | | | | **70** |

**Passing:** 28/70 (40%) | **Target:** 42+/70 (60%)

---

## ⚡ GUARANTEED QUESTIONS (Based on 4 Years PYQ)

### Section C - 100% Appearance Rate:
1. ✅ **CPM/PERT Network** (Unit 3) - Appears EVERY year
2. ✅ **EVA Numerical** (Unit 4) - Appears EVERY year

### High Frequency (75%+):
3. ✅ **RAD or Agile** (Unit 2) - 4/4 years
4. ✅ **Function Points** (Unit 2) - 3/4 years
5. ✅ **Oldham-Hackman** (Unit 5) - 3/4 years
6. ✅ **NPV/ROI Calculation** (Unit 1) - 3/4 years

---

## 📊 UNIT-WISE QUICK SUMMARY

### **UNIT 1: Project Evaluation & Planning** (10% weightage)

**🔴 Tier A Topics:**
- Software Project Management (definition, activities, importance)
- Categorization of Projects (strategic/tactical/operational, outsourced/in-house)
- Cost-Benefit Evaluation (NPV, ROI, Payback Period)

**Key Formulas:**
```
Net Profit (NP) = Total Revenue - Total Cost

ROI = (Net Profit / Total Cost) × 100%

Payback Period = Years to recover initial investment

NPV = Σ[Cash Flow(t) / (1+r)^t] - Initial Investment
     where r = discount rate (typically 10%)
```

**PV Factors @ 10%:**
| Year | Factor | Year | Factor |
|------|--------|------|--------|
| 1 | 0.9091 | 4 | 0.6830 |
| 2 | 0.8264 | 5 | 0.6209 |
| 3 | 0.7513 | | |

**Stepwise Project Planning (10 Steps):**
```
0. Select Project
1. Identify Scope & Objectives
2. Identify Infrastructure
3. Analyze Characteristics
4. Identify Products & Activities
5. Estimate Effort
6. Identify Risks
7. Allocate Resources
8. Review & Publicize Plan
9. Execute & Monitor
10. Lower-Level Planning (iterative)
```

---

### **UNIT 2: Project Life Cycle & Effort Estimation** (20% weightage)

**🔴 Tier A Topics:**
- Project Life Cycle (5 phases)
- RAD Model (4 phases)
- Agile Methodologies (Scrum framework)
- Function Points (calculation with numerical)

**Project Life Cycle:**
```
1. Initiation → Define, Get Approval
2. Planning → Detailed Roadmap, Baselines
3. Execution → Build Deliverables
4. Monitoring & Controlling → Track, Correct (parallel to execution)
5. Closure → Handover, Lessons Learned
```

**RAD Model (4 Phases):**
```
┌─────────────────────────────────────────────┐
│ 1. Requirements Planning (10-15%)          │
│    - High-level requirements               │
│    - Define scope & success criteria       │
├─────────────────────────────────────────────┤
│ 2. User Design (40-50%)                    │
│    - Build prototypes iteratively          │
│    - JAD workshops with users              │
│    - Continuous feedback & refinement      │
├─────────────────────────────────────────────┤
│ 3. Construction (30-40%)                   │
│    - Convert prototype to production code  │
│    - Use code generators, reusable comps   │
│    - Continuous testing                    │
├─────────────────────────────────────────────┤
│ 4. Cutover (5-10%)                         │
│    - UAT, training, deployment             │
│    - Data migration                        │
└─────────────────────────────────────────────┘
Timeline: 60-90 days total
```

**Agile Manifesto (4 Values):**
```
1. Individuals & Interactions > Processes & Tools
2. Working Software > Comprehensive Documentation
3. Customer Collaboration > Contract Negotiation
4. Responding to Change > Following a Plan
```

**Scrum Framework:**
```
Roles:
- Product Owner (customer rep, owns backlog)
- Scrum Master (facilitator, removes blockers)
- Development Team (5-9 cross-functional members)

Artifacts:
- Product Backlog (prioritized feature list)
- Sprint Backlog (tasks for current sprint)
- Increment (potentially shippable product)

Events:
- Sprint (1-4 weeks, typically 2)
- Sprint Planning (select work)
- Daily Standup (15 min sync)
- Sprint Review (demo)
- Retrospective (improve)
```

**Function Point Calculation:**

**Step 1: Count Components**
| Component | Count | Weight (Avg) |
|-----------|-------|--------------|
| External Inputs (EI) | X | 4 |
| External Outputs (EO) | Y | 5 |
| External Inquiries (EQ) | Z | 4 |
| Internal Logical Files (ILF) | A | 10 |
| External Interface Files (EIF) | B | 7 |

**Step 2: Calculate UFP**
```
UFP = (EI × 4) + (EO × 5) + (EQ × 4) + (ILF × 10) + (EIF × 7)
```

**Step 3: Calculate VAF**
```
TDI = Σ(14 GSC ratings) [typically 42 if all moderate]
VAF = 0.65 + (0.01 × TDI)
     = 0.65 + 0.42 = 1.07 (if TDI=42)
```

**Step 4: Calculate AFP**
```
AFP = UFP × VAF
```

---

### **UNIT 3: Activity Planning & Risk Management** (30% weightage)

**🔴 Tier A Topics - MOST IMPORTANT UNIT:**
- Critical Path Method (CPM) - **GUARANTEED EVERY YEAR**
- Forward Pass & Backward Pass
- PERT Technique
- Risk Management

**CPM Process (Step-by-Step):**

```
┌────────────────────────────────────────────┐
│ STEP 1: List Activities                   │
│ Activity | Duration | Predecessors        │
├────────────────────────────────────────────┤
│ STEP 2: Draw Network Diagram (AON)        │
│ Boxes = Activities, Arrows = Dependencies │
├────────────────────────────────────────────┤
│ STEP 3: FORWARD PASS                      │
│ • Start: EST = 0                          │
│ • EFT = EST + Duration                    │
│ • Multiple predecessors:                  │
│   EST = MAX(EFT of all predecessors)      │
│ • Project Duration = MAX(all EFTs)        │
├────────────────────────────────────────────┤
│ STEP 4: BACKWARD PASS                     │
│ • End: LFT = Project Duration             │
│ • LST = LFT - Duration                    │
│ • Multiple successors:                    │
│   LFT = MIN(LST of all successors)        │
├────────────────────────────────────────────┤
│ STEP 5: Calculate Total Float             │
│ TF = LST - EST (or LFT - EFT)             │
├────────────────────────────────────────────┤
│ STEP 6: Identify Critical Path            │
│ All activities with TF = 0                │
└────────────────────────────────────────────┘
```

**Activity Node Format:**
```
┌─────────────────────┐
│   Activity Name     │
├──────────┬──────────┤
│   EST    │   EFT    │
├──────────┼──────────┤
│ Duration │          │
├──────────┼──────────┤
│   LST    │   LFT    │
├──────────┴──────────┤
│  Total Float (TF)   │
└─────────────────────┘
```

**PERT Formulas:**
```
Expected Time (TE) = (O + 4M + P) / 6
  where: O = Optimistic
         M = Most Likely
         P = Pessimistic

Variance (V) = [(P - O) / 6]²

Standard Deviation (SD) = √Variance = (P - O) / 6

Project Variance = Σ(Variances of CRITICAL PATH activities only)

Project SD = √(Project Variance)

Z-score = (Target Date - Expected Duration) / Project SD
  Then use normal table for probability
```

**Risk Management Process:**
```
┌─────────────────────────────────────────────┐
│ 1. RISK IDENTIFICATION                      │
│    • Brainstorming, checklists, SWOT       │
│    • Expert interviews, document review     │
├─────────────────────────────────────────────┤
│ 2. RISK ASSESSMENT                          │
│    • Probability: VLow, Low, Med, High, VH │
│    • Impact: VLow, Low, Med, High, Critical│
│    • Risk Score = Probability × Impact     │
├─────────────────────────────────────────────┤
│ 3. RISK PLANNING (4 Strategies)            │
│    • AVOID - Eliminate risk                │
│    • MITIGATE - Reduce probability/impact  │
│    • TRANSFER - Shift to 3rd party         │
│    • ACCEPT - Do nothing, acknowledge      │
├─────────────────────────────────────────────┤
│ 4. RISK MONITORING & CONTROL               │
│    • Track status, execute responses       │
│    • Monitor triggers, update register     │
└─────────────────────────────────────────────┘
```

---

### **UNIT 4: Project Management & Control** (30% weightage)

**🔴 Tier A Topic:**
- **Earned Value Analysis (EVA) - GUARANTEED NUMERICAL EVERY YEAR**

**EVA Core Values:**
```
PV (Planned Value) = Planned % complete × BAC
     "What SHOULD be done"

EV (Earned Value) = Actual % complete × BAC
     "What WAS actually done"

AC (Actual Cost) = Money actually spent
     "What was actually SPENT"
```

**EVA Formulas (MEMORIZE!):**

**Performance Metrics:**
```
Schedule Variance (SV) = EV - PV
  • SV > 0: Ahead of schedule
  • SV < 0: Behind schedule

Cost Variance (CV) = EV - AC
  • CV > 0: Under budget
  • CV < 0: Over budget

Schedule Performance Index (SPI) = EV / PV
  • SPI > 1.0: Ahead (e.g., 1.10 = 10% ahead)
  • SPI < 1.0: Behind (e.g., 0.90 = 10% behind)

Cost Performance Index (CPI) = EV / AC
  • CPI > 1.0: Under budget (e.g., 1.10 = $1.10 value per $1 spent)
  • CPI < 1.0: Over budget (e.g., 0.90 = $0.90 value per $1 spent)
```

**Forecasting Formulas:**
```
Estimate At Completion (EAC):
  Method 1: EAC = BAC / CPI
    (Use when only CPI influences future)
  
  Method 2: EAC = AC + [(BAC - EV) / (CPI × SPI)]
    (Use when both CPI & SPI influence)

Estimate To Complete (ETC) = EAC - AC

Variance At Completion (VAC) = BAC - EAC
  • VAC > 0: Will finish under budget
  • VAC < 0: Will finish over budget
```

**EVA Calculation Steps:**
```
Given: BAC, EV, PV, AC

Step 1: Calculate SPI = EV / PV
Step 2: Calculate CPI = EV / AC
Step 3: Calculate EAC = BAC / CPI (or use Method 2)
Step 4: Calculate VAC = BAC - EAC
Step 5: Interpret results
```

**Framework for Management & Control:**
```
┌──────────────────────────────────────┐
│ 1. PLANNING                          │
│    • Set baselines (scope, schedule, │
│      cost, quality)                  │
│    • Define metrics, KPIs            │
├──────────────────────────────────────┤
│ 2. MONITORING                        │
│    • Collect actual performance data │
│    • Measure against baselines       │
│    • Track variances                 │
├──────────────────────────────────────┤
│ 3. CONTROLLING                       │
│    • Analyze root causes             │
│    • Take corrective actions         │
│    • Update forecasts                │
├──────────────────────────────────────┤
│ 4. REPORTING                         │
│    • Status reports, dashboards      │
│    • Exception reporting             │
│    • Stakeholder communication       │
└──────────────────────────────────────┘
Operates at 3 levels: Strategic, Tactical, Operational
```

**Software Configuration Management (SCM):**
```
4 Key Activities:
1. Configuration Identification
   - Define Configuration Items (CIs)
   - Establish baselines

2. Configuration Control (Change Control)
   - Submit change request
   - Impact analysis
   - CCB approval
   - Implementation

3. Configuration Status Accounting
   - Track versions, changes
   - Who changed what when why

4. Configuration Audit
   - Verify conformance
   - Functional & physical audits
```

---

### **UNIT 5: Staffing in Software Projects** (10% weightage)

**🔴 Tier A Topics:**
- Organizational Behavior
- **Oldham-Hackman Job Characteristic Model**

**Oldham-Hackman Model Structure:**
```
┌────────────────────────────────────────────┐
│     5 CORE JOB DIMENSIONS                  │
├────────────────────────────────────────────┤
│ 1. SKILL VARIETY                           │
│    • Degree job requires different skills  │
│    • Low: Repetitive → High: Diverse       │
├────────────────────────────────────────────┤
│ 2. TASK IDENTITY                           │
│    • Complete whole piece of work          │
│    • Low: Fragment → High: End-to-end      │
├────────────────────────────────────────────┤
│ 3. TASK SIGNIFICANCE                       │
│    • Impact on others' lives               │
│    • Low: Trivial → High: Meaningful       │
├────────────────────────────────────────────┤
│ 4. AUTONOMY                                │
│    • Freedom & discretion                  │
│    • Low: Micromanaged → High: Empowered   │
├────────────────────────────────────────────┤
│ 5. FEEDBACK                                │
│    • Clear performance information         │
│    • Low: Uncertain → High: Regular info   │
└────────────────────────────────────────────┘
              ↓
┌────────────────────────────────────────────┐
│  3 CRITICAL PSYCHOLOGICAL STATES           │
├────────────────────────────────────────────┤
│ 1. Experienced Meaningfulness              │
│    (Created by: SV + TI + TS)              │
│ 2. Experienced Responsibility              │
│    (Created by: Autonomy)                  │
│ 3. Knowledge of Results                    │
│    (Created by: Feedback)                  │
└────────────────────────────────────────────┘
              ↓
┌────────────────────────────────────────────┐
│  5 PERSONAL & WORK OUTCOMES                │
├────────────────────────────────────────────┤
│ 1. High Internal Work Motivation           │
│ 2. High Quality Work Performance           │
│ 3. High Satisfaction with Work             │
│ 4. Low Absenteeism and Turnover            │
│ 5. Personal Growth and Development         │
└────────────────────────────────────────────┘
```

**Motivating Potential Score (MPS):**
```
MPS = [(Skill Variety + Task Identity + Task Significance) / 3] 
      × Autonomy 
      × Feedback

• Each dimension rated 1-7 (low to high)
• Autonomy & Feedback are MULTIPLIERS
• If either Autonomy or Feedback = 0, MPS = 0!
• Higher MPS = More motivating job
```

**Best Methods of Staff Selection (Ranked by Validity):**
```
1. Work Sample Tests (Highest)
   - Actual job tasks (coding test, code review)
   
2. Structured Interviews
   - Standardized questions, scoring rubric
   - Behavioral (STAR) + Situational questions
   
3. Cognitive Ability Tests
   - Intelligence, problem-solving, learning ability
   
4. Personality Tests
   - Big Five: Conscientiousness (best predictor)
   
5. Reference Checks
   - "Would you rehire?" = Most telling question
   
6. Portfolio/GitHub Review
   - Real code, projects, contributions
```

**Motivation (Intrinsic vs Extrinsic):**
```
INTRINSIC (More powerful for knowledge workers):
• Mastery - Learning, improving skills
• Autonomy - Freedom to choose how
• Purpose - Meaningful work with impact
• Challenge - Complex, interesting problems

EXTRINSIC:
• Salary, bonuses
• Recognition, titles
• Career advancement
• Perks (flexible hours, remote)

Key: For developers, intrinsic > extrinsic
```

---

## 🎯 GUARANTEED NUMERICALS - PRACTICE THESE!

### **CPM Numerical (Unit 3) - GUARANTEED**

**Given:**
- Activity list with duration and predecessors

**Find:**
- Draw network
- Forward pass (EST, EFT)
- Backward pass (LST, LFT)
- Total Float
- Critical Path
- Project Duration

**Pro Tips:**
- Create activity table first
- Draw network neatly with labeled nodes
- For multiple predecessors: EST = **MAX** of predecessors' EFT
- For multiple successors: LFT = **MIN** of successors' LST
- TF = 0 → Critical activity
- Double-check critical path duration matches project duration

---

### **EVA Numerical (Unit 4) - GUARANTEED**

**Given:**
- Activities with PV, AC, % complete
- OR: BAC, EV, PV, AC directly

**Find:**
- SPI, CPI
- Often: EAC, VAC

**Solution Steps:**
```
Step 1: Calculate EV for each activity
        EV = % Complete × PV

Step 2: Calculate Totals
        Total PV = Sum of all PV
        Total AC = Sum of all AC
        Total EV = Sum of all EV

Step 3: Calculate SPI & CPI
        SPI = Total EV / Total PV
        CPI = Total EV / Total AC

Step 4: Interpret
        SPI < 1.0 = Behind schedule
        CPI < 1.0 = Over budget

Step 5: If asked, calculate EAC & VAC
        EAC = BAC / CPI
        VAC = BAC - EAC
```

**Pro Tips:**
- Don't forget to calculate EV (common mistake!)
- Use TOTALS for SPI/CPI, not individual activities
- Show interpretation in words, not just numbers
- Box final answers

---

### **Function Points (Unit 2) - High Frequency**

**Given:**
- Counts: EI, EO, EQ, ILF, EIF
- Weights (usually average)
- GSC ratings (usually moderate = 42)

**Find:**
- UFP, VAF, AFP

**Solution Steps:**
```
Step 1: UFP = Σ(Count × Weight)
        = (EI×weight) + (EO×weight) + ... + (EIF×weight)

Step 2: VAF = 0.65 + (0.01 × TDI)
        If TDI = 42 (moderate), VAF = 1.07

Step 3: AFP = UFP × VAF
```

---

### **NPV Calculation (Unit 1) - High Frequency**

**Given:**
- Initial investment (Year 0, negative)
- Cash flows for Years 1-5
- Discount rate (typically 10%)

**Find:**
- NPV, ROI, Payback Period

**Solution Steps:**
```
Step 1: Calculate PV for each year
        PV = Cash Flow / (1 + r)^t
        Use PV factors from table

Step 2: Sum all PVs
        NPV = Σ(PV of all years) - Initial Investment

Step 3: If NPV > 0, project is financially viable

For ROI:
        Total Revenue = Sum of all positive cash flows
        ROI = (Total Revenue - Total Cost) / Total Cost × 100

For Payback:
        Calculate cumulative cash flow each year
        Find year when cumulative turns positive
```

---

## 📋 SECTION-WISE STRATEGY

### **Section A (14 marks) - 7×2 = Must Score 12+**

**Time:** 15-20 minutes total

**Strategy:**
- Each answer: 4-5 lines (half page)
- Structure: Definition (1 line) + 2-3 key points + Example (if space)
- Don't overthink, write what you know
- No diagrams needed

**High-Frequency Topics:**
- Define SPM, Agile, CPM, PERT, EVA, Risk Management
- Function Points, Organizational Behavior
- Oldham-Hackman dimensions (Skill Variety, Autonomy, etc.)
- Project Life Cycle stages

---

### **Section B (21 marks) - 3×7 = Choose Wisely**

**Time:** 60-70 minutes (20-25 min per question)

**Strategy:**
- Pick questions you can write 1.5-2 pages for
- Structure: Intro → Main body (4-5 points) → Conclusion
- Use headings/subheadings
- Simple diagram adds value (optional)

**Common Topics:**
- RAD Model (4 phases with explanation)
- Agile vs Waterfall comparison
- Staff selection methods
- Risk Management process
- PERT or CPM theory
- Oldham-Hackman model

---

### **Section C (35 marks) - 5×7 = Do 4 well, 1 decent**

**Time:** 100-110 minutes (20-25 min per question)

**Strategy:**
- Q3: Usually Unit 1 or 2 (NPV/ROI or Agile)
- Q4: Usually Unit 2 (RAD, COCOMO)
- Q5: **ALWAYS CPM/PERT** (Unit 3) - **DO THIS!**
- Q6: **ALWAYS EVA** (Unit 4) - **DO THIS!**
- Q7: Usually Unit 5 or Unit 1 (Oldham-Hackman or Stepwise Planning)

**Must-Do Questions:**
1. ✅ CPM/PERT numerical (Q5)
2. ✅ EVA numerical (Q6)
3. Pick 3 more from Q3, Q4, Q7 based on preparation

**Numerical Questions:**
- Show ALL formulas first
- Create tables for organization
- Show step-by-step calculations
- Box final answers with units
- Write interpretation

**Theory Questions:**
- Introduction (define concept)
- Main body with headings
- Real-world examples
- Diagram if time permits
- Conclusion (benefits/applications)

---

## ⚠️ COMMON MISTAKES TO AVOID

### CPM:
- ❌ Using SUM instead of MAX for multiple predecessors
- ❌ Using MAX instead of MIN for multiple successors
- ❌ Not stating project duration
- ❌ Wrong critical path identification

### EVA:
- ❌ Forgetting to calculate EV (EV = % × PV)
- ❌ Using individual activity values instead of totals
- ❌ Wrong EAC formula (EAC = BAC / CPI, not BAC × CPI)
- ❌ No interpretation of SPI/CPI values

### Function Points:
- ❌ Forgetting VAF calculation
- ❌ Using UFP as final answer (should be AFP)

### General:
- ❌ No units in numerical answers (rupees, weeks, %)
- ❌ Not showing formulas before calculating
- ❌ Messy presentation (use tables!)
- ❌ Running out of time (practice time management)

---

## 🎯 FINAL 24-HOUR REVISION PLAN

### **6 Hours Before Exam:**

**Hour 1-2: Formulas (Write 3x)**
- All CPM formulas (EST, EFT, LST, LFT, TF)
- All EVA formulas (SPI, CPI, EAC, VAC)
- Function Points (UFP, VAF, AFP)
- NPV, ROI, Payback
- PERT (TE, Variance)
- Oldham-Hackman MPS

**Hour 3: Solve 2 Numericals**
- 1 CPM problem (full solution)
- 1 EVA problem (full solution)

**Hour 4: Memorize Definitions**
- SPM, Agile, RAD, Scrum
- CPM, PERT, EVA, Risk Management
- Oldham-Hackman (5 dimensions)
- Function Points
- Organizational Behavior

**Hour 5: Review Unit Summaries**
- Skim Unit 1-5 summaries from this doc
- Focus on Tier A topics only

**Hour 6: Mock Paper Planning**
- Read 2023-24 or 2024-25 PYQ
- Decide which questions you'll attempt
- Practice time allocation

### **30 Minutes Before Exam:**
- ✅ Formula sheet review (don't memorize new content)
- ✅ Deep breaths, stay calm
- ✅ Read instructions carefully in exam
- ✅ Attempt CPM and EVA numericals first (guaranteed marks)

---

## ✅ FINAL CHECKLIST

**Formulas Memorized:**
- [ ] CPM: EST, EFT, LST, LFT, TF
- [ ] EVA: SPI, CPI, EAC, VAC
- [ ] PERT: TE = (O+4M+P)/6, Variance = [(P-O)/6]²
- [ ] Function Points: UFP, VAF, AFP
- [ ] NPV, ROI, Payback
- [ ] Oldham-Hackman: MPS formula

**Must-Know Definitions:**
- [ ] Software Project Management
- [ ] Agile (4 values)
- [ ] RAD Model (4 phases)
- [ ] CPM & PERT
- [ ] Earned Value Analysis
- [ ] Oldham-Hackman (5 dimensions)

**Numerical Practice:**
- [ ] Solved 3-5 CPM problems
- [ ] Solved 3-5 EVA problems
- [ ] Solved 2-3 Function Point problems
- [ ] Solved 2 NPV problems

**Strategy Clear:**
- [ ] Know which Section C questions to attempt
- [ ] Time allocation planned (20-25 min per Section C)
- [ ] Formula sheet ready (write on scratch paper before exam starts)

---

## 🔥 POWER TIPS FOR 60%+ SCORE

1. **CPM + EVA = 14 marks minimum** (20% of total) - These are FREE marks if you practice!

2. **Section A = Easy 12/14** - Just write definitions + 2 points. Don't overthink.

3. **Section B = Choose familiar topics** - RAD/Agile, Risk Management, SCM are easy to write.

4. **Time Management:**
   - Section A: 20 min
   - Section B: 70 min
   - Section C: 110 min
   - Buffer: 10 min

5. **Presentation Matters:**
   - Use tables in numericals
   - Underline headings
   - Box final answers
   - Write neatly

6. **If you forget formulas:**
   - Write what you remember
   - Show logic/approach
   - Partial credit guaranteed

7. **Don't leave questions blank:**
   - Write something relevant
   - Better than zero marks

---

**GOOD LUCK! You've got this! 🎯**

**Remember:** This syllabus heavily favors practice over memorization. CPM and EVA numericals are FREE marks if you practice them. Focus 60% of your revision time on Unit 3 and Unit 4!

---

**END OF QUICK REVISION NOTES**
