# enterprise-systems-requirements-spec
# Enterprise Software Requirements Specification (SRS)

# CampusMealSync: Software Requirements Specification (SRS)
### CIS 3300 — Systems Analysis & Design | Group #7 Client Project

> **Project Title:** CampusMealSync (Enterprise Campus Resource & Meal Synchronization System) 
> **Course:** CIS 3300 — Systems Analysis & Design | Georgia State University
> **Role:** Lead Systems Analyst & Requirements Engineering (Elicitation, Functional Decomposition, Process Modeling)
> **Team Members:** Araceli Andrade Gutierrez, Muamer Begovic, Elad Bogle, Jayla Jones, Saki Mohamed
> **Project Scope:** 2-Week Intensive Agile Analysis Sprint (Inferred from lecture specifications and embedded criteria)

---

## 1. Project Vision & Executive Summary

Across the Georgia State University downtown campus, hundreds of students experience food insecurity, while campus dining facilities and meal-plan holders generate predictable daily surpluses of unused swipes and prepared food. **Panther's Pantry** faces persistent manual fulfillment bottlenecks, lacking real-time visibility into inventory and intake channels

+---------------------+       +-----------------------+       +----------------------+
|  SURPLUS RESOURCES  | ----> | OPERATIONAL BOTTLENECK| ----> |   NEGATIVE IMPACT    |
| Unused meal swipes  |       | Panther's Pantry manual|       | Food waste & student |
| & dining hall food  |       | fulfillment bottlenecks|       | insecurity continue  |
+---------------------+       +-----------------------+       +----------------------+


**CampusMealSync** is an enterprise resource management platform designed to bridge the operational gap between GSU Dining Services, Panther's Pantry staff, and students. The platform enables peer-to-peer meal swipe reallocation, dynamic pantry inventory reservation, and real-time surplus dining notifications, replacing fragmented physical queues with an automated, stigma-free digital pipeline.

---
## 2. Stakeholder Taxonomy & User Classes

To resolve ambiguity from early lecture requirements, our analysis defined three distinct user tiers based on operational interactions

+----------------------------+--------------------------------+------------------------------+
| GSU STUDENTS (Favored)     | PANTHER'S PANTRY STAFF (Favored)| DINING VENDORS (Secondary)   |
| • Frictionless swipe giving| • Real-time inventory control  | • 1-tap end-of-day surplus   |
| • Stigma-free, anonymous   | • Automated intake schedules   |   broadcasts                 |
|   intake & reservations    | • Fulfillment bottleneck triage| • Minimized waste liability  |
+----------------------------+--------------------------------+------------------------------+


1. **GSU Students (Favored User Class):** Meal plan holders wanting to donate excess swipes, alongside students requiring immediate, confidential access to meal allocations and pantry goods.
2. **Panther's Pantry Staff & Volunteers (Favored User Class):** Operations managers requiring live inventory tracking, scheduled pickup windows, and automated intake logging to eliminate line congestion.
3. **Campus Dining Vendors / Managers (Secondary User Class):** Dining commons administrators who need single-tap broadcast tools to alert registered students to perishable end-of-day food surpluses.

---

## 3. System Architecture & Feature Tree Decomposition

The system's core capabilities are organized into four functional epics:

                              [ CampusMealSync Core ]
                                         │
     ┌───────────────────┬───────────────┴───────────────┬───────────────────┐
     ▼                   ▼                               ▼                   ▼
[ Panther's Pantry ] [ Peer-to-Peer Swipes ]        [ Surplus Food Alerts ] [ Analytics Hub ]
• Live inventory     • Secure swipe donation        • Push notifications    • Bottleneck metrics
• Pickup scheduling  • Anonymous swipe requests     • Opt-in student alerts • Donation auditing


### Epic 1: Panther's Pantry Digital Reservation Hub
* **FE-01 (Real-Time Inventory Visibility):** Live catalog tracking available pantry goods, dietary categories (e.g., halal, vegan, gluten-free), and stock levels to prevent stockout friction.
* **FE-02 (Staggered Pickup Scheduling):** Time-slot reservation engine that smooths visitor foot-traffic, eliminating physical queues outside pantry distribution centers.

### Epic 2: Peer-to-Peer Meal Swipe Exchange Engine
* **FE-03 (Secure Swipe Donation Pool):** Interface allowing meal-plan holders to transfer unused contract swipes into an anonymous campus pool without handling financial transactions.
* **FE-04 (Stigma-Free Request Channel):** Direct, privacy-preserving credential issuance allowing students facing immediate hunger to claim meal vouchers redeemable at GSU Dining Commons.

### Epic 3: Dining Hall Surplus Broadcast Layer
* **FE-05 (Vendor Broadcast Console):** Rapid-entry interface for dining managers to post surplus quantity, location (e.g., Central Hub, Dining Commons), and expiration windows.
* **FE-06 (Push Notification Distribution):** Geolocation- and preference-based alert system notifying opt-in students when verified prepared food is available for immediate pickup.

### Epic 4: Operational Analytics & Reporting Dashboard
* **FE-07 (Bottleneck & Fulfillment Auditing):** Data logging module tracking fulfillment times, unclaimed reservations, and peak pickup windows to optimize pantry volunteer shifts.
* **FE-08 (Resource Reallocation Metrics):** Administrative reporting evaluating total diverted food waste (in lbs) and redistributed meal values.

---

## 4. Requirements Engineering & Systems Analysis Artifacts

* **Structured Requirements Elicitation:** Conducted peer and administrative interview sessions to uncover root operational causes—identifying that meal insecurity on campus is driven by information asymmetry rather than total resource scarcity.
* **Agile Decomposition Under Ambiguity:** Decoupled dense lecture presentation criteria into an actionable product backlog, organizing functional dependencies into 4 epics, 8 feature modules, and validated user stories.
* **Data Modeling & Normalization:** Designed 3NF-compliant Entity-Relationship Diagrams (ERDs) mapping `STUDENT`, `SWIPE_DONATION`, `PANTRY_INVENTORY`, `PICKUP_RESERVATION`, and `SURPLUS_ALERT` entities with primary/foreign keys and referential integrity constraints.
* **Process & Boundary Modeling:** Authored Context (Level 0) and Level 1 Data Flow Diagrams (DFDs) tracing inputs from GSU single sign-on authentication through database transactions and push notification gateways.

---

## 5. CIS 3300 SRS Verification Criteria

| Academic Evaluation Standard | Project Implementation Alignment |
| :--- | :--- |
| **Meaningful Community Impact** | Directly targets documented student hunger and dining food waste at GSU. |
| **Direct Stakeholder Access** | Leveraged immediate access to GSU student peers and Panther's Pantry staff for authentic requirements discovery. |
| **Information-Driven Solvability**| Solves data visibility and coordination friction rather than physical warehouse constraints. |
| **Scattered Requirement Synthesis**| Successfully inferred, structured, and presented an Agile requirements blueprint despite ambiguous and embedded baseline course prompts. |
## 2. Stakeholder Taxonomy & User Classes

To resolve ambiguity from early lecture requirements, our analysis defined three distinct user tiers based on operational interactions[cite: 28]:
