# Beyond the Grandstand: Qualtrics Simulation Methodology and Technical Reference

**Course:** BA 600 001 – Consulting Studio  
**School:** University of Michigan – Stephen M. Ross School of Business  
**Project partners:** Office of Action-Based Learning and Office of Digital Education  
**Document owner:** Kat Parker - ODE  
**Faculty lead:** Andy Wicklund  
**Technical lead:** Kat Parker  
**Simulation version:** Version 1  
**Last updated:** 09/25/2026  
**Status:** Draft

---

## 1. Document Purpose

This document explains the instructional design, simulation methodology, technical architecture, scoring system, content-management process, and operating procedures for the **Beyond the Grandstand: Scaling the Manitou Island Ghosts** simulation.

It is intended for:

- Faculty members
- Course administrators
- Action-based learning staff
- Digital education staff
- Future simulation maintainers
- Other project stakeholders

This document is designed to answer the following questions:

1. What is the simulation intended to teach?
2. How does the four-level experience work?
3. How are team decisions scored?
4. How are curveballs assigned?
5. How does the simulation remain consistent for group participants?
6. Which parts of the simulation are managed in Qualtrics?
7. Which content is managed outside Qualtrics?
8. How are updates tested and published?
9. What data are collected?
10. What should future maintainers know?

---

## 2. Executive Summary

**Beyond the Grandstand** is a multi-day, team-based consulting simulation hosted in Qualtrics. Students act as consultants to the Manitou Island Ghosts, an independent minor-league baseball organization seeking to become a major regional attraction.

The simulation operates as a rule-based game master. It:

- Presents a common business case
- Guides teams through sequential decision nodes
- Introduces changing business conditions
- Assigns curveballs
- Tracks hidden performance dimensions
- Records team recommendations and reflections
- Provides recaps across multiple simulation levels
- Produces a final strategic archetype

Decisions, scoring effects, curveball assignments, branching, and outcomes are determined by predefined rules and configuration files.

### High-level design

| Component | Approach |
|---|---|
| Delivery platform | Qualtrics |
| Participation modes | Solo and group |
| Number of levels | 4 |
| Decision nodes per level | 5 |
| Total scored nodes | 20 |
| Choices per node | 5 |
| Curveball pools | 3 |
| Scoring dimensions | 5 |
| Student score visibility | Hidden |
| Narrative content source | Qualtrics-hosted JSON |
| Scoring source | Qualtrics-hosted JSON |
| Release schedule | Google Sheet/API |
| Final outcomes | 4 archetypes |

---

## 3. Instructional Context

### 3.1 Course context

The simulation takes place during the opening week of BA 600. It prepares Master of Management students for a sponsored action-based learning engagement by allowing them to practice problem framing, decision-making under uncertainty, stakeholder management, and collaborative consulting behaviors.

### 3.2 Student audience

- Program: All Winter Master of Management students
- Approximate enrollment: [Number]
- Typical prior business experience: Limited
- Typical team size: [Number]
- Number of teams: [Number]
- Relevant accessibility or scheduling considerations: [Description]

### 3.3 Why a simulation is used

[Explain why the learning objectives cannot be addressed as effectively through lecture or a static written case alone.]

Example:

> A static case allows students to analyze a stable set of facts. This simulation instead requires teams to make decisions before all relevant information is available and then adapt when external conditions change. This better approximates the ambiguity, stakeholder complexity, and iterative judgment involved in a consulting engagement.

---

## 4. Learning Objectives

The simulation supports the following learning objectives.

### 4.1 Defining and solving problems to improve enterprise performance

Students will:

- Define complex business problems, create and test hypotheses, analyze data, and deliver actionable recommendations utilizing frameworks learned in core courses. 
- Drive change and innovation within an organizational context.


### 4.2 Making decisions under uncertainty and ambiguity

Students will:

- Plan, execute, control, and close projects successfully. 
- Navigate ambiguity, develop risk mitigation strategies and adapt to unforeseen changes swiftly and effectively.
- Experience personal growth through intentional exposure to challenging opportunities strengthening resilience through the process.



### 4.3 Communicating persuasively to build courage and conviction to act

Students will:

- Prepare and deliver compelling presentations and reports to stakeholders. 
- Develop negotiation skills and build consensus among team members and stakeholders.


### 4.4 Working collaboratively in inclusive teams and with learning partners

Students will:

- Lead diverse teams, manage conflicts, foster collaboration, and deliver shared success across learning partners including sponsors and faculty advisors through establishing and nurturing high-quality professional relationships.

### 4.5 Thinking critically to identify opportunities and deliver impact

Students will:

- Ethically evaluate tradeoffs of business decisions. 
- Be aware of bias and assumptions. 
- Consider the cultural context in which the project is taking place.


---

## 5. Business Case Summary

### 5.1 Organization

The Manitou Island Ghosts (MIGs) are an independent minor league baseball team operating out of Traverse City, Michigan. Playing their home games at a stadium just off the main tourist corridor, the Ghosts enjoy steady, localized fan support. Ticket sales remain stable, covering overhead and keeping the lights on, but the franchise has reached a plateau. Despite Traverse City’s booming summer tourism industry, the Ghosts remain an afterthought for visitors who prioritize wineries, beaches, and dining.

### 5.2 Strategic challenge

The Chief Marketing Officer (CMO) has set an ambitious goal: transform the Ghosts from a casual regional pastime into a primary regional attraction—a must-visit destination akin to the sports-entertainment phenomenon of the Savannah Bananas. The franchise owners want a strategy that drives revenue, increases brand equity, and leverages the region's tourism footprint without alienating their loyal local fan base.

### 5.3 Primary objectives

- Brand Transformation: Shift public perception from a standard minor league ballclub to a premier sports-entertainment destination.
- Economic Impact: Drive higher out-of-town attendance, merchandise sales, and community partnerships.
- Strategic Roadmap: Deliver an actionable, high-ROI marketing and operational plan to the team sponsor and ownership group within a four-phase rollout.


### 5.4 Intentional ambiguity

The case does not provide all information needed to make a risk-free decision. This is intentional.

Students must decide:

- Which evidence is most important
- Which assumptions are acceptable
- When additional analysis is warranted
- How much to adapt after receiving new information
- Which tradeoffs are most important
