# UNIT 3: Activity Planning aur Risk Management

**Is unit me kya-kya aayega:**

- Activity planning objectives
- Project schedules
- Network planning
- Forward pass aur backward pass
- Critical Path Method (CPM) - SUPER IMPORTANT
- PERT technique
- Risk identification aur assessment
- Risk management
- Resource allocation

---

## 📌 Activity Planning Ka Objective

> 🟢 **Tier C** | Frequency: 1/4 | Section: A + B

### Main Goals

**1. Feasibility Check:**

- Kya target date achieve kar sakte ho?
- Resource bottlenecks identify karo

**2. Resource Planning:**

- Kaunse resources kab chahiye
- Hiring, training plan karo

**3. Detailed Schedule:**

- Activities break karo
- Timeline set karo
- Milestones define karo

**4. Communication Tool:**

- Stakeholders ko timeline dikhao
- Coordination enable karo

**5. Risk Management:**

- Critical activities identify karo
- Float/slack find karo
- Contingencies plan karo

**6. Progress Tracking:**

- Baseline set karo
- Actual vs planned compare karo

---

## 📌 Project Schedules

> 🟡 **Tier B** | Frequency: 2/4 | Section: B + C

### Definition

**Schedule** ek timetable hai jo batata hai kab activities start aur finish hongi.

### Schedule Types

**Master Schedule:**

- High-level overview
- Months/quarters
- Executives ke liye

**Detailed Schedule:**

- Task-level detail
- Days/weeks
- Team ke liye

**Milestone Schedule:**

- Key deliverables only
- Decision points
- Checkpoints

### Formats

**1. Activity List (Table):**

- Simple, spreadsheet me
- Disadvantage: Dependencies clear nahi

**2. Gantt Chart (Bars):**

- Visual, timeline
- Disadvantage: CPM clear nahi

**3. Network Diagram (CPM/PERT):**

- Dependencies clear
- Critical path visible
- Best for scheduling analysis

---

## 📌 Activity Node Structure

> 🟡 **Tier B** | Frequency: 2/4 | Section: A

### Activity Node Format

```
┌──────────────────────────┐
│  Activity ID/Name        │
├────────────┬─────────────┤
│   EST      │     EFT     │
├────────────┼─────────────┤
│ Duration   │             │
├────────────┼─────────────┤
│   LST      │     LFT     │
├────────────┴─────────────┤
│   Float/Slack            │
└──────────────────────────┘
```

### Key Terms

- **EST:** Earliest Start Time (forward pass se)
- **EFT:** Earliest Finish Time = EST + Duration
- **LST:** Latest Start Time (backward pass se)
- **LFT:** Latest Finish Time = LST + Duration
- **Duration:** Task ka time
- **Float:** Delay kar sakte ho without delaying project

### Float Calculation

```
Float = LST - EST (or LFT - EFT)

Agar Float = 0: Critical activity (no flexibility)
Agar Float > 0: Non-critical (can delay by Float days)
```

---

## 📌 Critical Path Method (CPM) - MOST IMPORTANT

> 🔴 **Tier A** | Frequency: 4/4 | Section: C (Always appears!)

### Definition

**CPM** longest path find karta hai project network me. Ye path project ka minimum duration determine karta hai. Isi path ke activities delay hone par poora project delay hota hai.

### Key Concepts

**Critical Path:** Longest sequence of activities
**Critical Activities:** Float = 0 (no delay allowed)
**Non-Critical:** Float > 0 (can delay)

### CPM Steps

**Step 1: Activities List Banao**

- All tasks list karo
- Duration assign karo
- Dependencies identify karo

**Step 2: Network Diagram Draw Karo**

- Activity-on-Node (AON) use karo
- Boxes = activities
- Arrows = dependencies

**Step 3: Forward Pass (EST aur EFT Calculate)**

- Start se end tak
- EST = 0 for start
- EST of next = EFT of previous (or max if multiple predecessors)
- EFT = EST + Duration

**Step 4: Backward Pass (LST aur LFT Calculate)**

- End se start tak
- LFT = Project Duration for end
- LST = LFT - Duration
- LFT of previous = LST of next (or min if multiple successors)

**Step 5: Calculate Float**

- Float = LST - EST
- Float = 0: Critical

**Step 6: Identify Critical Path**

- All activities with Float = 0
- Trace from start to end

### CPM Example (Simple)

```
Activities:
A (5 days), B (3 days, depends on A), C (4 days, depends on B)

Forward Pass:
A: EST=0, EFT=5
B: EST=5, EFT=8
C: EST=8, EFT=12

Backward Pass (Project duration = 12):
C: LFT=12, LST=8
B: LFT=8, LST=5
A: LFT=5, LST=0

Float Calculation:
A: Float = 0-0 = 0 (Critical)
B: Float = 5-5 = 0 (Critical)
C: Float = 8-8 = 0 (Critical)

Critical Path: A → B → C (12 days)
```

### CPM Benefits

✅ Project duration determine ho jata hai
✅ Critical activities identify ho jaate hain
✅ Float calculation se priority manage ho sakti hai
✅ What-if analysis possible hoti hai
✅ Progress monitoring easy hoti hai

### Crashing the Schedule

Agar deadline earlier ho to:

1. Critical activities identify karo
2. Resources add karo (overtime, more people)
3. Duration reduce karo
4. Cost increase hota hai usually

---

## 📌 Forward Pass aur Backward Pass

> 🔴 **Tier A** | Frequency: 3/4 | Section: C

### Forward Pass (Calculate EST aur EFT)

**Purpose:** Earliest times find karna

**Rules:**

- Start activity: EST = 0
- EFT = EST + Duration
- Multiple predecessors: EST = MAX(predecessors' EFT)

**Example:**

```
Activity A: EST=0, Duration=5, EFT=5
Activity B: EST=5, Duration=3, EFT=8
Activity C: Depends on B, EST=8, Duration=4, EFT=12

Project Duration = Max(all EFT) = 12
```

### Backward Pass (Calculate LST aur LFT)

**Purpose:** Latest times find karna (without delaying project)

**Rules:**

- End activity: LFT = Project Duration
- LST = LFT - Duration
- Multiple successors: LFT = MIN(successors' LST)

**Example (working backward from 12):**

```
Activity C: LFT=12, Duration=4, LST=8
Activity B: LFT=8, Duration=3, LST=5
Activity A: LST=0, Duration=5, LST=0
```

---

## 📌 PERT Technique

> 🔴 **Tier A** | Frequency: 3/4 | Section: B + C

### Definition

**PERT** use hota hai jab activity duration uncertain hote hain.

### Three Time Estimates

**Optimistic (O):** Best case scenario, best effort, everything goes right

**Most Likely (M):** Most probable estimate, normal conditions

**Pessimistic (P):** Worst case, everything goes wrong

### Expected Time Formula

```
TE = (O + 4M + P) / 6

Most Likely ko 4x weight dete ho kyunki wo most probable hai.
```

### Variance aur Standard Deviation

```
Variance = [(P - O) / 6]²

Standard Deviation = (P - O) / 6
```

**High variance = High uncertainty**

### Example

```
Activity Coding:
Optimistic: 5 days
Most Likely: 8 days
Pessimistic: 17 days

TE = (5 + 4×8 + 17) / 6 = (5 + 32 + 17) / 6 = 54 / 6 = 9 days

StdDev = (17 - 5) / 6 = 2 days

Confidence Level:
- 1 StdDev (68%): 7-11 days
- 2 StdDev (95%): 5-13 days
```

### When to Use PERT

✅ High uncertainty projects
✅ R&D projects
✅ Novel technology

❌ Routine projects (overhead zyada)

---

## 📌 Risk Identification

> 🟡 **Tier B** | Frequency: varies | Section: varies

### How to Identify Risks

**1. Brainstorming:**

- Team members sabko ideas dete hain
- All possible risks list karo

**2. Expert Interviews:**

- Experienced people se pooch

**3. Lessons Learned:**

- Past projects se seekho

**4. Checklist:**

- Known risks ka checklist use karo

**Risk Categories:**

- Technical risks
- Schedule risks
- Cost risks
- Resource risks
- External risks

---

## 📌 Risk Assessment aur Planning

> 🟡 **Tier B** | Frequency: varies | Section: varies

### Assessment Process

**1. Probability:** Kitni likely?

- Very High: 75-100%
- High: 50-75%
- Medium: 25-50%
- Low: 5-25%
- Very Low: 0-5%

**2. Impact:** Agar happen to damage kitna?

- Critical: Major impact
- High: Significant impact
- Medium: Moderate
- Low: Minor
- Negligible: Negligible

**3. Risk Priority:**

- Risk = Probability × Impact
- Calculate priority

### Risk Response Strategies

**1. Avoid:** Risk ko completely avoid karo

**2. Mitigate:** Risk ko reduce karo

**3. Transfer:** Insurance, vendor ko pass karo

**4. Accept:** Risk le lo, contingency plan banao

---

## 📌 Monte Carlo Simulation

> 🟢 **Tier C** | Frequency: 0/4 | Section: Never appeared

**Concept:** Thousands scenarios generate karke outcomes analyze karo.

(Low priority - exam me rare hai)

---

## 📌 Resource Allocation

> 🟡 **Tier B** | Frequency: varies | Section: varies

**Goals:**

- Sahi skills wale resource sahi task par assign karo
- Overallocation avoid karo
- Efficient utilization

---

## 🎯 UNIT 3 KEY FORMULAS

**Forward Pass:**

```
EFT = EST + Duration
EST(next) = MAX(predecessors' EFT)
```

**Backward Pass:**

```
LST = LFT - Duration
LFT(previous) = MIN(successors' LST)
```

**Float:**

```
Float = LST - EST
Float = LFT - EFT
```

**PERT:**

```
TE = (O + 4M + P) / 6
StdDev = (P - O) / 6
```

---

## 📌 Exam Tips - Unit 3

**CPM/PERT numerical questions sab time aate hain (Section C):**

- Network diagram draw karna
- Forward pass karna
- Backward pass karna
- Critical path find karna
- Duration aur variance calculate karna

**Must master karo:**

- CPM process complete
- Forward/backward pass calculations
- Float calculation
- PERT three-estimate method

---

## 📌 Project Schedules

> 🟡 **Tier B** | Frequency: 2/4 | Section: B + C

### Definition

**Project Schedule** is a timetable showing when activities will start and finish, considering dependencies, resource availability, and constraints.

### Types of Schedules

**1. Master Schedule (High-Level)**

- Shows major phases and milestones
- Timeline: Months or quarters
- Audience: Executives, sponsors
- Example: Q1-Requirements, Q2-Development, Q3-Testing, Q4-Deployment

**2. Detailed Schedule (Granular)**

- Shows individual tasks and subtasks
- Timeline: Days or weeks
- Audience: Project team
- Example: Design database schema (3 days), Create ER diagram (2 days)

**3. Milestone Schedule**

- Shows key deliverables and decision points
- No activity details, only checkpoints
- Example: Requirements Approved (Mar 15), Design Complete (May 30)

### Three Forms of Presenting Schedule

**1. Activity List (Text Format)**

```
Task ID | Task Name           | Duration | Start Date | End Date   | Predecessors
--------|---------------------|----------|------------|------------|-------------
T1      | Requirements        | 10 days  | Jan 1      | Jan 10     | -
T2      | Design              | 15 days  | Jan 11     | Jan 25     | T1
T3      | Coding              | 20 days  | Jan 26     | Feb 14     | T2
```

**Advantages:**

- Simple, easy to create in spreadsheet
- Shows all details in tabular form

**Disadvantages:**

- Hard to visualize dependencies
- Difficult to see critical path

**2. Gantt Chart (Bar Chart)**

- Horizontal bars showing task duration
- X-axis: Timeline, Y-axis: Tasks
- Visual representation of schedule

**Advantages:**

- ✅ Easy to understand visually
- ✅ Shows timeline clearly
- ✅ Can show progress (% complete)
- ✅ Good for presentations

**Disadvantages:**

- ❌ Doesn't clearly show dependencies
- ❌ Hard to identify critical path
- ❌ Complex for large projects (100+ tasks)

**3. Network Diagram (CPM/PERT)**

- Nodes represent activities or events
- Arrows show dependencies
- Two types:
  - **Activity-on-Node (AON):** Activity in box, arrows show sequence
  - **Activity-on-Arrow (AOA):** Activity on arrow, nodes are events

**Advantages:**

- ✅ Shows dependencies clearly
- ✅ Easy to identify critical path
- ✅ Reveals parallel activities
- ✅ Best for scheduling analysis

**Disadvantages:**

- ❌ Complex to draw for large projects
- ❌ Not intuitive for non-technical stakeholders
- ❌ Doesn't show timeline on calendar

![Project Schedules Forms](diagrams/project_schedules.svg)

### Comparison of Schedule Formats

| **Aspect**             | **Activity List**                 | **Gantt Chart**                   | **Network Diagram**           |
| ---------------------- | --------------------------------- | --------------------------------- | ----------------------------- |
| **Ease of Creation**   | Easy                              | Medium                            | Complex                       |
| **Shows Dependencies** | Poorly                            | Somewhat                          | Excellently                   |
| **Shows Timeline**     | Text only                         | Visual bars                       | No calendar                   |
| **Critical Path**      | Not visible                       | Not clear                         | Very clear                    |
| **Best For**           | Small projects, detailed tracking | Presentations, progress reporting | Scheduling analysis, planning |
| **Audience**           | Team members                      | Stakeholders, management          | Project planners, technical   |

---

## 📌 Activity Node Structure

> 🟡 **Tier B** | Frequency: 2/4 | Section: A

### Definition

In **Activity-on-Node (AON)** networks, each activity is represented as a rectangular node containing scheduling information.

### Standard Activity Node Format

```
┌─────────────────────────────────┐
│  Activity ID / Activity Name    │
├────────────┬────────────────────┤
│    EST     │       EFT          │
│            │                    │
├────────────┼────────────────────┤
│  Duration  │                    │
│            │                    │
├────────────┼────────────────────┤
│    LST     │       LFT          │
│            │                    │
├────────────┴────────────────────┤
│        Total Float (TF)         │
└─────────────────────────────────┘
```

### Node Components

**1. Activity Identification**

- **Activity ID:** Unique identifier (A, B, C or T1, T2)
- **Activity Name:** Descriptive label (Requirements Gathering, Database Design)

**2. Time Values**

- **EST (Earliest Start Time):** Earliest an activity can begin (from forward pass)
- **EFT (Earliest Finish Time):** EST + Duration
- **LST (Latest Start Time):** Latest an activity can start without delaying project (from backward pass)
- **LFT (Latest Finish Time):** LST + Duration
- **Duration:** Time to complete activity (days, weeks)

**3. Float (Slack)**

- **Total Float:** TF = LST - EST = LFT - EFT
- **Meaning:** How much activity can be delayed without delaying project
- **Critical Activity:** TF = 0 (no flexibility)

### Example Activity Node

```
┌─────────────────────────────────┐
│     A - Requirements            │
├────────────┬────────────────────┤
│   EST: 0   │    EFT: 10         │
│            │                    │
├────────────┼────────────────────┤
│ Duration:  │                    │
│  10 days   │                    │
├────────────┼────────────────────┤
│  LST: 0    │    LFT: 10         │
│            │                    │
├────────────┴────────────────────┤
│   Total Float: 0 (Critical)     │
└─────────────────────────────────┘
```

**Interpretation:**

- Activity A must start on day 0 (EST = LST = 0)
- Takes 10 days
- Must finish by day 10
- Zero float → Critical activity
- Any delay delays entire project

![Activity Node Structure](diagrams/activity_node_structure.svg)

---

## 📌 Critical Path Method (CPM)

> 🔴 **Tier A** | Frequency: 4/4 | Section: C (Always appears!)

### Definition

**CPM** is a network analysis technique to determine the longest path through a project network, identifying activities that cannot be delayed without delaying the entire project.

### Key Concepts

**1. Critical Path**

- Longest sequence of activities from start to finish
- Determines minimum project duration
- Activities with zero float/slack
- Any delay on critical path delays project

**2. Float/Slack**

- **Total Float:** Maximum delay without delaying project
- **Free Float:** Delay without delaying successors
- **Critical Activities:** Float = 0
- **Non-Critical:** Float > 0

**3. Dependencies**

- **Finish-to-Start (FS):** Activity B starts after A finishes (most common)
- **Start-to-Start (SS):** B starts when A starts
- **Finish-to-Finish (FF):** B finishes when A finishes
- **Start-to-Finish (SF):** B finishes when A starts (rare)

### CPM Process (Step-by-Step)

**Step 1: List All Activities**

- Identify every task in project
- Assign unique ID to each
- Determine duration for each
- Identify predecessors (what must finish before this starts)

**Example:**

| Activity | Description      | Duration (weeks) | Predecessors |
| -------- | ---------------- | ---------------- | ------------ |
| A        | Requirements     | 6                | -            |
| B        | System Design    | 4                | -            |
| C        | Install Hardware | 3                | A            |
| D        | Data Migration   | 4                | B            |
| E        | Draft Procedures | 4                | B            |
| F        | Recruit Staff    | 12               | -            |
| G        | User Training    | 5                | E, F         |
| H        | Install & Test   | 3                | C, D         |

**Step 2: Draw Network Diagram**

- Use Activity-on-Node (AON) convention
- Each activity = box/node
- Arrows show dependencies (precedence)
- Start node → Activities → End node

**Network for Above Example:**

```
       A(6)                C(3)
Start ──────→ ┌──────────→ ──────→ ┐
              │                     │
              │                     ├──→ H(3) ──→ End
       B(4)   │            D(4)     │
      ──────→ ┼──────────→ ────────→┘
              │
              │            E(4)
              └──────────→ ──────→ ┐
                                   │
       F(12)                       ├──→ G(5) ──→ End
      ─────────────────────────────┘
```

**Step 3: Forward Pass (Calculate EST and EFT)**

**Rules:**

- **Start activity:** EST = 0
- **EFT = EST + Duration**
- **If activity has multiple predecessors:** EST = Maximum EFT of all predecessors

**Calculation for Example:**

| Activity | Duration | Predecessors | EST             | EFT             |
| -------- | -------- | ------------ | --------------- | --------------- |
| A        | 6        | -            | 0               | 0 + 6 = **6**   |
| B        | 4        | -            | 0               | 0 + 4 = **4**   |
| F        | 12       | -            | 0               | 0 + 12 = **12** |
| C        | 3        | A            | 6               | 6 + 3 = **9**   |
| D        | 4        | B            | 4               | 4 + 4 = **8**   |
| E        | 4        | B            | 4               | 4 + 4 = **8**   |
| G        | 5        | E, F         | max(8, 12) = 12 | 12 + 5 = **17** |
| H        | 3        | C, D         | max(9, 8) = 9   | 9 + 3 = **12**  |

**Project Duration = Maximum EFT = max(17, 12) = 17 weeks**

**Step 4: Backward Pass (Calculate LST and LFT)**

**Rules:**

- **End activity:** LFT = Project Duration (from forward pass)
- **LST = LFT - Duration**
- **If activity has multiple successors:** LFT = Minimum LST of all successors

**Calculation (working backwards):**

| Activity | Duration | Successors | LFT            | LST             |
| -------- | -------- | ---------- | -------------- | --------------- |
| G        | 5        | -          | 17             | 17 - 5 = **12** |
| H        | 3        | -          | 17             | 17 - 3 = **14** |
| E        | 4        | G          | 12             | 12 - 4 = **8**  |
| F        | 12       | G          | 12             | 12 - 12 = **0** |
| C        | 3        | H          | 14             | 14 - 3 = **11** |
| D        | 4        | H          | 14             | 14 - 4 = **10** |
| A        | 6        | C          | 11             | 11 - 6 = **5**  |
| B        | 4        | D, E       | min(10, 8) = 8 | 8 - 4 = **4**   |

**Step 5: Calculate Total Float**

**Formula:** TF = LST - EST (or LFT - EFT)

| Activity | EST | LST | EFT | LFT | TF = LST - EST    |
| -------- | --- | --- | --- | --- | ----------------- |
| A        | 0   | 5   | 6   | 11  | 5 - 0 = **5**     |
| B        | 0   | 4   | 4   | 8   | 4 - 0 = **4**     |
| C        | 6   | 11  | 9   | 14  | 11 - 6 = **5**    |
| D        | 4   | 10  | 8   | 14  | 10 - 4 = **6**    |
| E        | 4   | 8   | 8   | 12  | 8 - 4 = **4**     |
| F        | 0   | 0   | 12  | 12  | 0 - 0 = **0** ✓   |
| G        | 12  | 12  | 17  | 17  | 12 - 12 = **0** ✓ |
| H        | 9   | 14  | 12  | 17  | 14 - 9 = **5**    |

**Step 6: Identify Critical Path**

**Critical Activities:** All activities with TF = 0

- **F** (Recruit Staff): 12 weeks, TF = 0
- **G** (User Training): 5 weeks, TF = 0

**Critical Path:** Start → **F → G** → End

**Total Critical Path Duration:** 12 + 5 = **17 weeks**

**Interpretation:**

- Project will take minimum **17 weeks**
- Activities F and G are critical (cannot be delayed)
- All other activities have slack/float (can be delayed without impacting project)
- Focus management attention on F and G

### CPM Benefits

**1. Project Duration**

- Determines minimum completion time
- Sets realistic deadline

**2. Critical Activity Identification**

- Shows where delays are unacceptable
- Prioritize resources and management attention

**3. Float Calculation**

- Identifies scheduling flexibility
- Helps resource leveling

**4. What-If Analysis**

- "What if activity D takes 6 weeks instead of 4?"
- "Can we crash the schedule by adding resources to F?"

**5. Progress Monitoring**

- Track critical activities closely
- Alert if critical path changes

### Crashing the Schedule

**Definition:** Reducing project duration by adding resources to critical activities.

**Process:**

1. Identify critical path
2. Find critical activity with lowest crash cost
3. Add resources to reduce duration
4. Recalculate CPM
5. Check if critical path changed
6. Repeat until target date or budget exhausted

**Example:**

- Critical path: F(12) → G(5) = 17 weeks
- Target: 15 weeks (need to save 2 weeks)
- Crash F by hiring 2 more recruiters: F becomes 10 weeks (cost: $5,000)
- New critical path: F(10) → G(5) = 15 weeks ✓

![CPM Network](diagrams/cpm_network.svg)

---

## 📌 Forward Pass & Backward Pass Techniques

> 🔴 **Tier A** | Frequency: 3/4 | Section: C

### Forward Pass (Calculate EST and EFT)

**Purpose:** Determine earliest times activities can start and finish

**Starting Point:**

- Begin at project start
- Set EST of all starting activities = 0

**Rules:**

**1. For activities with NO predecessors:**

```
EST = 0
EFT = EST + Duration
```

**2. For activities with ONE predecessor:**

```
EST = EFT of predecessor
EFT = EST + Duration
```

**3. For activities with MULTIPLE predecessors:**

```
EST = MAXIMUM of all predecessors' EFT
EFT = EST + Duration
```

**Example:**

```
Activity A: Duration = 5 days
  - No predecessor
  - EST = 0
  - EFT = 0 + 5 = 5

Activity B: Duration = 3 days
  - Predecessor: A
  - EST = 5 (EFT of A)
  - EFT = 5 + 3 = 8

Activity C: Duration = 4 days
  - Predecessors: A (EFT=5) and B (EFT=8)
  - EST = max(5, 8) = 8
  - EFT = 8 + 4 = 12
```

**Project Duration = Maximum EFT of all activities**

### Backward Pass (Calculate LST and LFT)

**Purpose:** Determine latest times activities can start and finish without delaying project

**Starting Point:**

- Begin at project end
- Set LFT of all ending activities = Project Duration (from forward pass)

**Rules:**

**1. For activities with NO successors:**

```
LFT = Project Duration
LST = LFT - Duration
```

**2. For activities with ONE successor:**

```
LFT = LST of successor
LST = LFT - Duration
```

**3. For activities with MULTIPLE successors:**

```
LFT = MINIMUM of all successors' LST
LST = LFT - Duration
```

**Example (working backwards from previous):**

```
Activity C: Duration = 4 days
  - No successor
  - LFT = 12 (Project Duration)
  - LST = 12 - 4 = 8

Activity B: Duration = 3 days
  - Successor: C
  - LFT = 8 (LST of C)
  - LST = 8 - 3 = 5

Activity A: Duration = 5 days
  - Successors: B (LST=5) and C (LST=8)
  - LFT = min(5, 8) = 5
  - LST = 5 - 5 = 0
```

### Complete Example with Both Passes

**Given:**

| Activity | Duration | Predecessors |
| -------- | -------- | ------------ |
| A        | 8        | -            |
| B        | 5        | -            |
| C        | 3        | A            |
| D        | 4        | B            |
| E        | 3        | B            |
| F        | 10       | -            |
| G        | 3        | E, F         |
| H        | 2        | C, D         |

**Forward Pass:**

| Activity | Duration | Predecessors | EST          | EFT |
| -------- | -------- | ------------ | ------------ | --- |
| A        | 8        | -            | 0            | 8   |
| B        | 5        | -            | 0            | 5   |
| F        | 10       | -            | 0            | 10  |
| C        | 3        | A            | 8            | 11  |
| D        | 4        | B            | 5            | 9   |
| E        | 3        | B            | 5            | 8   |
| G        | 3        | E, F         | max(8,10)=10 | 13  |
| H        | 2        | C, D         | max(11,9)=11 | 13  |

**Project Duration = 13 weeks**

**Backward Pass:**

| Activity | Successors | LFT        | LST |
| -------- | ---------- | ---------- | --- |
| G        | -          | 13         | 10  |
| H        | -          | 13         | 11  |
| E        | G          | 10         | 7   |
| F        | G          | 10         | 0   |
| C        | H          | 11         | 8   |
| D        | H          | 11         | 7   |
| B        | D, E       | min(7,7)=7 | 2   |
| A        | C          | 8          | 0   |

**Float Calculation:**

| Activity | EST | LST | TF = LST-EST | Critical? |
| -------- | --- | --- | ------------ | --------- |
| A        | 0   | 0   | 0            | ✓ Yes     |
| B        | 0   | 2   | 2            | No        |
| C        | 8   | 8   | 0            | ✓ Yes     |
| D        | 5   | 7   | 2            | No        |
| E        | 5   | 7   | 2            | No        |
| F        | 0   | 0   | 0            | ✓ Yes     |
| G        | 10  | 10  | 0            | ✓ Yes     |
| H        | 11  | 11  | 0            | ✓ Yes     |

**Critical Path: A → C → H** and **F → G** (parallel critical paths)
**Duration: 13 weeks**

![Forward Backward Pass](diagrams/forward_backward_pass.svg)

---

## 📌 PERT Technique

> 🔴 **Tier A** | Frequency: 3/4 | Section: B + C

### Definition

**PERT (Program Evaluation and Review Technique)** is a probabilistic network analysis method used when activity durations are uncertain, using three time estimates.

### Key Difference: CPM vs PERT

| **Aspect**      | **CPM**                              | **PERT**                                               |
| --------------- | ------------------------------------ | ------------------------------------------------------ |
| **Duration**    | Single deterministic value           | Three estimates (optimistic, most likely, pessimistic) |
| **Nature**      | Deterministic                        | Probabilistic                                          |
| **Focus**       | Cost and time trade-off              | Time only                                              |
| **Best For**    | Well-defined projects (construction) | Research, new products, high uncertainty               |
| **Uncertainty** | Not considered                       | Explicitly accounted for                               |

### Three Time Estimates

**1. Optimistic Time (O or a)**

- Best-case scenario (everything goes perfectly)
- Probability ≈ 1% (very rare)
- Example: "If nothing goes wrong, we can finish in 3 days"

**2. Most Likely Time (M or m)**

- Realistic estimate based on normal conditions
- Mode of distribution (most frequent outcome)
- Example: "Normally takes 5 days"

**3. Pessimistic Time (P or b)**

- Worst-case scenario (everything goes wrong)
- Probability ≈ 1% (very rare)
- Example: "If we face all problems, could take 9 days"

### PERT Formulas

**1. Expected Time (TE or μ)**

```
TE = (O + 4M + P) / 6

Where:
- O = Optimistic time
- M = Most Likely time
- P = Pessimistic time
- 4M = Weighted heavily because it's most probable
```

**2. Variance (V or σ²)**

```
Variance (V) = [(P - O) / 6]²

Measures uncertainty in estimate
Higher variance = more uncertainty
```

**3. Standard Deviation (SD or σ)**

```
SD = √Variance = (P - O) / 6

Measures spread of possible durations
```

**4. Project Variance**

```
Project Variance = Σ Variances of critical path activities only
(Not all activities, only those on critical path)
```

**5. Project Standard Deviation**

```
Project SD = √(Project Variance)
```

**6. Probability of Completion**

```
Z = (Target Date - Expected Project Duration) / Project SD

Then use standard normal table to find probability
```

### PERT Process (Step-by-Step)

**Step 1: Gather Three Estimates for Each Activity**

**Example Project:**

| Activity | Optimistic (O) | Most Likely (M) | Pessimistic (P) | Predecessors |
| -------- | -------------- | --------------- | --------------- | ------------ |
| A        | 2              | 4               | 6               | -            |
| B        | 3              | 5               | 7               | -            |
| C        | 1              | 2               | 3               | A            |
| D        | 4              | 6               | 8               | A, B         |
| E        | 2              | 3               | 10              | C            |
| F        | 3              | 4               | 5               | D, E         |

**Step 2: Calculate Expected Time (TE) for Each Activity**

```
Activity A: TE = (2 + 4×4 + 6) / 6 = (2 + 16 + 6) / 6 = 24/6 = 4 weeks

Activity B: TE = (3 + 4×5 + 7) / 6 = (3 + 20 + 7) / 6 = 30/6 = 5 weeks

Activity C: TE = (1 + 4×2 + 3) / 6 = (1 + 8 + 3) / 6 = 12/6 = 2 weeks

Activity D: TE = (4 + 4×6 + 8) / 6 = (4 + 24 + 8) / 6 = 36/6 = 6 weeks

Activity E: TE = (2 + 4×3 + 10) / 6 = (2 + 12 + 10) / 6 = 24/6 = 4 weeks

Activity F: TE = (3 + 4×4 + 5) / 6 = (3 + 16 + 5) / 6 = 24/6 = 4 weeks
```

**Summary Table:**

| Activity | O   | M   | P   | TE  | Variance = [(P-O)/6]²       |
| -------- | --- | --- | --- | --- | --------------------------- |
| A        | 2   | 4   | 6   | 4   | [(6-2)/6]² = (4/6)² = 0.44  |
| B        | 3   | 5   | 7   | 5   | [(7-3)/6]² = (4/6)² = 0.44  |
| C        | 1   | 2   | 3   | 2   | [(3-1)/6]² = (2/6)² = 0.11  |
| D        | 4   | 6   | 8   | 6   | [(8-4)/6]² = (4/6)² = 0.44  |
| E        | 2   | 3   | 10  | 4   | [(10-2)/6]² = (8/6)² = 1.78 |
| F        | 3   | 4   | 5   | 4   | [(5-3)/6]² = (2/6)² = 0.11  |

**Step 3: Draw Network and Perform CPM with TE Values**

Use TE as activity durations and perform forward/backward pass:

**Forward Pass:**

- A: EST=0, EFT=4
- B: EST=0, EFT=5
- C: EST=4, EFT=6
- D: EST=max(4,5)=5, EFT=11
- E: EST=6, EFT=10
- F: EST=max(11,10)=11, EFT=15

**Project Expected Duration = 15 weeks**

**Backward Pass:**

- F: LFT=15, LST=11
- E: LFT=11, LST=7
- D: LFT=11, LST=5
- C: LFT=7, LST=5
- B: LFT=5, LST=0
- A: LFT=min(5,5)=5, LST=1

**Float Calculation:**

| Activity | EST | LST | Float |
| -------- | --- | --- | ----- |
| A        | 0   | 1   | 1     |
| B        | 0   | 0   | 0 ✓   |
| C        | 4   | 5   | 1     |
| D        | 5   | 5   | 0 ✓   |
| E        | 6   | 7   | 1     |
| F        | 11  | 11  | 0 ✓   |

**Critical Path: B → D → F**
**Critical Path Duration: 5 + 6 + 4 = 15 weeks**

**Step 4: Calculate Project Variance (Critical Path Only)**

```
Project Variance = Variance(B) + Variance(D) + Variance(F)
                 = 0.44 + 0.44 + 0.11
                 = 0.99

Project Standard Deviation = √0.99 = 0.995 ≈ 1 week
```

**Step 5: Probability Analysis**

**Question:** What is probability of completing project in 16 weeks?

```
Z = (Target - Expected) / SD
  = (16 - 15) / 1
  = 1

From standard normal table: P(Z ≤ 1) = 0.8413 = 84.13%
```

**Interpretation:** 84% probability of finishing within 16 weeks

**Question:** What is probability of completing in 13 weeks?

```
Z = (13 - 15) / 1 = -2

From table: P(Z ≤ -2) = 0.0228 = 2.28%
```

**Interpretation:** Only 2.28% chance of finishing in 13 weeks (very unlikely)

### PERT Benefits

**1. Handles Uncertainty**

- Acknowledges that estimates are uncertain
- Provides probability of meeting deadlines
- More realistic than single-point estimates

**2. Risk Assessment**

- High variance activities = high risk
- Focus on reducing uncertainty in critical activities
- Example: Activity E has variance 1.78 (highest) → needs attention

**3. Better Decision Making**

- "What's probability of finishing by contract date?"
- "Should we commit to this deadline?"
- Data-driven risk discussions

**4. Resource Planning**

- Identify activities with high uncertainty
- Plan contingencies
- Allocate buffer time appropriately

### PERT Limitations

**1. Assumes Beta Distribution**

- Real distributions may differ
- Three estimates may not be accurate

**2. Independence Assumption**

- Assumes activity durations are independent
- In reality, one delay may cause others

**3. Estimation Difficulty**

- Hard to estimate optimistic and pessimistic accurately
- Tendency to be overly optimistic

**4. Focus on Time Only**

- Doesn't consider cost
- CPM better for cost-time trade-offs

---

## 📌 Risk Management

> 🔴 **Tier A** | Frequency: 4/4 | Section: A + B + C

### Definition

**Risk Management** is the systematic process of identifying, assessing, prioritizing, and mitigating risks to minimize their impact on project objectives.

### Risk vs Issue vs Problem

**Risk:**

- Uncertain future event
- May or may not happen
- "If X occurs, then Y impact"
- Example: "Key developer might leave"

**Issue:**

- Risk that has occurred
- Happening now
- Requires immediate action
- Example: "Database server crashed"

**Problem:**

- Issue that hasn't been resolved
- Negative impact already occurring
- Example: "Team morale low due to crunch mode for 2 months"

### Risk Categories

**1. Technical Risk**

- Technology unproven or new
- Integration challenges
- Performance issues
- Skill gaps in team
- Example: "Using new AI framework with limited documentation"

**2. Schedule Risk**

- Unrealistic deadlines
- Dependencies on external parties
- Underestimated effort
- Example: "Third-party API delivery delayed"

**3. Cost Risk**

- Budget overruns
- Currency fluctuations
- Vendor price increases
- Example: "Cloud hosting costs 50% higher than estimated"

**4. Resource Risk**

- Key person dependency
- Attrition
- Resource unavailability
- Competing priorities
- Example: "Only one person knows legacy system"

**5. Organizational Risk**

- Funding cuts
- Priority changes
- Management turnover
- Merger/acquisition
- Example: "New CTO wants different technology stack"

**6. External Risk**

- Regulatory changes
- Market shifts
- Natural disasters
- Vendor bankruptcy
- Example: "GDPR-like regulation introduced mid-project"

### Risk Management Process

**Phase 1: Risk Identification**

**Techniques:**

**1. Brainstorming Sessions**

- Gather team, stakeholders
- Generate risk list freely
- No filtering in this phase
- Document all ideas

**2. Checklist-Based**

- Use standard risk categories
- Review past project risks
- Industry-specific checklists
- Example: "Have we considered database scalability?"

**3. SWOT Analysis**

- Strengths, Weaknesses (internal)
- Opportunities, Threats (external risks)

**4. Expert Interviews**

- Consult experienced people
- Domain experts
- Lessons from similar projects

**5. Assumption Analysis**

- Review all project assumptions
- "What if this assumption is wrong?"
- Example: Assume "Users have broadband" → Risk: "What if rural users have slow connections?"

**6. Document Review**

- Analyze requirements, contracts, specs
- Look for ambiguities, conflicts
- Example: "Requirement says 'fast response' but no specific SLA"

**Risk Register Template:**

| Risk ID | Risk Description         | Category  | Probability | Impact | Priority | Owner     |
| ------- | ------------------------ | --------- | ----------- | ------ | -------- | --------- |
| R001    | Key developer may leave  | Resource  | Medium      | High   | High     | PM        |
| R002    | Third-party API unstable | Technical | High        | Medium | High     | Tech Lead |

**Phase 2: Risk Assessment**

**Qualitative Assessment:**

**Probability Scale:**

- Very Low: 0-10%
- Low: 10-30%
- Medium: 30-50%
- High: 50-70%
- Very High: 70-100%

**Impact Scale (on project objectives):**

- **Very Low:** < 5% deviation in cost/schedule
- **Low:** 5-10%
- **Medium:** 10-20%
- **High:** 20-40%
- **Critical:** > 40%

**Probability-Impact Matrix:**

|               | Very Low | Low  | Medium | High | Critical |
| ------------- | -------- | ---- | ------ | ---- | -------- |
| **Very High** | Med      | Med  | High   | High | Critical |
| **High**      | Low      | Med  | Med    | High | High     |
| **Medium**    | Low      | Low  | Med    | Med  | High     |
| **Low**       | VLow     | Low  | Low    | Med  | Med      |
| **Very Low**  | VLow     | VLow | Low    | Low  | Med      |

**Risk Score = Probability × Impact**

**Example:**

- Risk: Senior developer leaves
- Probability: Medium (40%)
- Impact: High (30% schedule delay)
- Risk Score: 0.40 × 30% = 12% (High priority)

**Quantitative Assessment:**

**Expected Monetary Value (EMV):**

```
EMV = Probability × Financial Impact

Example:
- Risk: Server failure during peak season
- Probability: 20%
- Impact: $100,000 lost revenue
- EMV = 0.20 × $100,000 = $20,000
```

**Phase 3: Risk Planning (Response Strategies)**

**1. Avoid (Eliminate the risk)**

- Change plan to eliminate risk entirely
- Example: Risk = "Unproven technology may fail"
  - **Avoidance:** Use mature, proven technology instead

**2. Mitigate (Reduce probability or impact)**

- Take actions to lower likelihood or severity
- Example: Risk = "Developer may leave"
  - **Mitigation:** Cross-train team, document knowledge, improve retention

**3. Transfer (Shift risk to third party)**

- Insurance, warranties, contracts
- Example: Risk = "Hardware failure"
  - **Transfer:** Buy insurance, use vendor SLA

**4. Accept (Do nothing, but acknowledge)**

- For low-priority risks
- Passive acceptance: No action
- Active acceptance: Set aside contingency budget
- Example: Risk = "Minor UI bug in rare scenario"
  - **Acceptance:** Fix in future release if users complain

**5. Exploit (For positive risks/opportunities)**

- Ensure opportunity happens
- Example: "New team member is expert in required skill"
  - **Exploit:** Assign them to critical tasks

**Risk Response Plan Example:**

| Risk                 | Strategy            | Actions                                                      | Owner     | Budget     | Timeline |
| -------------------- | ------------------- | ------------------------------------------------------------ | --------- | ---------- | -------- |
| Developer leaves     | Mitigate            | 1. Document code<br>2. Pair programming<br>3. Cross-training | PM        | $5K        | Ongoing  |
| Third-party API down | Transfer + Mitigate | 1. SLA with vendor<br>2. Build fallback mechanism            | Tech Lead | $10K       | Sprint 2 |
| Requirement changes  | Accept              | 1. Set aside 15% contingency<br>2. Agile approach            | PM        | 15% budget | -        |

**Phase 4: Risk Monitoring and Control**

**Ongoing Activities:**

**1. Track Risk Status**

- Review risk register weekly
- Update probability/impact as new info emerges
- Close risks that are no longer relevant
- Add newly identified risks

**2. Monitor Risk Triggers**

- **Trigger:** Early warning sign risk is materializing
- Example:
  - Risk: "Developer leaves"
  - Triggers: Resume on job sites, increased sick days, declined new tasks

**3. Execute Response Plans**

- When risk occurs, implement planned response
- Example: Developer gives notice → Immediately start knowledge transfer

**4. Risk Audits**

- Periodic review of risk management effectiveness
- "Are we identifying risks early enough?"
- "Are our mitigation strategies working?"

**5. Update Stakeholders**

- Report top risks in status meetings
- Dashboard with risk trend (increasing/decreasing)
- Escalate critical risks to sponsors

### Risk Management Best Practices

**1. Make it Part of Culture**

- Encourage team to raise risks without fear
- Reward early risk identification
- "No surprises" culture

**2. Prioritize Ruthlessly**

- Focus on top 5-10 risks
- Don't waste time on trivial risks
- 80-20 rule: 20% of risks cause 80% of problems

**3. Assign Ownership**

- Every risk has an owner
- Owner monitors and executes mitigation
- Clear accountability

**4. Integrate with Planning**

- Risk mitigation tasks in project schedule
- Budget allocated for contingencies
- Not a separate activity

**5. Learn from Past**

- Review risks from previous projects
- Build organizational risk database
- Common risks get standard mitigation plans

---

## 🎯 PYQ MODEL ANSWERS

### 🎯 PYQ [2021-22] - "Briefly discuss about the need of Activity Planning" (Section A, 2 marks)

**Model Answer:**

Activity Planning is essential to: (1) Break project into manageable tasks, (2) Establish task dependencies and sequence, (3) Identify resource requirements and allocate them timely, (4) Determine realistic schedule and critical activities, (5) Provide baseline for monitoring progress, (6) Facilitate coordination among teams. Without activity planning, projects lack clear roadmap, leading to missed deadlines, resource conflicts, and cost overruns.

---

### 🎯 PYQ [2021-22] - "What do you mean by Risk Management?" (Section A, 2 marks)

**Model Answer:**

Risk Management is the systematic process of identifying, assessing, prioritizing, and mitigating project risks to minimize negative impact on objectives. It involves four phases: (1) Risk Identification - brainstorming potential risks, (2) Risk Assessment - evaluating probability and impact, (3) Risk Planning - developing mitigation strategies (avoid, mitigate, transfer, accept), (4) Risk Monitoring - tracking and controlling risks throughout project lifecycle.

---

### 🎯 PYQ [2021-22, 2022-23, 2023-24] - "Discuss about the Forward Pass and Backward Pass techniques in Activity Planning and Risk Management" (Section C, 10/7 marks)

**Model Answer:**

**Introduction:**

Forward Pass and Backward Pass are fundamental techniques in Critical Path Method (CPM) used to calculate earliest and latest times for project activities, enabling identification of critical path and project duration.

**Forward Pass Technique:**

**Purpose:**

- Calculate Earliest Start Time (EST) and Earliest Finish Time (EFT) for each activity
- Determine minimum project duration
- Work forward from project start to end

**Process:**

**Step 1: Start with Initial Activities**

- Activities with no predecessors
- Set EST = 0 for all starting activities

**Step 2: Calculate for Each Activity**

```
EFT = EST + Duration

For next activity:
- If one predecessor: EST = EFT of that predecessor
- If multiple predecessors: EST = MAXIMUM of all predecessors' EFT
```

**Example:**

| Activity | Duration | Predecessors | EST Calculation | EST | EFT |
| -------- | -------- | ------------ | --------------- | --- | --- |
| A        | 5        | -            | Start activity  | 0   | 5   |
| B        | 3        | -            | Start activity  | 0   | 3   |
| C        | 4        | A            | EFT of A        | 5   | 9   |
| D        | 6        | A, B         | max(5, 3) = 5   | 5   | 11  |
| E        | 2        | C, D         | max(9, 11) = 11 | 11  | 13  |

**Project Duration = Maximum EFT = 13 days**

**Backward Pass Technique:**

**Purpose:**

- Calculate Latest Start Time (LST) and Latest Finish Time (LFT) for each activity
- Determine schedule flexibility (float/slack)
- Work backward from project end to start

**Process:**

**Step 1: Start with Final Activities**

- Activities with no successors
- Set LFT = Project Duration (from forward pass)

**Step 2: Calculate for Each Activity**

```
LST = LFT - Duration

For previous activity:
- If one successor: LFT = LST of that successor
- If multiple successors: LFT = MINIMUM of all successors' LST
```

**Example (continuing from above):**

| Activity | Duration | Successors | LFT Calculation | LFT | LST |
| -------- | -------- | ---------- | --------------- | --- | --- |
| E        | 2        | -          | Project end     | 13  | 11  |
| D        | 6        | E          | LST of E = 11   | 11  | 5   |
| C        | 4        | E          | LST of E = 11   | 11  | 7   |
| B        | 3        | D          | LST of D = 5    | 5   | 2   |
| A        | 5        | C, D       | min(7, 5) = 5   | 5   | 0   |

**Float Calculation and Critical Path:**

**Total Float Formula:**

```
Total Float = LST - EST (or LFT - EFT)
```

**Complete Analysis:**

| Activity | EST | LST | EFT | LFT | Total Float | Critical? |
| -------- | --- | --- | --- | --- | ----------- | --------- |
| A        | 0   | 0   | 5   | 5   | 0           | ✓ Yes     |
| B        | 0   | 2   | 3   | 5   | 2           | No        |
| C        | 5   | 7   | 9   | 11  | 2           | No        |
| D        | 5   | 5   | 11  | 11  | 0           | ✓ Yes     |
| E        | 11  | 11  | 13  | 13  | 0           | ✓ Yes     |

**Critical Path: A → D → E (all activities with float = 0)**
**Critical Path Duration: 5 + 6 + 2 = 13 days**

**Interpretation:**

**Critical Activities (A, D, E):**

- Zero float/slack
- Must start and finish on calculated dates
- Any delay delays entire project
- Require close monitoring
- Priority for resource allocation

**Non-Critical Activities (B, C):**

- Have float (scheduling flexibility)
- Activity B can be delayed up to 2 days without impacting project
- Activity C can be delayed up to 2 days
- Can be used for resource leveling
- Lower priority monitoring

**Practical Application in Risk Management:**

**1. Identify High-Risk Activities:**

- Critical activities are high-risk (zero tolerance for delay)
- Focus risk mitigation on critical path
- Example: If Activity D is complex, allocate best resources, add buffers

**2. Resource Optimization:**

- Use float in non-critical activities to smooth resource demand
- Example: If all activities need same specialist, delay Activity B by 2 days to avoid conflict

**3. What-If Analysis:**

- "What if Activity D takes 8 days instead of 6?"
  - Project duration becomes 15 days (2-day delay)
  - Activity C might become critical

**4. Schedule Compression:**

- To reduce project duration, compress critical activities only
- Crashing non-critical activities (B, C) won't help
- Example: Add resources to Activity D to reduce it to 4 days → Project becomes 11 days

**5. Progress Monitoring:**

- Track critical activities daily
- Non-critical activities can be tracked weekly
- Alert management if critical activity slips

**Complete Worked Example:**

**Given Project:**

| Activity | Duration (weeks) | Predecessors |
| -------- | ---------------- | ------------ |
| A        | 6                | -            |
| B        | 4                | -            |
| C        | 3                | A            |
| D        | 4                | B            |
| E        | 3                | B            |
| F        | 10               | -            |
| G        | 3                | E, F         |
| H        | 2                | C, D         |

**Forward Pass:**

- A: EST=0, EFT=6
- B: EST=0, EFT=4
- F: EST=0, EFT=10
- C: EST=6, EFT=9
- D: EST=4, EFT=8
- E: EST=4, EFT=7
- G: EST=max(7,10)=10, EFT=13
- H: EST=max(9,8)=9, EFT=11

**Project Duration = 13 weeks**

**Backward Pass:**

- G: LFT=13, LST=10
- H: LFT=13, LST=11
- E: LFT=10, LST=7
- F: LFT=10, LST=0
- C: LFT=11, LST=8
- D: LFT=11, LST=7
- B: LFT=min(7,7)=7, LST=3
- A: LFT=8, LST=2

**Float and Critical Path:**

| Activity | EST | LST | Float | Critical? |
| -------- | --- | --- | ----- | --------- |
| A        | 0   | 2   | 2     | No        |
| B        | 0   | 3   | 3     | No        |
| C        | 6   | 8   | 2     | No        |
| D        | 4   | 7   | 3     | No        |
| E        | 4   | 7   | 3     | No        |
| F        | 0   | 0   | 0     | ✓ Yes     |
| G        | 10  | 10  | 0     | ✓ Yes     |
| H        | 9   | 11  | 2     | No        |

**Critical Path: F → G**
**Duration: 10 + 3 = 13 weeks**

**Risk Management Insights:**

- Activities F (Recruit Staff, 10 weeks) and G (Training, 3 weeks) are critical
- **Risk:** If recruitment delayed, entire project delayed
- **Mitigation:** Start recruitment immediately, have backup recruitment agencies
- All other activities have float (2-3 weeks flexibility)
- Can delay activities A, B, C, D, E slightly to optimize resource usage

**Conclusion:**

Forward and Backward Pass techniques are essential CPM tools that enable project managers to:

- Determine realistic project duration
- Identify critical activities requiring close attention
- Calculate schedule flexibility for resource optimization
- Assess impact of delays or changes
- Make data-driven decisions on resource allocation and risk mitigation

These techniques form the foundation of effective project scheduling and control, enabling proactive management rather than reactive firefighting.

---

### 🎯 PYQ [2022-23] - "What do you mean by Project schedules? Mention the Objectives of Activity planning" (Section B, 10 marks)

**Model Answer:**

**Part 1: Project Schedules**

**Definition:**
Project Schedule is a detailed timetable showing when project activities will start and finish, considering task dependencies, resource availability, duration estimates, and constraints. It serves as roadmap for execution and baseline for monitoring progress.

**Components of Project Schedule:**

**1. Activities/Tasks:**

- Work packages from Work Breakdown Structure (WBS)
- Granular level (days or weeks)
- Example: "Design database schema", "Develop login module"

**2. Dependencies:**

- Predecessor-successor relationships
- Types: Finish-to-Start (most common), Start-to-Start, Finish-to-Finish
- Example: "Testing" cannot start before "Development" finishes

**3. Durations:**

- Estimated time for each activity
- Based on historical data, expert judgment, parametric models
- Example: "Database design: 5 days"

**4. Milestones:**

- Key events with zero duration
- Decision points, deliverables, phase completions
- Example: "Requirements Approved", "System Go-Live"

**5. Resource Assignments:**

- Who is responsible for each task
- Resource calendar (availability, holidays)
- Example: "John (Senior Dev): Login module"

**6. Constraints:**

- Fixed dates (must start/finish on specific date)
- External dependencies (vendor delivery, regulatory approval)
- Example: "Launch must be before Q4 holiday season"

**Three Forms of Presenting Project Schedule:**

**Form 1: Activity List (Tabular)**

- Spreadsheet with columns: Task ID, Name, Duration, Start, End, Predecessors, Resources
- **Advantages:** Easy to create, shows all details
- **Disadvantages:** Hard to visualize, doesn't show dependencies clearly
- **Best For:** Detailed tracking, small projects

**Form 2: Gantt Chart (Bar Chart)**

- Horizontal bars representing task duration on timeline
- X-axis: Time, Y-axis: Tasks
- Can show dependencies with arrows
- **Advantages:** Visual, easy to understand, shows timeline clearly, good for presentations
- **Disadvantages:** Doesn't emphasize critical path, complex for large projects
- **Best For:** Stakeholder communication, progress reporting

**Form 3: Network Diagram (CPM/PERT)**

- Boxes (activities) connected by arrows (dependencies)
- Shows critical path clearly
- **Advantages:** Reveals task interdependencies, identifies critical path, best for analysis
- **Disadvantages:** Complex to draw, not intuitive for non-technical stakeholders
- **Best For:** Project planning, schedule optimization, what-if analysis

**Schedule Development Process:**

**1. Define Activities:** Break down WBS into tasks
**2. Sequence Activities:** Identify dependencies
**3. Estimate Durations:** Use historical data, expert judgment
**4. Develop Schedule:** Use CPM/PERT to calculate dates
**5. Optimize:** Resource leveling, compression if needed
**6. Baseline:** Freeze schedule for tracking

**Part 2: Objectives of Activity Planning**

Activity Planning is critical for project success. Key objectives include:

**Objective 1: Assess Project Feasibility**

- **What:** Determine if project can be completed within constraints
- **How:** Calculate critical path, check if deadline achievable
- **Benefit:** Avoid committing to impossible deadlines
- **Example:** CPM shows 8-month duration, but contract requires 6 months → Negotiate or scope reduction

**Objective 2: Resource Planning and Allocation**

- **What:** Identify when and how many resources needed
- **How:** Map resource requirements to timeline
- **Benefit:** Timely hiring, training, procurement; avoid conflicts
- **Example:** "Need 3 Java developers in Sprint 3, but only have 2 → Hire/train now"

**Objective 3: Establish Realistic Schedule**

- **What:** Create achievable timeline based on data
- **How:** Use estimation techniques, consider dependencies
- **Benefit:** Set stakeholder expectations correctly
- **Example:** Bottom-up estimation shows 40 weeks, not 30 weeks as hoped

**Objective 4: Identify Critical Activities**

- **What:** Find tasks that cannot be delayed without delaying project
- **How:** Calculate critical path using CPM
- **Benefit:** Focus management attention and resources on critical tasks
- **Example:** "Database migration is on critical path → Allocate best DBA, monitor daily"

**Objective 5: Determine Schedule Flexibility (Float)**

- **What:** Identify activities with slack/buffer time
- **How:** Calculate total float for each activity
- **Benefit:** Optimize resource usage, handle unexpected delays
- **Example:** "UI design has 2 weeks float → Can delay if critical tasks need those designers"

**Objective 6: Facilitate Coordination and Communication**

- **What:** Provide common reference for all stakeholders
- **How:** Share schedule in appropriate format (Gantt for executives, network for team)
- **Benefit:** Everyone knows who does what when, reduces conflicts
- **Example:** "Frontend team knows backend API ready by Week 6 → Plan integration accordingly"

**Objective 7: Enable Progress Monitoring and Control**

- **What:** Create baseline to measure actual vs. planned performance
- **How:** Track task completion dates, compare with schedule
- **Benefit:** Early detection of slippages, timely corrective action
- **Example:** "Activity X should finish Tuesday, it's Wednesday and 60% done → Alert PM, reallocate resources"

**Objective 8: Support Risk Management**

- **What:** Identify schedule risks and plan mitigation
- **How:** Analyze dependencies, identify risky activities
- **Benefit:** Proactive risk handling, contingency planning
- **Example:** "Activity depends on third-party → Risk: vendor delay → Mitigation: Have backup vendor"

**Objective 9: Optimize Resource Utilization**

- **What:** Balance resource demand across timeline
- **How:** Resource leveling using float in non-critical activities
- **Benefit:** Avoid resource conflicts, reduce overtime, steady workload
- **Example:** "5 activities need same DBA in Week 3 → Shift non-critical activities to Week 4"

**Objective 10: Enable What-If Analysis**

- **What:** Assess impact of changes or delays
- **How:** Recalculate schedule with new assumptions
- **Benefit:** Informed decision making on scope, resources, deadlines
- **Example:** "What if we add 2 more developers? → Recalculate: Project finishes 3 weeks earlier"

**Benefits of Effective Activity Planning:**

**Business Benefits:**

- Realistic commitments to customers
- Better cash flow management (know when expenses occur)
- Competitive advantage (faster, more predictable delivery)

**Management Benefits:**

- Data-driven decisions
- Early warning of problems
- Clear priorities

**Team Benefits:**

- Clear expectations
- Reduced chaos and firefighting
- Visible progress and achievements

**Conclusion:**

Project schedules are the roadmap for project execution, providing timeline, dependencies, and resource assignments. Activity planning objectives ensure this roadmap is realistic, optimized, and actionable. Together, they enable proactive project management, transforming complex projects into manageable, trackable sets of activities with clear path to completion. Without robust scheduling and activity planning, projects are navigating without a map, leading to delays, cost overruns, and failure.

---

### 🎯 PYQ [2023-24, 2024-25] - "Formulate following Using CPM: (i) Construct the project network (ii) Perform Project Time estimation using forward and backward pass (iii) Identify the critical path" (Section C, 10/7 marks)

**Given Data (Standard Format):**

| Activity | Duration (weeks) | Precedents |
| -------- | ---------------- | ---------- |
| A        | 6                | -          |
| B        | 4                | -          |
| C        | 3                | A          |
| D        | 4                | B          |
| E        | 3                | B          |
| F        | 10               | -          |
| G        | 3                | E, F       |
| H        | 2                | C, D       |

**Model Answer:**

**(i) Construct Project Network Diagram:**

Using Activity-on-Node (AON) convention:

```
                    A(6)
                    ┌────┐
        Start ─────→│ A  │─────┐
          │         └────┘      │
          │                     ↓
          │         ┌────┐    ┌────┐    ┌────┐
          ├────────→│ B  │───→│ D  │───→│ H  │────→ End
          │         └────┘  ┌→└────┘    └────┘
          │          B(4)   │   D(4)      H(2)
          │                 │
          │                 │  ┌────┐    ┌────┐
          │                 └─→│ E  │───→│ G  │────→ End
          │                    └────┘  ┌→└────┘
          │                     E(3)   │  G(3)
          │                            │
          │         ┌────┐             │
          └────────→│ F  │─────────────┘
                    └────┘
                     F(10)

Legend:
- Boxes represent activities
- Arrows show dependencies (precedence)
- Numbers in parentheses are durations
```

**Network Explanation:**

- **Start Node:** Three parallel starting activities (A, B, F)
- **A → C → H path**
- **B → D → H path**
- **B → E → G path**
- **F → G path**
- **H and G converge to End**

**(ii) Perform Forward and Backward Pass:**

**FORWARD PASS (Calculate EST and EFT):**

**Rules:**

- EST of starting activities = 0
- EFT = EST + Duration
- For multiple predecessors: EST = max(EFT of all predecessors)

**Calculations:**

**Starting Activities (No Predecessors):**

```
Activity A: EST = 0, EFT = 0 + 6 = 6
Activity B: EST = 0, EFT = 0 + 4 = 4
Activity F: EST = 0, EFT = 0 + 10 = 10
```

**Dependent Activities:**

```
Activity C (Predecessor: A):
  EST = EFT of A = 6
  EFT = 6 + 3 = 9

Activity D (Predecessor: B):
  EST = EFT of B = 4
  EFT = 4 + 4 = 8

Activity E (Predecessor: B):
  EST = EFT of B = 4
  EFT = 4 + 3 = 7

Activity G (Predecessors: E, F):
  EST = max(EFT of E, EFT of F) = max(7, 10) = 10
  EFT = 10 + 3 = 13

Activity H (Predecessors: C, D):
  EST = max(EFT of C, EFT of D) = max(9, 8) = 9
  EFT = 9 + 2 = 11
```

**Forward Pass Summary:**

| Activity | Duration | Predecessors | EST | EFT |
| -------- | -------- | ------------ | --- | --- |
| A        | 6        | -            | 0   | 6   |
| B        | 4        | -            | 0   | 4   |
| F        | 10       | -            | 0   | 10  |
| C        | 3        | A            | 6   | 9   |
| D        | 4        | B            | 4   | 8   |
| E        | 3        | B            | 4   | 7   |
| G        | 3        | E, F         | 10  | 13  |
| H        | 2        | C, D         | 9   | 11  |

**Project Duration = max(EFT of G, EFT of H) = max(13, 11) = 13 weeks**

**BACKWARD PASS (Calculate LST and LFT):**

**Rules:**

- LFT of ending activities = Project Duration = 13
- LST = LFT - Duration
- For multiple successors: LFT = min(LST of all successors)

**Calculations (Working Backwards):**

**Ending Activities:**

```
Activity G: LFT = 13, LST = 13 - 3 = 10
Activity H: LFT = 13, LST = 13 - 2 = 11
```

**Working Backwards:**

```
Activity E (Successor: G):
  LFT = LST of G = 10
  LST = 10 - 3 = 7

Activity F (Successor: G):
  LFT = LST of G = 10
  LST = 10 - 10 = 0

Activity C (Successor: H):
  LFT = LST of H = 11
  LST = 11 - 3 = 8

Activity D (Successor: H):
  LFT = LST of H = 11
  LST = 11 - 4 = 7

Activity B (Successors: D, E):
  LFT = min(LST of D, LST of E) = min(7, 7) = 7
  LST = 7 - 4 = 3

Activity A (Successor: C):
  LFT = LST of C = 8
  LST = 8 - 6 = 2
```

**Backward Pass Summary:**

| Activity | Duration | Successors | LFT | LST |
| -------- | -------- | ---------- | --- | --- |
| G        | 3        | -          | 13  | 10  |
| H        | 2        | -          | 13  | 11  |
| E        | 3        | G          | 10  | 7   |
| F        | 10       | G          | 10  | 0   |
| C        | 3        | H          | 11  | 8   |
| D        | 4        | H          | 11  | 7   |
| B        | 4        | D, E       | 7   | 3   |
| A        | 6        | C          | 8   | 2   |

**Complete Schedule Table:**

| Activity | Duration | EST | EFT | LST | LFT | Total Float (LST - EST) |
| -------- | -------- | --- | --- | --- | --- | ----------------------- |
| A        | 6        | 0   | 6   | 2   | 8   | 2 - 0 = **2**           |
| B        | 4        | 0   | 4   | 3   | 7   | 3 - 0 = **3**           |
| C        | 3        | 6   | 9   | 8   | 11  | 8 - 6 = **2**           |
| D        | 4        | 4   | 8   | 7   | 11  | 7 - 4 = **3**           |
| E        | 3        | 4   | 7   | 7   | 10  | 7 - 4 = **3**           |
| F        | 10       | 0   | 10  | 0   | 10  | 0 - 0 = **0** ✓         |
| G        | 3        | 10  | 13  | 10  | 13  | 10 - 10 = **0** ✓       |
| H        | 2        | 9   | 11  | 11  | 13  | 11 - 9 = **2**          |

**(iii) Identify Critical Path:**

**Critical Activities:** All activities with Total Float = 0

- **Activity F:** Float = 0 ✓
- **Activity G:** Float = 0 ✓

**Critical Path: F → G**

**Critical Path Duration:**

```
F (10 weeks) + G (3 weeks) = 13 weeks
```

**Interpretation and Insights:**

**1. Project Duration:**

- Minimum completion time: **13 weeks**
- Determined by critical path F → G
- Any delay in F or G delays entire project

**2. Critical Activities (F, G):**

- **Activity F (Recruit Staff - 10 weeks):**
  - Must start on day 0, finish by week 10
  - Zero flexibility (EST = LST = 0)
  - Requires immediate attention
  - **Risk:** Recruitment delays are common → Mitigation: Start immediately, engage multiple agencies
- **Activity G (User Training - 3 weeks):**
  - Must start week 10, finish week 13
  - Cannot be delayed
  - Depends on completing F first
  - **Risk:** Staff unavailability for training → Mitigation: Book training rooms/trainers early

**3. Non-Critical Activities (A, B, C, D, E, H):**
All have float (scheduling flexibility):

- **Activity A (Requirements - 6 weeks):** 2 weeks float
  - Can start anytime between week 0 and week 2
  - Can finish between week 6 and week 8
  - Flexibility useful for resource leveling

- **Activity B (System Design - 4 weeks):** 3 weeks float
  - Maximum flexibility among non-critical activities
  - Can absorb delays without project impact

- **Activity H (Install & Test - 2 weeks):** 2 weeks float
  - Even though it comes at end, still has flexibility
  - Can start week 9 or delay until week 11

**4. Resource Optimization:**

- Can delay non-critical activities (A, B, C, D, E, H) to optimize resource usage
- Example: If same team needed for A and F, can delay A by 2 weeks
- Focus best resources on critical path (F, G)

**5. Schedule Compression:**
If need to reduce project duration from 13 to 11 weeks:

- **Option 1:** Crash Activity F (add recruiters) to reduce from 10 to 8 weeks → New duration: 11 weeks
- **Option 2:** Crash Activity G (parallel training sessions) to reduce from 3 to 1 week → New duration: 11 weeks
- **Won't Help:** Crashing A, B, C, D, E, or H (they're not on critical path)

**6. Risk Management Focus:**

- **High Priority:** Monitor F and G closely (daily tracking)
- **Medium Priority:** Watch for path A → C → H (total 11 weeks, close to critical)
- **Low Priority:** Path B → D, B → E have more buffer

**Conclusion:**

The Critical Path Method analysis reveals:

- **Project Duration:** 13 weeks minimum
- **Critical Path:** F → G (Recruit Staff → User Training)
- **Management Focus:** All resources and attention on recruitment (Activity F) and training logistics (Activity G)
- **Flexibility:** Other paths have 2-3 weeks buffer for resource optimization
- **Key Risk:** Recruitment delays; recommend starting immediately with multiple strategies

This CPM analysis provides data-driven insights for scheduling, resource allocation, and risk management, enabling proactive project control.

---

## 📝 SECTION A QUICK-ANSWER BANK (Unit III)

| **Question**                                 | **Answer (2 marks)**                                                                                                                                                                                                                                                                                                                                                    |
| -------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| What is Critical Path Method (CPM)?          | CPM is a network analysis technique to determine longest path through project, identifying minimum duration and critical activities (zero float). Uses forward pass (EST, EFT calculation) and backward pass (LST, LFT calculation). Critical activities cannot be delayed without delaying project. Essential for scheduling and resource prioritization.              |
| Define Total Float                           | Total Float (slack) is maximum time an activity can be delayed without delaying project completion. Formula: TF = LST - EST or LFT - EFT. TF = 0 indicates critical activity (no delay tolerated). TF > 0 indicates non-critical activity with scheduling flexibility. Used for resource leveling and risk management.                                                  |
| What is PERT?                                | PERT (Program Evaluation Review Technique) is probabilistic scheduling method using three time estimates: Optimistic (O), Most Likely (M), Pessimistic (P). Expected Time = (O + 4M + P)/6. Variance = [(P-O)/6]². Used for uncertain durations. Provides probability of meeting deadlines. Better than CPM for R&D, new products.                                      |
| Explain Forward Pass                         | Forward Pass calculates Earliest Start Time (EST) and Earliest Finish Time (EFT) by working forward from project start. Rules: EST of start activities = 0, EFT = EST + Duration. For multiple predecessors: EST = max(EFT of predecessors). Project Duration = maximum EFT of all activities.                                                                          |
| Explain Backward Pass                        | Backward Pass calculates Latest Start Time (LST) and Latest Finish Time (LFT) by working backward from project end. Rules: LFT of end activities = Project Duration, LST = LFT - Duration. For multiple successors: LFT = min(LST of successors). Enables float calculation and critical path identification.                                                           |
| What is Risk Management?                     | Risk Management is systematic process of identifying, assessing, prioritizing, and mitigating project risks. Four phases: (1) Identification - brainstorming, checklists, (2) Assessment - probability × impact, (3) Planning - avoid/mitigate/transfer/accept strategies, (4) Monitoring - track triggers, execute responses. Minimizes negative impact on objectives. |
| List Risk Response Strategies                | Four risk response strategies: (1) **Avoid** - eliminate risk by changing plan, (2) **Mitigate** - reduce probability or impact, (3) **Transfer** - shift to third party (insurance, contracts), (4) **Accept** - do nothing, acknowledge (passive) or set aside contingency (active). Choose based on priority and cost-benefit.                                       |
| What is Risk Probability-Impact Matrix?      | Risk P-I Matrix is qualitative assessment tool plotting risks on grid with Probability (Y-axis: VLow to VHigh) vs Impact (X-axis: VLow to Critical). Risks in High-High quadrant are top priority. Helps prioritize which risks need mitigation. Color-coded: Green (low), Yellow (medium), Red (high), Dark Red (critical).                                            |
| Define Activity Node Structure               | Activity Node in AON networks contains: Activity ID/Name, EST (top-left), EFT (top-right), Duration (center), LST (bottom-left), LFT (bottom-right), Total Float (bottom). Visually represents all scheduling information for one activity. Used in CPM network diagrams for analysis.                                                                                  |
| What is the difference between CPM and PERT? | CPM uses single deterministic duration, focuses on cost-time trade-off, best for well-defined projects. PERT uses three probabilistic estimates (O, M, P), provides expected time and variance, best for uncertain/R&D projects. CPM identifies cost of crashing. PERT calculates completion probability.                                                               |

---

## 💡 EXAM ANSWER TIPS - UNIT III

### For Section A (2 marks):

**CPM/PERT concepts:**

- Line 1: Definition
- Line 2-3: Key formula or process steps
- Keep under 5 lines

**Risk Management:**

- Define + list 4 phases or 4 response strategies
- Very concise

### For Section B (7-10 marks):

**Theory questions:**

- Introduction: Define concept
- Main body: Step-by-step process or detailed explanation
- Example: Simple numerical or scenario
- Conclusion: Benefits/applications

**Rarely asked from Unit III in Section B**

### For Section C (7-10 marks) - MOST IMPORTANT:

**CPM Numerical (Guaranteed Every Year):**

**Time allocation: 25-30 minutes**

**Must-do steps:**

1. **Create activity table** (Duration, Predecessors)
2. **Draw network diagram** (neat, labeled)
3. **Forward pass table** (EST, EFT columns)
4. **Backward pass table** (LST, LFT columns)
5. **Float calculation table** (TF = LST - EST)
6. **Identify critical path** (TF = 0 activities)
7. **State duration and path clearly**
8. **Box final answer**

**Presentation tips:**

- Use tables for calculations (not prose)
- Show formulas before calculating
- Label everything clearly
- Draw network diagram even if not asked (partial credit + helps you solve)
- Double-check critical path logic

**Common mistakes:**

- ❌ Wrong EST when multiple predecessors (should be max, not sum)
- ❌ Wrong LFT when multiple successors (should be min)
- ❌ Forgetting to show project duration
- ❌ Identifying wrong critical path
- ❌ Not drawing network diagram

### PERT Numerical (Less Common):

**If asked:**

1. Table with O, M, P values
2. Calculate TE for each: (O + 4M + P)/6
3. Calculate Variance: [(P-O)/6]²
4. Do CPM with TE values
5. Project Variance = Sum of critical path variances only
6. Probability: Z = (Target - Expected)/SD

**Time: 25-30 minutes**

---

## 📊 UNIT III SUMMARY

**Tier A Topics (Must Master):**

1. ✅ **Critical Path Method (CPM)** - GUARANTEED every year in Section C
2. ✅ Forward Pass & Backward Pass - Always part of CPM question
3. ✅ PERT Technique - High frequency (3/4)
4. ✅ Risk Management - All phases, response strategies

**Tier B Topics (Should Cover):**

1. ✅ Project Schedules - Types and forms
2. ✅ Activity Node Structure - Quick read
3. ✅ Cost Schedules - Brief understanding

**Tier C Topics (Skip):**

1. Objectives of Activity Planning - Low priority
2. Monte Carlo Simulation - Never asked
3. Resource Allocation - Brief mention only

**Time Investment:**

- **CPM practice:** 4 hours (solve 5-7 full problems)
- **PERT practice:** 2 hours (solve 3 problems)
- **Risk Management theory:** 2 hours
- **Other topics:** 1 hour
- **Total: 9 hours for Unit III**

**Critical Practice:**

- ✅ Solve ALL CPM questions from 4 PYQ years
- ✅ Practice drawing network diagrams quickly
- ✅ Memorize formulas: TF = LST - EST, PERT TE = (O+4M+P)/6
- ✅ Master forward/backward pass mechanics
- ✅ Create risk response strategy examples

---

**✅ Unit 3 Notes Complete!**

This is the **MOST IMPORTANT UNIT** - CPM appears in Section C every single year!

Type **'next'** to proceed to **Unit 4 notes** (Project Management and Control - EVA numerical guaranteed!)
