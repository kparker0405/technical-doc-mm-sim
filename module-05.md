## 9. Hidden Scoring Methodology

Students do not see their score totals during normal production use.

Each decision affects one or more of five dimensions.

| Dimension | Definition |
|---|---|
| Enterprise Impact | Potential to improve growth, revenue, brand value, or organizational performance |
| Critical Rigor | Quality of analysis, evidence, assumptions, and risk evaluation |
| Strategic Decisiveness | Ability to establish priorities, make recommendations, and maintain appropriate focus |
| Stakeholder Trust | Ability to build credibility, alignment, and professional relationships |
| Resourcefulness | Ability to use available resources, partnerships, pilots, and adaptive approaches effectively |

### 9.1 Score updates

For each selected choice:


```
New cumulative score
=
Previous cumulative score
+
Choice-specific score effect
```

### 9.2 Score range
Score effects currently use:

```
-2 to 2
```
A negative score indicates a tradeoff or risk. It does not necessarily mean that the choice is irrational or professionally indefensible. 

### 9.3 Student visibility
In production mode:
- Students do not see scores.
- Students do not see scoring thresholds.
- Students do not receive "correct" or "incorrect" messages.
- Consequences are communicated through narrative develpoments and the final outcome. 

In development mode:
- Current cumulative scores may be displayed. 
- QIDs, NodeKeys, and selected positions may be displayed. 
- Configuration versions may be displayed. 

---
### Strategic-State Variables
Some decisions establish or updated a named strategic state.
| State variable | Set at | Purpose|
| ----------- | ----------- | -----------|
|InitialStategy | Node 1.1 | Records the initial project direction |     
MidpointStrategy | Node 2.2 | Records the strategy after initial adaptation |
|CrisisStrategyResponse | Node 3.4 | Records the crisis-response posture|
|FinalStrategy | Node 4.1 | Records the final strategic direction |

These variables support:
- Recap text
- Faculty analysis
- Final reflection
- Interpretation of the team's strategic path

---
## 11. Curveball Methodology
### 11.1 Curveball pools
|Pool|Category|Number of events| Placement|
|----|------|-----|----|
|1|Tourism and Regional Infrastructure|5|Before Level 2|
|2| Economic and Corporate Landscape|5|Before Node 3.1|
|3A|Local Policy and Community Relations|5|After Node 3.1|
|3B|Competitive Environment and Market Dynamics|5|After Node 3.1|

### 11.2 Group assignment
Group-mode curveballs are assigned deterministcally using the Team ID. This provides:
- Consistency for all members of the same team
- Balanced assignment across up to 100 groups
- Reproducible assignments
- Comparable but nonidentical team experiences

The formula that designates which curveball is assigned to which group is based off of calculates done to to their team number. 

For Pool 1, each of the five events appears 20 times across Teams 1-100.

For Pool 2, we use a different balanced pattern so its assignment is not identifcal to pool 1, and each of the five events appears 20 times across Teams 1-100.

For Pool 3, odd-numbered teams are designated a curveball from the Community/Policy category, and even-numbered teams is designated a curveball from the Competition/Market category. Each event in the selected Pool 3 category appears 10 times across Teams 1-100. 

### 11.3 Solo assignment
Solo participants receive:
- One random event from Pool 1
- One random event from Pool 2
- One random Pool 3 category
- One random event from the selected Pool 3 category

The selected events are stored in embedded variables and remain fixed for the duration of the simulation. 

### 11.4 Curveball content
Curveball content is maintained outside individual Qualtrics questions. Each curveball contains:
```
CurveballID
PoolNumber (1-3)
Category
PoolPosition (1-5)
Title
Body
Active (0-1)
```
One generic Qualtrics display question inserts the assigned title and body dynamically.
## 12. Final Archetype Methodology
The simulation produces one of four ending archetypes. 
|Archetype| General interpretation|
|-----|-----|
|Regional Powerhouse| Strong enterprise impact, rigor, and stakeholder trust|
|Viral Spectacle| High enterprise impact without equally strong balance in other dimensions|
|Safe Hometown Club| Strong stakeholder trust but less enterprise impact|
|Unaligned Agency|Insufficient strategic alignment, trust, or enterprise impact|
### 12.1 Current decision logic
```
IF Enterprise Impact is high 
AND Critical Rigor is high
AND Stakeholder Trust is high:
    Regional Powerhouse

Else if Enterprise Impact is high:
    Viral Spectacle

Else if Stakeholder Trust is high:
    Safe Hometown Club

Else:
    Unaligned Agency
```
### 12.2 Threshold Calculations
The maximum possible score for a dimension is calculated by:
1. Identifying the highest available score for that dimension at each node.
2. Summing those node-level maximums.
3. Multiplying the total by the threshold percentage.
4. Rounding upward.
The threshold is currently the maximum possible score multiply by 60%.
### 12.3 Ending content
Final archetype titles and descriptions are stored in the simulation content file and dynamically insertde into one Qualtrics outcome question.
## 13. Decision Logs and Recaps
### 13.1 Purpose
Decision logs capture information that multiple-choice selections cannot fully represent:
* Current recommendation
* Primary rationale
* Main uncertainty 
* Team decision process
* Confidence level
### 13.2 Daily decision-log fields
|Field|Purpose|
|---|---|
|Recommendation|Captures the team's current direction|
|Rationale| Captures the strongest supporting reason|
|Uncertainty|Identifies the most important unresolved assumption|
|Alignment|Records how the group reached the decision|
|Confidence|Records confidence on a 1-5 scale|
### 13.3 Recaps
At the start of later levels, Qualtrics displays a concise recap using piped text from earlier decision logs.
Recaps may include:
* Current strategic direction
* Previous recommendation
* Primary uncertainty
* Crisis-response posture
* Conditions that would cause reconsideration
