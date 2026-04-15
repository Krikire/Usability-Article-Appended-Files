# Appended Files to Article about Gamified Systems Usability

This repository contains supplementary data for the article on the usability of gamified systems. Two Excel workbooks are provided:

- [Results.xlsx](Results.xlsx) — evaluation data and aggregated results for every analysed gamified system.
- [usabilityRecommendationsForGamifiedSystems.xlsx](usabilityRecommendationsForGamifiedSystems.xlsx) — the rule base of usability recommendations used to perform the evaluation.

---

## 1. `Results.xlsx`

The workbook is organised into three logical groups of sheets: a per-system evaluation sheet for each analysed application, a category-level aggregation sheet, and a final results sheet.

### 1.1 Sheet: System-Level Evaluation Data

*Sheets: `Duolingo`, `Duolingo ABC`, `Khan academy`, `Khan academy kids`, `Headspace`, `FITBIT`, `CodeAcademyGo`, `Fortune city`, `Habitica`, `Memrise`, `Brilliant`, `Fabulous`, `Clarify by fabulous`, `Strava`, `SuperBetter`, `Lumosity`, `Sidekick Health`, `ABCmouse`, `CogniFit`, `Shape by fabulous`, `Habit Tracker - Habit Mate`, `TaskGame - Gamify your life`, `Habio - Simple Habit Tracker`, `Walken`, `Narn Habit Tracker & Goals`, `Aula Lengua`, `Foursquare Swarm - Check In`, `Roomsy Chores Tracker & Chart`, `Fitmint - Walk & Steps Tracker`, `Workout Quest - Gamified Gym`, `Death Reminder App`, `Pharmacy Crack Rx Drug Trivia`, `Gametize Explore Experiences`.*

Each sheet presents detailed evaluation data for one analysed gamified system and contains structured tables used to assess the implementation of usability recommendations.

#### 1.1.1 Evaluation of Recommended Gamification Elements (URSIGE)

The first table presents the evaluation of usability recommendations for recommended gamification elements (URSIGE).

Three types of usability recommendation sources are included:

- Recommendations by age group and application domain
- ISO 9241 recommendations
- WCAG 2.2 recommendations

For each gamification element (e.g., Quests, Points, Levels), the following implementation levels are recorded:

- **Fulfilled** — the recommendation is fully implemented
- **Partially fulfilled** — the recommendation is partially implemented
- **Not fulfilled** — the recommendation is not implemented
- **Total** — total number of applicable recommendations (Fulfilled + 0.5 × Partially fulfilled)

The values in the table indicate the number of recommendations in each category.

A summary table on the right aggregates these values and provides:

- Total number of recommendations
- Number of fulfilled recommendations
- Number of partially fulfilled recommendations
- Number of not fulfilled recommendations
- Overall fulfilment percentage

#### 1.1.2 Evaluation of Not Recommended Gamification Elements (URUIGE)

The second table follows the same structure but evaluates usability recommendations for gamification elements that were **not** recommended by the tool but were still implemented in the system (URUIGE).

The same three recommendation sources are used:

- Recommendations by age group and application domain
- ISO 9241 recommendations
- WCAG 2.2 recommendations

The evaluation logic is identical to the recommended elements:

- Fulfilled / Partially fulfilled / Not fulfilled counts are recorded
- Totals and aggregated results are calculated

A summary table provides overall metrics for non-recommended elements, including:

- Total number of recommendations
- Number of fulfilled recommendations
- Number of partially fulfilled recommendations
- Number of not fulfilled recommendations
- Overall fulfilment percentage

#### 1.1.3 Degree of Satisfaction (DoS) Calculation

At the bottom of the sheet, the Degree of Satisfaction (DoS) is calculated for the evaluated application.

The calculation is based on:

- **P** — total number of ratings
- **H** — number of high ratings
- **C** — number of low ratings
- **n** — control parameter

The DoS metric is used to reflect the overall user satisfaction with the application and is later used in correlation analysis with usability recommendation adherence.

### 1.2 Sheet: Results by Recommendation Category

*Sheet: `Results by recommendation categ`.*

This sheet presents aggregated results for each analysed gamified system. Each column represents a system. Each row represents evaluation results for a specific recommendation category.

The following categories are evaluated:

- General Usability Recommendations (GUR)
- Implemented Gamification Elements (IGE)
- Usability Recommendations for Recommended Gamification Elements (URSIGE)
- Usability Recommendations for Not Recommended Gamification Elements (URUIGE)

#### 1.2.1 General Usability Recommendations (GUR)

This section shows how each system satisfies general usability recommendations. The following values are provided:

- Total number of recommendations
- Fulfilled
- Partially fulfilled
- Not fulfilled
- Total fulfilled (Fulfilled + 0.5 × Partially fulfilled)
- Percentage fulfilled

#### 1.2.2 Implemented Gamification Elements (IGE)

This section evaluates how many recommended gamification elements are implemented. The following values are provided:

- Total number of recommended gamification elements
- Number of elements implemented in the system
- Percentage of recommended elements implemented

#### 1.2.3 Usability Recommendations for Recommended Elements (URSIGE)

This section presents aggregated results of usability recommendation implementation for recommended gamification elements. The values are derived from the system-level evaluation sheets, where each system was analysed individually.

#### 1.2.4 Usability Recommendations for Not Recommended Elements (URUIGE)

This section presents aggregated results of usability recommendation implementation for gamification elements that were not recommended but are implemented in the system. The values are derived from the system-level evaluation sheets.

### 1.3 Sheet: Results

*Sheet: `Results`.*

This sheet presents the aggregated results of all analysed gamified systems. Each row represents a single gamified system. Each column represents a specific evaluation metric.

#### 1.3.1 System Information

- **Age group** — target user groups of the system (e.g., children, teenagers, adults, elderly)
- **Application domain** — domain(s) in which the system is used (e.g., education, health, productivity)

#### 1.3.2 Popularity Metrics

- **User rating** — average user rating of the system (from Google Play store)
- **Rate number** — total number of user ratings (from Google Play store)
- **Downloads** — total number of downloads
- **Popular rate (DoS)** — Degree of Satisfaction metric calculated based on rating distribution; reflects overall user satisfaction and mitigates bias caused by rating volume

#### 1.3.3 Usability and Gamification Metrics

- **General Usability Recommendations (GUR)** — percentage of general usability recommendations fulfilled in the system
- **Implemented Gamification Elements (IGE)** — percentage of recommended gamification elements that are implemented in the system
- **Usability Recommendations for Recommended Gamification Elements (URSIGE)** — percentage of usability recommendations fulfilled for recommended gamification elements
- **Usability Recommendations for NOT Recommended Gamification Elements (URUIGE)** — percentage of usability recommendations fulfilled for gamification elements that were not recommended but are implemented
- **Overall** — combined adherence metric calculated from GUR, URSIGE, and URUIGE
- **Elements recommendations (URGE)** — overall adherence to usability recommendations for gamification elements

---

## 2. `usabilityRecommendationsForGamifiedSystems.xlsx`

This workbook contains the rule base of usability recommendations that drives the evaluation in `Results.xlsx`. Each sheet defines recommendations as input/output rules: the INPUT columns describe the applicability conditions (e.g., age group, application domain, disorder, usability goal, gamification element) and the OUTPUT columns provide the recommendation itself together with an illustrative example.

### 2.1 Sheet: Generalised recommendations

General usability recommendations applicable at the system level (GUR).

- **INPUT:** `usabilityGoal`, `usabilityPrinciple`, `ageGroup`, `applicationDomain`, `disorder`, `gamificationGoal`
- **OUTPUT:** `genRecommendation`, `example`

### 2.2 Sheet: Suitable gamification elements

Gamification elements that are recommended for a given context, together with the usability recommendations to apply when they are implemented. Feeds the URSIGE evaluation.

- **INPUT:** `ageGroup`, `applicationDomain`, `disorder`, `gamificationGoal`, `usabilityGoal`
- **OUTPUT:** `gamificationElement`, `usabilityRecommendation`

### 2.3 Sheet: Not suitable gamification elements

Gamification elements that are **not** recommended for a given context. Used to identify non-recommended but implemented elements whose usability is evaluated under URUIGE.

- **INPUT:** `ageGroup`, `applicationDomain`, `disorder`, `usabilityGoal`, `gamificationGoal`
- **OUTPUT:** `notSuitableGamificationElement`

### 2.4 Sheet: ISO

Usability recommendations for gamification elements derived from the ISO 9241 family of standards.

- **INPUT:** `gamificationElement`
- **OUTPUT:** `ISOrecommendation`, `elementUsabilityRecommendation`, `example`

### 2.5 Sheet: WCAG

Usability recommendations for gamification elements derived from WCAG 2.2, scoped by disorder (e.g., hearing impairment, visual impairment).

- **INPUT:** `gamificationElement`, `disorder`
- **OUTPUT:** `WCAGrecommendation`, `elementUsabilityRecommendation`, `example`
