# UNIT 2: Project Life Cycle aur Effort Estimation

**Is unit me kya-kya aayega:**

- Software process aur models
- Project life cycle ke phases
- RAD (Rapid Application Development)
- Agile methodologies
- DSDM aur XP
- Effort estimation
- COCOMO model
- Function points
- Parametric models

---

## 📌 Project Life Cycle

> 🔴 **Tier A** | Frequency: 3/4 | Section: A

### Definition

**Project life cycle** matlab project ke start se end tak ke phases. Har phase me specific activities aur deliverables hote hain.

### Phases

**1. Initiation Phase:**

- Business need identify karo
- Feasibility check karo
- Stakeholders identify karo
- Project charter banao
- Management approval lo

**Duration:** 2-4 weeks
**Output:** Project charter, feasibility report

**2. Planning Phase:**

- Detailed scope define karo
- Timeline banao (Gantt chart, network diagram)
- Budget estimate karo
- Quality aur communication plan banao
- Risk analysis karo
- Baselines set karo

**Duration:** 3-8 weeks
**Output:** Project plan, schedule, budget

**3. Execution Phase:**

- Actual development work
- Code likhana, unit testing
- Team manage karna
- Quality assurance
- Vendor management

**Duration:** 60-80% of total project time
**Output:** Working software, tests, documentation

**4. Monitoring & Control Phase** (runs parallel to execution):

- Progress track karo
- Budget vs actual check karo
- Changes implement karo
- Status reports
- Corrective actions

**Duration:** Throughout project
**Output:** Status reports, metrics

**5. Closure Phase:**

- Final product deliver karo
- Client acceptance
- Resources release karo
- Lessons learned document karo
- Project close karo

**Duration:** 1-2 weeks
**Output:** Acceptance sign-off, final report

### Phase Summary Table

| **Phase**      | **Key Work**      | **Team Size** | **Risk** | **Cost** |
| -------------- | ----------------- | ------------- | -------- | -------- |
| **Initiation** | Plan, feasibility | Small         | High     | Low      |
| **Planning**   | Detailed plan     | Medium        | High     | Medium   |
| **Execution**  | Build product     | Large         | Medium   | High     |
| **Monitor**    | Track progress    | Mgmt          | Medium   | Low      |
| **Closure**    | Finalize          | Small         | Low      | Low      |

---

## 📌 Software Process aur Process Models

> 🟢 **Tier C** | Frequency: 1/4 | Section: B

### Quick Overview

**Software process:** Activities jo software banati hain (specification, design, development, testing).

**Process models:** Ye activities kaise organize hote hain, ye dikhate hain.

**Common models:**

- Waterfall: Sequential
- Iterative: Repeated cycles
- Incremental: Deliver in parts
- Spiral: Risk-driven
- Agile: Adaptive

---

## 📌 RAD (Rapid Application Development)

> 🔴 **Tier A** | Frequency: 4/4 | Section: B + C

### Definition

**RAD** ek methodology hai jo fast development ko priority deta hai. 60-90 days me complete system deliver karna goal hota hai.

### Key Characteristics

**1. Speed First:**

- Quick delivery ko priority
- "Good enough" perfectness se zyada important
- Iterative improvement

**2. User Involvement:**

- Users actively participate
- Daily/weekly feedback
- Continuous validation

**3. Prototyping:**

- Quickly build prototypes
- Users se immediate feedback
- Refine aur evolve

**4. Reusability:**

- Existing components use karo
- Code generators
- Minimize custom development

**5. Small Teams:**

- 2-6 people best
- Co-located
- Empowered decisions

### RAD Phases

**Phase 1: Requirements Planning (10-15%)**

- High-level requirements
- Scope define
- Critical features identify
- Duration: 1-2 weeks

**Phase 2: User Design (40-50%)**

- Build prototypes iteratively
- JAD workshops (Joint App Development)
- Users test aur give feedback
- Refine design
- Duration: 4-6 weeks

**Phase 3: Construction (30-40%)**

- Prototype to production code
- Automated code generators use
- Testing (unit, integration)
- Optimization
- Duration: 3-5 weeks

**Phase 4: Cutover (5-10%)**

- UAT (User Acceptance Testing)
- Data migration
- User training
- Deployment
- Duration: 1 week

### RAD Advantages

✅ Fast (2-3 months vs 6-12 months)
✅ High user satisfaction
✅ Flexibility for changes
✅ Early risk detection
✅ Cost savings
✅ Better quality through iteration

### RAD Disadvantages

❌ Skilled developers chahiye
❌ Large, complex systems ke liye nahi
❌ Users ka committed time chahiye
❌ Documentation kam ho sakta hai
❌ Scaling difficult

### When to Use RAD

✅ UI-heavy applications
✅ Time-to-market critical
✅ Users available for collaboration
✅ Modular requirements

❌ NOT for large enterprise systems
❌ NOT for safety-critical systems
❌ NOT when requirements very unclear

---

## 📌 DSDM (Dynamic System Development Method)

> 🟢 **Tier C** | Frequency: 1/4 | Section: C

**Key idea:** Agile + timeboxing

**Features:**

- Time-boxed deliverables
- Active user involvement
- Prioritization (MoSCoW)
- **M**ust have, **S**hould have, **C**ould have, **W**on't have this time

---

## 📌 Extreme Programming (XP)

> 🟡 **Tier B** | Frequency: varies | Section: varies

**Engineering-focused Agile:**

**Core practices:**

- Pair programming (2 developers ek workstation par)
- TDD (Test-Driven Development)
- Continuous integration
- Small releases
- Refactoring

**Benefits:**

- High code quality
- Fewer bugs
- Better team knowledge

---

## 📌 Effort Estimation Basics

> 🟢 **Tier C** | Frequency: 1/4 | Section: A + C

### Kyun Important Hai?

Project start karne se pehle:

- Kitna effort lagega (man-hours)?
- Kitna time lagega?
- Kitna budget chahiye?

### Estimation Methods

**1. Expert Judgment:**

- Experienced people ka estimate
- Based on past projects
- Subjectif but practical

**2. Analogous Estimation:**

- Similar past projects se compare
- "Ye project us jaisa hi tha"
- Quick, but historical data chahiye

**3. Parametric Estimation:**

- Mathematical models
- Historical data use
- Formula-based
- Examples: COCOMO, function points

**4. Bottom-up Estimation:**

- Har task ka estimate
- Sabka total = project estimate
- Detailed but time-consuming
  |------------|---------------|-----------|
  | **Approach** | Sequential, phase-based | Iterative, incremental |
  | **Requirements** | All defined upfront, frozen | Evolving, flexible |
  | **Planning** | Detailed upfront | Just-in-time, adaptive |
  | **Delivery** | Single release at end | Multiple releases (every 2 weeks) |
  | **Customer Involvement** | Requirements phase only | Continuous, every sprint |
  | **Testing** | At end of development | Continuous, throughout |
  | **Documentation** | Extensive | Minimal, just enough |
  | **Change** | Difficult, expensive | Welcome, easy to accommodate |
  | **Team Structure** | Hierarchical, specialized roles | Self-organizing, cross-functional |
  | **Risk** | High (late feedback) | Low (frequent validation) |
  | **Predictability** | High (fixed plan) | Lower (adaptive) |
  | **Best For** | Stable requirements, regulatory | Evolving requirements, innovation |

---

## 📌 Function Points (FP) and COSMIC

> 🔴 **Tier A** | Frequency: 3/4 | Section: B + C (Numerical)

### Definition

**Function Point Analysis (FPA)** is a standardized method to measure software size based on functionality delivered to users, independent of technology used.

### Why Function Points?

**Problems with Lines of Code (LOC):**

- Language-dependent (1000 lines Java ≠ 1000 lines Python)
- Can't estimate before coding
- Encourages verbose coding
- Doesn't measure user value

**Benefits of FP:**

- ✅ Technology-independent
- ✅ Can estimate early (from requirements)
- ✅ Measures user functionality
- ✅ Industry-standard metric
- ✅ Enables benchmarking across projects

### Function Point Counting (5 Components)

**1. External Inputs (EI)**

- **Definition:** Data entry screens, forms where user inputs data
- **Examples:** Login form, registration form, order entry screen
- **Count:** Each unique input transaction
- **Complexity Weights:**
  - Low: 3
  - Average: 4
  - High: 6

**2. External Outputs (EO)**

- **Definition:** Reports, screens displaying processed data
- **Examples:** Invoice, sales report, dashboard
- **Count:** Each unique output
- **Complexity Weights:**
  - Low: 4
  - Average: 5
  - High: 7

**3. External Inquiries (EQ)**

- **Definition:** Input-output combination, queries
- **Examples:** Search by customer ID, view order status
- **Count:** Each unique query
- **Complexity Weights:**
  - Low: 3
  - Average: 4
  - High: 6

**4. Internal Logical Files (ILF)**

- **Definition:** Data stored and maintained by application
- **Examples:** Customer database, product catalog, order history
- **Count:** Each logical group of data
- **Complexity Weights:**
  - Low: 7
  - Average: 10
  - High: 15

**5. External Interface Files (EIF)**

- **Definition:** Data referenced from other systems
- **Examples:** Tax rate from government API, payment gateway data
- **Count:** Each external data source
- **Complexity Weights:**
  - Low: 5
  - Average: 7
  - High: 10

### FP Calculation Steps

**Step 1: Count Function Types**

Count occurrences of each component type from requirements.

**Step 2: Determine Complexity**

Assess each function as Low/Average/High based on:

- Number of data elements
- Number of file types referenced

(In exams, usually "Average" complexity is assumed if not specified)

**Step 3: Calculate Unadjusted Function Points (UFP)**

```
UFP = Σ (Count × Weight)
    = (EI count × EI weight) + (EO count × EO weight) +
      (EQ count × EQ weight) + (ILF count × ILF weight) +
      (EIF count × EIF weight)
```

**Step 4: Calculate Value Adjustment Factor (VAF)**

Based on 14 General System Characteristics (GSC):

1. Data communications
2. Distributed processing
3. Performance objectives
4. Heavily used configuration
5. Transaction rate
6. Online data entry
7. End-user efficiency
8. Online update
9. Complex processing
10. Reusability
11. Installation ease
12. Operational ease
13. Multiple sites
14. Facilitate change

Each rated 0-5:

- 0 = Not present
- 1 = Incidental influence
- 2 = Moderate influence
- 3 = Average influence
- 4 = Significant influence
- 5 = Essential

```
TDI (Total Degree of Influence) = Σ (all 14 GSC ratings)
VAF = 0.65 + (0.01 × TDI)
```

Range: 0.65 to 1.35

(In exams, if GSCs are "moderate", TDI ≈ 42, VAF ≈ 1.07)

**Step 5: Calculate Adjusted Function Points (AFP)**

```
AFP = UFP × VAF
```

### Example Calculation

**Given:**

- External Inputs (EI): 30 (Average complexity)
- External Outputs (EO): 42 (Average complexity)
- External Inquiries (EQ): 8 (Average complexity)
- Internal Logical Files (ILF): 7 (Average complexity)
- External Interface Files (EIF): 6 (Average complexity)
- All GSCs rated as moderate

**Step 1: Count = Given above**

**Step 2: Weights (Average complexity from table):**

- EI: 4
- EO: 5
- EQ: 4
- ILF: 10
- EIF: 7

**Step 3: UFP Calculation:**

```
UFP = (30 × 4) + (42 × 5) + (8 × 4) + (7 × 10) + (6 × 7)
    = 120 + 210 + 32 + 70 + 42
    = 474
```

**Step 4: VAF Calculation:**

```
Assume all 14 GSCs rated as 3 (moderate)
TDI = 14 × 3 = 42
VAF = 0.65 + (0.01 × 42) = 0.65 + 0.42 = 1.07
```

**Step 5: AFP Calculation:**

```
AFP = UFP × VAF
    = 474 × 1.07
    = 507 Function Points
```

**Interpretation:**
This system has 507 function points of functionality.

### Converting FP to Effort

**Formula:**

```
Effort (person-hours) = Function Points × Hours per FP
```

**Typical Hours per FP by Language:**

- Assembly: 25-30 hours/FP
- C: 12-15 hours/FP
- Java: 8-12 hours/FP
- Python: 6-8 hours/FP
- Low-code platforms: 3-5 hours/FP

**Example:**

- 507 FP × 10 hours/FP = 5,070 person-hours
- If team of 5 people: 5,070 / 5 = 1,014 hours per person
- At 40 hours/week: 1,014 / 40 = 25.4 weeks ≈ 6 months

### COSMIC Full Function Points

**COSMIC (Common Software Measurement International Consortium)** is a second-generation FP method designed for:

- Real-time systems
- Embedded software
- Scientific applications
- More accurate sizing

**Key Differences from Traditional FP:**

- Focuses on **data movement** rather than data storage
- Four types of data movements:
  1. **Entry:** Data moves from user into system
  2. **Exit:** Data moves from system to user
  3. **Read:** Data moves from persistent storage to process
  4. **Write:** Data moves from process to persistent storage
- Each movement = 1 COSMIC Function Point (CFP)
- No complexity adjustment

**Advantages:**

- ✅ More accurate for complex systems
- ✅ Better for real-time and embedded software
- ✅ Simpler (no VAF calculation)
- ✅ ISO standard (ISO/IEC 19761)

**When to Use:**

- Traditional FP: Business applications, CRUD systems
- COSMIC: Real-time systems, scientific software, layered architectures

![Function Point Components](diagrams/function_point_components.svg)

---

## 📌 COCOMO Model

> 🟢 **Tier C** | Frequency: 1/4 | Section: C

### Overview (Brief)

**COCOMO (COnstructive COst MOdel)** estimates effort and schedule based on size (in thousands of lines of code - KLOC).

**Three Levels:**

**1. Basic COCOMO**

```
Effort (person-months) = a × (KLOC)^b
Development Time (months) = c × (Effort)^d
```

**2. Intermediate COCOMO**

- Adds 15 cost drivers (product, hardware, personnel, project attributes)
- More accurate than Basic

**3. Detailed COCOMO**

- Phase-wise estimation
- Most accurate, most complex

**Three Project Types:**

| **Type**                   | **a** | **b** | **c** | **d** | **Examples**                         |
| -------------------------- | ----- | ----- | ----- | ----- | ------------------------------------ |
| **Organic** (Simple)       | 2.4   | 1.05  | 2.5   | 0.38  | Small business apps, data entry      |
| **Semi-Detached** (Medium) | 3.0   | 1.12  | 2.5   | 0.35  | Medium complexity, some integration  |
| **Embedded** (Complex)     | 3.6   | 1.20  | 2.5   | 0.32  | Real-time, embedded, safety-critical |

**Example (Organic Project):**

- Size: 10 KLOC
- Effort = 2.4 × (10)^1.05 = 2.4 × 11.22 = 27 person-months
- Time = 2.5 × (27)^0.38 = 2.5 × 3.24 = 8.1 months
- Team size = 27 / 8.1 = 3.3 ≈ 3-4 people

**COCOMO II:**

- Modern version for iterative, reuse-based development
- Uses Function Points or Object Points instead of KLOC
- Better for Agile, component-based systems

---

## 📌 Parametric Productivity Model

> 🟢 **Tier C** | Frequency: 1/4 | Section: A

### Brief Overview

**Parametric Model** estimates effort using mathematical formulas based on project parameters (size, complexity, team capability).

**General Form:**

```
Effort = f(Size, Complexity, Team, Technology)
```

**Examples:**

- COCOMO (size-based)
- Function Point-based models
- Putnam's Model (SLIM)

**Key Concept:**
Use historical data from past projects to derive formula coefficients for your organization.

---

## 🎯 PYQ MODEL ANSWERS

### 🎯 PYQ [2021-22] - "Define Project Life Cycle" (Section A, 2 marks)

**Model Answer:**

Project Life Cycle is the series of phases a project passes through from initiation to closure. It includes five phases: (1) Initiation - define project and get approval, (2) Planning - create roadmap and baselines, (3) Execution - build deliverables, (4) Monitoring & Controlling - track performance, (5) Closure - formal handover and lessons learned. Each phase has specific activities and deliverables.

---

### 🎯 PYQ [2021-22] - "Discuss about the Effort Estimation" (Section A, 2 marks)

**Model Answer:**

Effort Estimation is the process of predicting the amount of work (person-hours or person-months) required to complete project activities. Techniques include: (1) Expert Judgment - experience-based, (2) Analogous - compare with similar past projects, (3) Parametric - use formulas like COCOMO, (4) Function Points - count user functionality. Accurate estimation is critical for realistic planning, budgeting, and resource allocation.

---

### 🎯 PYQ [2021-22, 2022-23, 2023-24] - "Write short notes on: (i) Software process and Process Models (ii) Choice of Process models (iii) Rapid Application Development (RAD)" (Section B, 10 marks)

**Model Answer:**

**(i) Software Process and Process Models:**

Software Process is the set of activities and tasks required to develop software, including specification, design, development, validation, and evolution.

Process Model is an abstract representation that describes the workflow, sequence, and structure of these activities.

**Common Process Models:**

- **Waterfall:** Linear, sequential phases (requirements → design → development → testing → deployment). Best for stable requirements.
- **Iterative:** Repeated cycles of development, each improving the system. Allows refinement.
- **Incremental:** System developed in parts, each increment adds functionality. Early delivery of partial system.
- **Spiral:** Risk-driven, combines iterative + prototyping. Good for high-risk projects.
- **Agile:** Adaptive, customer collaboration, iterative 2-week sprints. Best for evolving requirements.

**(ii) Choice of Process Models:**

Selection depends on:

**1. Requirements Clarity:**

- Clear, stable → Waterfall
- Unclear, evolving → Agile, RAD

**2. Project Size:**

- Small (< 6 months) → Agile, RAD
- Large (> 1 year) → Incremental, Spiral

**3. Risk Level:**

- High risk → Spiral (risk-driven iterations)
- Low risk → Waterfall

**4. Customer Involvement:**

- High availability → Agile, RAD
- Limited availability → Waterfall, Incremental

**5. Team Experience:**

- Experienced → Agile, XP
- Mixed experience → Waterfall (well-defined roles)

**6. Time Constraints:**

- Tight deadline → RAD, Agile
- Flexible timeline → Waterfall

**7. Criticality:**

- Safety-critical → Waterfall (extensive documentation, testing)
- Non-critical → Agile

**Decision Matrix Example:**

| **Factor**             | **Waterfall** | **Agile**    | **RAD**   | **Spiral** |
| ---------------------- | ------------- | ------------ | --------- | ---------- |
| Requirements Stability | High          | Low          | Medium    | Medium     |
| Project Size           | Large         | Small-Medium | Small     | Large      |
| Time to Market         | Slow          | Fast         | Very Fast | Medium     |
| Customer Availability  | Low           | High         | High      | Medium     |
| Documentation Need     | High          | Low          | Low       | Medium     |

**(iii) Rapid Application Development (RAD):**

RAD is a methodology focused on rapid prototyping and quick delivery, typically 60-90 days.

**Four Phases:**

1. **Requirements Planning (10-15% time):**
   - High-level requirements
   - Define critical features
   - Identify success criteria

2. **User Design (40-50% time):**
   - Build prototypes iteratively
   - JAD (Joint Application Development) workshops
   - Continuous user feedback
   - Refine UI/UX

3. **Construction (30-40% time):**
   - Convert prototype to production code
   - Use code generators, reusable components
   - Continuous integration and testing

4. **Cutover (5-10% time):**
   - User acceptance testing
   - Training and deployment
   - Data migration

**Key Features:**

- **Speed:** 60-90 day delivery
- **Prototyping:** Build working models quickly
- **User Involvement:** Daily collaboration
- **Reusability:** Leverage existing components
- **Small Teams:** 2-6 people, co-located

**When to Use:**

- ✅ Time-critical projects
- ✅ UI-intensive applications
- ✅ Users available for continuous input
- ✅ Requirements can be modularized

**When NOT to Use:**

- ❌ Large, complex systems
- ❌ Safety-critical applications
- ❌ High technical risk
- ❌ Users unavailable

**Advantages:** Fast, flexible, high user satisfaction
**Disadvantages:** Requires skilled team, not scalable, limited documentation

---

### 🎯 PYQ [2021-22, 2022-23, 2023-24] - "What is the concept and need of Agile methods in Project Life Cycle?" (Section C, 10/7 marks)

**Model Answer:**

**Concept of Agile:**

Agile is an iterative, incremental approach to software development that emphasizes flexibility, customer collaboration, and rapid delivery of working software.

**Core Philosophy - Agile Manifesto:**

1. Individuals and interactions > Processes and tools
2. Working software > Comprehensive documentation
3. Customer collaboration > Contract negotiation
4. Responding to change > Following a plan

**How Agile Works:**

**Iterative Development:**

- Work divided into short iterations (sprints): 1-4 weeks, typically 2 weeks
- Each sprint delivers potentially shippable increment
- At sprint end: working software demonstrated to stakeholders

**Key Practices:**

- **Daily Standups:** 15-min sync meetings
- **Sprint Planning:** Select features for sprint
- **Sprint Review:** Demo completed work
- **Retrospective:** Reflect and improve
- **Continuous Integration:** Frequent code merges, automated testing

**Scrum Framework:**

- **Roles:** Product Owner, Scrum Master, Development Team
- **Artifacts:** Product Backlog, Sprint Backlog, Increment
- **Events:** Sprint, Sprint Planning, Daily Standup, Review, Retrospective

**Need for Agile in Project Life Cycle:**

**1. Handle Changing Requirements:**

- **Traditional Problem:** Requirements freeze upfront, changes costly
- **Agile Solution:** Welcome changes even late in development
- **Benefit:** Adapt to market shifts, user feedback, technology evolution
- **Example:** E-commerce app - add payment method mid-project based on competitor launch

**2. Reduce Risk:**

- **Traditional Problem:** Single big-bang delivery at end, late feedback
- **Agile Solution:** Incremental delivery, frequent validation
- **Benefit:** Detect issues early when cheap to fix
- **Example:** Prototype UI in Sprint 1, get feedback, avoid costly rework later

**3. Faster Time-to-Market:**

- **Traditional Problem:** 6-12 month wait for any usable product
- **Agile Solution:** Working software every 2 weeks
- **Benefit:** Early value delivery, competitive advantage
- **Example:** Release MVP in 2 months, full product in 6 months vs. 12-month waterfall

**4. Better Quality:**

- **Traditional Problem:** Testing at end, defects pile up
- **Agile Solution:** Continuous testing, TDD, pair programming
- **Benefit:** Fewer defects, better code quality
- **Example:** XP practices - write tests before code, refactor continuously

**5. Improved Customer Satisfaction:**

- **Traditional Problem:** Customer sees product only at end, often not what they wanted
- **Agile Solution:** Customer involved every sprint, sees progress
- **Benefit:** Product matches customer expectations
- **Example:** Customer reprioritizes backlog each sprint based on demos

**6. Team Empowerment and Motivation:**

- **Traditional Problem:** Hierarchical, developers just code to spec
- **Agile Solution:** Self-organizing teams, collective ownership
- **Benefit:** Higher morale, productivity, innovation
- **Example:** Team decides how to implement features, owns quality

**7. Transparency and Visibility:**

- **Traditional Problem:** Status unclear until late, surprises at end
- **Agile Solution:** Daily progress visible via burndown charts, sprint demos
- **Benefit:** Stakeholders always know project status
- **Example:** Management sees velocity dropping, addresses issues immediately

**Integration in Project Life Cycle:**

**Initiation:** Define product vision, create initial backlog
**Planning:** High-level roadmap, release plan (not detailed)
**Execution:** Sprints - plan, develop, test, review, repeat
**Monitoring:** Daily standups, burndown charts, velocity tracking
**Closure:** Final sprint, retrospective, handover

**When Agile is Most Needed:**

| **Situation**                | **Why Agile**                              |
| ---------------------------- | ------------------------------------------ |
| Startup building new product | Requirements unclear, need rapid iteration |
| Competitive market           | Fast releases to stay ahead                |
| Mobile app development       | User preferences change quickly            |
| Innovation projects          | Experimentation and pivots needed          |
| Customer-facing apps         | Continuous user feedback critical          |

**Conclusion:**

Agile is not just a methodology but a mindset shift. In today's fast-paced, uncertain business environment, the ability to adapt quickly is crucial. Agile's iterative nature, customer focus, and emphasis on working software make it essential for modern software projects, especially where requirements evolve, time-to-market matters, and customer satisfaction is paramount.

---

### 🎯 PYQ [2022-23] - "Discuss Function Point and compare it with Lines of Code" (Section A, 2 marks)

**Model Answer:**

Function Point (FP) measures software size based on user functionality (inputs, outputs, queries, files) independent of technology. Lines of Code (LOC) counts physical code lines. FP advantages: (1) Technology-independent, (2) Can estimate before coding, (3) Measures user value. LOC problems: (1) Language-dependent, (2) Available only after coding, (3) Encourages verbose code. FP is superior for early estimation and cross-project comparison.

---

### 🎯 PYQ [2022-23] - "Outline COSMIC full function points for software cost estimation" (Section B, 10 marks)

**Model Answer:**

**COSMIC Full Function Points (CFP):**

COSMIC (Common Software Measurement International Consortium) is a second-generation function point method designed for modern software including real-time, embedded, and layered systems.

**Core Concept:**

COSMIC measures software size based on **data movement** rather than data storage or transaction types like traditional FP.

**Four Types of Data Movements:**

**1. Entry (E):**

- **Definition:** Data moves from user (or external system) into the functional process
- **Example:** User enters order details into form
- **Count:** 1 CFP per unique entry

**2. Exit (X):**

- **Definition:** Data moves from functional process to user (or external system)
- **Example:** System displays order confirmation to user
- **Count:** 1 CFP per unique exit

**3. Read (R):**

- **Definition:** Data moves from persistent storage into functional process
- **Example:** Process reads customer data from database
- **Count:** 1 CFP per unique read

**4. Write (W):**

- **Definition:** Data moves from functional process to persistent storage
- **Example:** Process writes order to database
- **Count:** 1 CFP per unique write

**Measurement Process:**

**Step 1: Identify Functional Processes**

- Decompose software into functional processes (user-triggered actions)
- Example in e-commerce: "Place Order", "View Order History", "Process Payment"

**Step 2: Identify Data Movements for Each Process**

- For "Place Order" process:
  - Entry (E): User enters order details → 1 CFP
  - Read (R): System reads product info from DB → 1 CFP
  - Read (R): System reads customer info from DB → 1 CFP
  - Write (W): System saves order to DB → 1 CFP
  - Exit (X): System displays confirmation to user → 1 CFP
  - **Total for "Place Order":** 5 CFP

**Step 3: Count All Data Movements**

- Sum CFP across all functional processes
- Example: If 20 processes, each averaging 4 movements = 80 CFP

**Step 4: Convert to Effort**

```
Effort = CFP × Hours per CFP
```

Typical: 5-15 hours per CFP depending on technology and team

**Example Calculation:**

**Online Banking System:**

| **Functional Process**   | **E** | **X** | **R** | **W** | **Total CFP** |
| ------------------------ | ----- | ----- | ----- | ----- | ------------- |
| Login                    | 1     | 1     | 1     | 0     | 3             |
| View Account Balance     | 0     | 1     | 2     | 0     | 3             |
| Transfer Money           | 1     | 1     | 3     | 2     | 7             |
| View Transaction History | 1     | 1     | 1     | 0     | 3             |
| Change Password          | 1     | 1     | 1     | 1     | 4             |

**Total Size:** 3 + 3 + 7 + 3 + 4 = **20 CFP**

**Effort Estimation:**

- Assume 10 hours per CFP
- Total Effort = 20 × 10 = 200 person-hours
- Team of 2 people: 200 / 2 = 100 hours each
- At 40 hours/week: 2.5 weeks

**Advantages of COSMIC:**

**1. Simplicity:**

- No complexity adjustment (unlike traditional FP's VAF)
- Straightforward counting rules
- Less subjective

**2. Applicability:**

- ✅ Real-time systems (embedded software)
- ✅ Scientific applications
- ✅ Multi-layered architectures (frontend, middleware, backend)
- ✅ Service-oriented architectures (SOA)
- Traditional FP struggles with these

**3. Accuracy:**

- More granular measurement
- Better correlation with effort
- Reflects actual processing logic

**4. Standardization:**

- ISO/IEC 19761 standard
- Widely adopted internationally
- Good for benchmarking

**Comparison: Traditional FP vs. COSMIC:**

| **Aspect**     | **Traditional FP**             | **COSMIC CFP**               |
| -------------- | ------------------------------ | ---------------------------- |
| **Focus**      | Data storage + transactions    | Data movement                |
| **Components** | 5 types (EI, EO, EQ, ILF, EIF) | 4 types (E, X, R, W)         |
| **Complexity** | 3 levels (Low, Avg, High)      | No complexity levels         |
| **Adjustment** | VAF (0.65-1.35)                | No adjustment                |
| **Best For**   | Business applications, CRUD    | Real-time, embedded, layered |
| **Ease**       | More complex                   | Simpler                      |

**Cost Estimation Using COSMIC:**

**Step 1: Measure Size (CFP)**
**Step 2: Determine Productivity Rate**

- Historical data: Your team's average hours per CFP
- Industry benchmarks: 5-15 hours/CFP

**Step 3: Calculate Effort**

```
Effort = CFP × Hours per CFP
```

**Step 4: Calculate Cost**

```
Cost = Effort × Hourly Rate
```

**Example:**

- Size: 250 CFP
- Productivity: 8 hours/CFP
- Effort: 250 × 8 = 2,000 hours
- Hourly Rate: $50/hour
- **Total Cost:** 2,000 × $50 = **$100,000**

**Conclusion:**

COSMIC Full Function Points provide a modern, accurate, and simpler alternative to traditional FP, especially for complex systems. By focusing on data movements, COSMIC better captures the true functional size of software, leading to more reliable cost and effort estimates. It's particularly valuable for real-time systems, embedded software, and architectures where traditional FP falls short.

---

### 🎯 PYQ [2023-24] - "Calculate the function point value for a project with the following information domain characteristics..." (Section B, 10 marks)

**Given:**

- Number of user inputs = 30
- Number of user outputs = 42
- Number of user enquiries = 08
- Number of files = 07
- Number of external interfaces = 06
- All complexity adjustment values are moderate
- Weighting factors (Average column):
  - EI: 10, EO: 7, EQ: 4, ILF: 5, EIF: 4

**Model Answer:**

**Step 1: Identify Components and Counts**

| Component                      | Count |
| ------------------------------ | ----- |
| External Inputs (EI)           | 30    |
| External Outputs (EO)          | 42    |
| External Inquiries (EQ)        | 8     |
| Internal Logical Files (ILF)   | 7     |
| External Interface Files (EIF) | 6     |

**Step 2: Apply Weights (Average Complexity)**

Given weights (from table):

- EI weight: 10
- EO weight: 7
- EQ weight: 4
- ILF weight: 5
- EIF weight: 4

**Step 3: Calculate Unadjusted Function Points (UFP)**

```
UFP = (EI × Weight) + (EO × Weight) + (EQ × Weight) + (ILF × Weight) + (EIF × Weight)

UFP = (30 × 10) + (42 × 7) + (8 × 4) + (7 × 5) + (6 × 4)
    = 300 + 294 + 32 + 35 + 24
    = 685
```

**Step 4: Calculate Value Adjustment Factor (VAF)**

Since all complexity adjustment values are **moderate**, we assume each of the 14 General System Characteristics (GSC) is rated as **3**.

```
Total Degree of Influence (TDI) = 14 × 3 = 42

VAF = 0.65 + (0.01 × TDI)
    = 0.65 + (0.01 × 42)
    = 0.65 + 0.42
    = 1.07
```

**Step 5: Calculate Adjusted Function Points (AFP)**

```
AFP = UFP × VAF
    = 685 × 1.07
    = 732.95
    ≈ 733 Function Points
```

**Final Answer:**

The function point value for this project is **733 FP**.

**Interpretation:**
This is a medium to large-sized project with significant functionality.

**Effort Estimation Example:**
If we assume an average of 10 hours per function point:

- Total Effort = 733 × 10 = 7,330 person-hours
- With a team of 5 people: 7,330 / 5 = 1,466 hours per person
- At 40 hours/week: 1,466 / 40 = 36.6 weeks ≈ **9 months**

---

### 🎯 PYQ [2024-25] - "What is the agile methodology?" (Section A, 2 marks)

**Model Answer:**

Agile methodology is an iterative software development approach that delivers working software in short cycles (sprints of 1-4 weeks), emphasizing customer collaboration, flexibility to change, and continuous improvement. Core values include: individuals over processes, working software over documentation, customer collaboration over contracts, and responding to change over following plans. Popular frameworks: Scrum, XP, Kanban.

---

### 🎯 PYQ [2024-25] - "What are the different stages of project life cycle?" (Section A, 2 marks)

**Model Answer:**

Project Life Cycle has five stages: (1) **Initiation** - define project, conduct feasibility, get approval, (2) **Planning** - create detailed roadmap, schedule, budget, baselines, (3) **Execution** - develop deliverables, manage team, (4) **Monitoring & Controlling** - track performance, implement changes, report status (runs parallel to execution), (5) **Closure** - obtain acceptance, handover, lessons learned, release resources.

---

### 🎯 PYQ [2024-25] - "Explain the significant features of the RAD model for software development" (Section B, 7 marks)

**Model Answer:**

**Rapid Application Development (RAD) - Significant Features:**

**1. Speed and Time-Boxing:**

- **Feature:** Complete projects in 60-90 days
- **Mechanism:** Strict timeboxes for each phase, parallel development
- **Benefit:** Fast time-to-market, competitive advantage
- **Example:** E-commerce site launched in 75 days vs. 6 months traditional

**2. Prototyping-Centric:**

- **Feature:** Build working prototypes iteratively from day one
- **Mechanism:** Start with basic prototype, add features incrementally
- **Benefit:** Visualize system early, clarify requirements, reduce rework
- **Example:** UI prototype in week 1, add backend functionality week 2-3

**3. Active User Involvement:**

- **Feature:** Daily collaboration with end users
- **Mechanism:** Joint Application Development (JAD) workshops, daily feedback sessions
- **Benefit:** Ensures system meets actual needs, high user satisfaction
- **Example:** Users test prototype daily, suggest changes immediately

**4. Component Reusability:**

- **Feature:** Leverage pre-built components, frameworks, code generators
- **Mechanism:** Library of reusable modules, drag-and-drop tools
- **Benefit:** Reduce development time by 40-60%
- **Example:** Use pre-built authentication module instead of building from scratch

**5. Small, Skilled Teams:**

- **Feature:** 2-6 member cross-functional teams
- **Mechanism:** Co-located team with all needed skills (developer, designer, tester)
- **Benefit:** Fast communication, quick decisions, no handoff delays
- **Example:** Team sits together, resolves issues in minutes vs. days

**6. Minimal Planning and Documentation:**

- **Feature:** Just-enough planning, focus on working software
- **Mechanism:** High-level requirements, no detailed specs, code is documentation
- **Benefit:** More time on building, less on paperwork
- **Example:** 10-page requirements doc vs. 100-page in waterfall

**7. Iterative Refinement:**

- **Feature:** Continuous improvement cycles
- **Mechanism:** Build → Demo → Feedback → Refine → Repeat
- **Benefit:** Each iteration is better, converges to user needs
- **Example:** Version 1 (basic), Version 2 (refined UI), Version 3 (optimized)

**8. Flexibility:**

- **Feature:** Welcome changes throughout development
- **Mechanism:** Modular design, loose coupling
- **Benefit:** Adapt to changing business needs
- **Example:** Add payment gateway mid-project without disrupting existing features

**9. Risk Reduction:**

- **Feature:** Early and frequent validation
- **Mechanism:** Users see progress weekly, validate functionality
- **Benefit:** Catch misunderstandings early when cheap to fix
- **Example:** Discover wrong report format in week 2, not at end

**10. Automated Tools:**

- **Feature:** Heavy reliance on CASE tools, code generators, low-code platforms
- **Mechanism:** Visual development, automatic code generation
- **Benefit:** 3-5x productivity boost
- **Example:** Generate CRUD operations automatically from database schema

**Comparison: RAD vs. Waterfall:**

| **Feature**      | **RAD**       | **Waterfall**           |
| ---------------- | ------------- | ----------------------- |
| Duration         | 60-90 days    | 6-18 months             |
| Prototyping      | Core activity | Optional                |
| User Involvement | Daily         | Requirements phase only |
| Documentation    | Minimal       | Extensive               |
| Flexibility      | High          | Low                     |
| Team Size        | 2-6           | 10+                     |

**Conclusion:**

RAD's significant features make it ideal for time-critical projects with available users and modular requirements. Its emphasis on speed, prototyping, and user collaboration delivers systems that closely match user needs in a fraction of traditional timelines.

---

### 🎯 PYQ [2024-25] - "What is the COCOMO II model? Explain its components and how it is used in software cost estimation" (Section C, 7 marks)

**Model Answer:**

**COCOMO II (COnstructive COst MOdel II):**

COCOMO II is a modern software cost estimation model developed by Dr. Barry Boehm (1997) to address limitations of original COCOMO (1981), particularly for iterative development, component reuse, and rapid development environments.

**Need for COCOMO II:**

- Original COCOMO assumed waterfall model
- Didn't handle reuse, COTS integration, rapid development
- Based on 1970s-80s projects
- COCOMO II designed for 1990s+ practices: object-oriented, reuse, Agile

**Three Sub-Models:**

**1. Application Composition Model:**

- **For:** Early prototyping, very high-level estimation
- **Size Metric:** Object Points or Function Points
- **Use Case:** RAD, 4GL projects, GUI-heavy applications
- **Formula:**
  ```
  Effort = (Object Points × Productivity Rate)
  ```

**2. Early Design Model:**

- **For:** After requirements, before detailed design
- **Size Metric:** Function Points or Unadjusted Function Points (UFP)
- **Accuracy:** ±20-30%
- **Use Case:** Proposal, feasibility stage
- **Formula:**
  ```
  Effort = A × (Size)^E × Π(Early Cost Drivers)
  Where E is determined by scale factors
  ```

**3. Post-Architecture Model:**

- **For:** After architecture is defined
- **Size Metric:** Source Lines of Code (SLOC) or Function Points
- **Accuracy:** ±10-15%
- **Use Case:** Detailed planning, budgeting
- **Formula:**
  ```
  Effort (PM) = A × (Size)^E × Π(EM)
  Where:
  - PM = Person-Months
  - A = Constant (2.94 for COCOMO II)
  - Size = KSLOC (thousands of source lines)
  - E = Exponent derived from Scale Factors
  - EM = Effort Multipliers from 17 cost drivers
  ```

**Key Components of COCOMO II:**

**1. Scale Factors (5 factors, determine exponent E):**

| **Scale Factor**                        | **Range** | **Description**                       |
| --------------------------------------- | --------- | ------------------------------------- |
| **Precedentedness (PREC)**              | 0-5       | Familiarity with project type         |
| **Development Flexibility (FLEX)**      | 0-5       | Conformance to requirements/specs     |
| **Architecture/Risk Resolution (RESL)** | 0-5       | Risk management, architecture clarity |
| **Team Cohesion (TEAM)**                | 0-5       | Stakeholder cooperation               |
| **Process Maturity (PMAT)**             | 0-5       | CMM/CMMI level                        |

**Exponent Calculation:**

```
B = 0.91 + 0.01 × Σ(Scale Factors)
E = B + 0.01 × Special Factor

Typical E range: 1.0 to 1.3
```

**2. Effort Multipliers (17 Cost Drivers):**

**Product Attributes (5):**

- RELY (Required Reliability): Very Low to Very High
- DATA (Database Size): Low to Very High
- CPLX (Product Complexity): Very Low to Extra High
- RUSE (Required Reusability): Low to Very High
- DOCU (Documentation Match): Very Low to Very High

**Platform Attributes (3):**

- TIME (Execution Time Constraint): Nominal to Extra High
- STOR (Main Storage Constraint): Nominal to Extra High
- PVOL (Platform Volatility): Low to Very High

**Personnel Attributes (5):**

- ACAP (Analyst Capability): Very Low to Very High
- PCAP (Programmer Capability): Very Low to Very High
- PCON (Personnel Continuity): Very Low to Very High
- APEX (Application Experience): Very Low to Very High
- PLEX (Platform Experience): Very Low to Very High

**Project Attributes (4):**

- TOOL (Tool Support): Very Low to Very High
- SITE (Multi-site Development): Very Low to Very High
- SCED (Schedule Constraint): Very Low to Very High
- LTEX (Language & Tool Experience): Very Low to Very High

**Each driver has multiplier values:**

- Very Low: 0.75 - 0.85 (reduces effort)
- Low: 0.88 - 0.95
- Nominal: 1.00 (baseline)
- High: 1.07 - 1.15
- Very High: 1.20 - 1.50 (increases effort)
- Extra High: 1.30 - 1.70

**Cost Estimation Process:**

**Step 1: Estimate Size**

- Count SLOC (Source Lines of Code) or Function Points
- Example: 50,000 lines of code = 50 KSLOC

**Step 2: Determine Scale Factors**

- Rate each of 5 scale factors (0-5)
- Example: PREC=3, FLEX=4, RESL=3, TEAM=4, PMAT=3
- Sum = 17
- E = 0.91 + (0.01 × 17) = 1.08

**Step 3: Determine Effort Multipliers**

- Rate all 17 cost drivers
- Example:
  - RELY=High (1.10), CPLX=High (1.17), ACAP=High (0.85)
  - Product of all 17 multipliers = 1.24

**Step 4: Calculate Effort**

```
Effort = 2.94 × (50)^1.08 × 1.24
       = 2.94 × 62.5 × 1.24
       = 228 person-months
```

**Step 5: Calculate Schedule**

```
Schedule = C × (Effort)^F
Where:
- C = 3.67 (constant)
- F = 0.28 + 0.2 × (E - 0.91) = 0.28 + 0.2 × 0.17 = 0.314

Schedule = 3.67 × (228)^0.314
         = 3.67 × 5.12
         = 18.8 months
```

**Step 6: Calculate Team Size**

```
Average Team Size = Effort / Schedule
                  = 228 / 18.8
                  = 12 people
```

**Advantages of COCOMO II:**

**1. Flexibility:**

- Three models for different project stages
- Suitable for waterfall, iterative, agile

**2. Realism:**

- Accounts for modern practices (reuse, COTS, rapid development)
- Based on contemporary project data

**3. Calibration:**

- Can be calibrated to organization's historical data
- Improves accuracy over time

**4. Comprehensive:**

- 22 factors capture project complexity
- More accurate than simple SLOC-based formulas

**5. Tool Support:**

- Commercial tools available (COCOMO II Suite)
- Automated calculation, sensitivity analysis

**Limitations:**

**1. Effort Intensive:**

- Requires detailed assessment of 22 factors
- Time-consuming for quick estimates

**2. Subjectivity:**

- Rating cost drivers involves judgment
- Different estimators may rate differently

**3. Data Dependency:**

- Accuracy depends on historical data quality
- New organizations lack calibration data

**4. SLOC Estimation:**

- Estimating SLOC before coding is difficult
- Function Points may be better for early estimates

**Conclusion:**

COCOMO II is a robust, comprehensive model for software cost estimation, particularly valuable for large projects where accuracy justifies the effort of detailed assessment. Its consideration of modern development practices, reuse, and team factors makes it more realistic than simple size-based formulas, though it requires expertise and historical data for optimal results.

---

## 📝 SECTION A QUICK-ANSWER BANK (Unit II)

| **Question**                                 | **Answer (2 marks)**                                                                                                                                                                                                                                                                                                                                     |
| -------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Define Project Life Cycle                    | Project Life Cycle is the series of phases from initiation to closure: (1) Initiation - define and approve, (2) Planning - create roadmap, (3) Execution - build deliverables, (4) Monitoring & Controlling - track and correct (parallel to execution), (5) Closure - handover and lessons learned.                                                     |
| What is Rapid Application Development (RAD)? | RAD is a methodology focused on rapid prototyping and delivery in 60-90 days through four phases: Requirements Planning, User Design (iterative prototyping with JAD workshops), Construction (convert prototype to production), Cutover (UAT and deployment). Emphasizes speed, user involvement, reusability, and small teams.                         |
| Define Agile methodology                     | Agile is an iterative approach delivering working software in short sprints (1-4 weeks) with continuous customer collaboration. Based on four values: individuals > processes, working software > documentation, collaboration > contracts, responding to change > following plan. Frameworks: Scrum, XP, Kanban.                                        |
| What is Scrum?                               | Scrum is an Agile framework with 3 roles (Product Owner, Scrum Master, Dev Team), 3 artifacts (Product Backlog, Sprint Backlog, Increment), and 5 events (Sprint, Sprint Planning, Daily Standup, Sprint Review, Retrospective). Delivers potentially shippable increments every 1-4 weeks.                                                              |
| What is Function Point?                      | Function Point (FP) measures software size based on user functionality (inputs, outputs, queries, files, interfaces) independent of technology. Calculated as UFP (count × weights) × VAF (adjustment factor 0.65-1.35). Used for early estimation, benchmarking, and productivity measurement. Better than LOC.                                         |
| What is COCOMO?                              | COCOMO (COnstructive COst MOdel) estimates effort and schedule based on size (KLOC). Formula: Effort = a × (KLOC)^b. Three types: Organic (simple, a=2.4, b=1.05), Semi-detached (medium, a=3.0, b=1.12), Embedded (complex, a=3.6, b=1.20). COCOMO II is modern version for iterative, reuse-based development.                                         |
| Explain Extreme Programming (XP)             | XP is an Agile methodology emphasizing engineering practices: Pair Programming (two devs, one workstation), Test-Driven Development (write test first), Continuous Integration (integrate multiple times daily), Simple Design (simplest that works), Refactoring (continuous improvement), Collective Code Ownership, Sustainable Pace (40-hour weeks). |
| What is Sprint in Scrum?                     | Sprint is a time-boxed iteration (1-4 weeks, typically 2) in Scrum where team delivers potentially shippable increment. Includes Sprint Planning (select work), Daily Standup (sync), Development (build), Sprint Review (demo), Retrospective (improve). Scope frozen during sprint; no changes allowed.                                                |
| List advantages of RAD                       | RAD advantages: (1) Fast delivery (60-90 days), (2) High user satisfaction (continuous involvement), (3) Flexibility to changes, (4) Early risk identification (prototypes), (5) Reduced costs (reusability), (6) Better quality (iterative feedback). Best for time-critical, UI-intensive, small-medium projects.                                      |
| What is COSMIC Full Function Points?         | COSMIC (CFP) measures size by data movements: Entry (user→system), Exit (system→user), Read (storage→process), Write (process→storage). Each movement = 1 CFP. Simpler than traditional FP (no complexity, no VAF). Better for real-time, embedded, layered systems. ISO/IEC 19761 standard.                                                             |
| Explain Test-Driven Development              | TDD is XP practice: (1) Write failing test (Red), (2) Write minimal code to pass (Green), (3) Refactor (improve design). Ensures 100% test coverage, prevents regressions, improves design (testable code is good code). Tests serve as documentation and safety net for refactoring.                                                                    |

---

## 💡 EXAM ANSWER TIPS - UNIT II

### For 2-Mark Questions (Section A):

**RAD/Agile questions:**

- Line 1: Definition
- Line 2-3: 2-3 key features or principles
- Example if space permits

**Life Cycle questions:**

- List all 5 phases with one-line description each
- No need for detailed activities in 2-mark answers

### For 7-Mark Questions (Section B):

**RAD/Agile Explanation:**

- Introduction: 2-3 lines
- Key Features/Principles: 4-5 points with brief explanation
- When to use / Advantages: 2-3 points
- Conclusion: 1-2 lines

**Function Point Calculation:**

- Show all steps clearly
- Create table for organized presentation
- Box final answer

### For 7/10-Mark Numerical (Function Points):

**Step-by-step approach:**

1. Write formula first
2. Create table showing components, counts, weights
3. Calculate UFP (show calculation)
4. Calculate VAF (show TDI calculation)
5. Calculate AFP = UFP × VAF
6. Box final answer with "Function Points" unit
7. Optional: Show effort conversion example

**Time: 20-25 minutes for numerical**

### For 7/10-Mark Theory (Agile, RAD, COCOMO):

**Structure:**

- Introduction + Definition: 3-4 lines
- Main body with headings:
  - RAD: 4 phases with activities
  - Agile: Values, principles, Scrum framework
  - COCOMO: Formula, scale factors, cost drivers
- Comparison table (RAD vs Waterfall, Agile vs Traditional)
- Example scenario
- Conclusion: Benefits and when to use

**Include simple diagram if time permits**

### Common Mistakes to Avoid:

1. ❌ Confusing UFP with AFP (AFP = UFP × VAF)
2. ❌ Missing VAF calculation in FP problems
3. ❌ Not showing units (Function Points, person-months)
4. ❌ Mixing RAD and Agile concepts (they're different)
5. ❌ Writing Scrum events without explaining their purpose
6. ❌ Not creating comparison tables (very valuable in exam)

### Keywords to Use:

- **RAD:** Prototyping, JAD workshops, timeboxing, reusability
- **Agile:** Iterative, sprint, retrospective, self-organizing, customer collaboration
- **FP:** Technology-independent, user functionality, UFP, VAF, early estimation
- **COCOMO:** Parametric, scale factors, effort multipliers, calibration

---

## 📊 UNIT II SUMMARY

**Tier A Topics (Must Master):**

1. ✅ RAD Model (4 phases, when to use, advantages)
2. ✅ Agile Methodologies (values, principles, Scrum framework)
3. ✅ Function Points (calculation with UFP, VAF - practice 3-5 numerical)
4. ✅ Project Life Cycle (5 phases)

**Tier B Topics (Should Cover):**

1. ✅ COSMIC Full Function Points (data movements)
2. ✅ Extreme Programming (XP practices)

**Tier C Topics (Low Priority, skim only):**

1. Software Process Models (brief overview)
2. COCOMO Model (only if time permits)
3. Parametric Models (brief mention)

**Time Investment:**

- Tier A: 7-8 hours (including numerical practice)
- Tier B: 2 hours
- Tier C: 1 hour (skim)
- **Total: 10 hours for Unit II**

**Practice Required:**

- ✅ Solve 5 Function Point numerical problems
- ✅ Draw Scrum framework diagram
- ✅ Create RAD vs Waterfall comparison table
- ✅ Memorize Agile values and key principles
- ✅ Practice FP formulas: UFP = Σ(count × weight), AFP = UFP × VAF

---

**✅ Unit 2 Notes Complete!**

Type **'next'** to proceed to **Unit 3 notes** (Activity Planning and Risk Management) - the MOST IMPORTANT UNIT with CPM/PERT guaranteed questions!
