# Metricon University Undergraduate Data Dictionary

This document outlines the structure, definitions, and generation logic for each column in the simulated undergraduate dataset of 10,000 students at Metricon University, as of Spring 2025.

---

## Student Identifiers & Demographics

### `student_id`
- **Description:** Unique identifier for each student
- **Logic:** Sequentially generated IDs from U000001 to U010000

### `gender`
- **Description:** Student's self-reported gender identity
- **Values:** Female, Male, Nonbinary, Prefer not to say
- **Logic:** Reflects national enrollment trends (e.g., 56% Female, 41% Male)

### `race_ethnicity`
- **Description:** Student's race or ethnicity
- **Values:** White, Hispanic/Latinx, Black/African American, Asian, Two or more races, American Indian/Alaska Native, Native Hawaiian/Other Pacific Islander, Prefer not to say
- **Logic:** Weighted distribution modeled on SUNY and national R1 trends

### `age_at_entry`
- **Description:** Age of student when they entered Metricon University
- **Logic:** Most first-time students are 17–18; transfers are 19–22

### `first_generation_status`
- **Description:** Whether student is first in their family to attend college
- **Logic:** Correlated with low income, Pell eligibility, and EFC

### `low_income_status`
- **Description:** Whether student is low-income
- **Logic:** Based on estimated family contribution (EFC) and Pell status

### `residency_status`
- **Description:** In-state, out-of-state, or international residency
- **Values:** In-state, Out-of-state, International
- **Logic:** Majority are in-state, small proportion international

---

## Academic Background & Enrollment

### `high_school_gpa`
- **Description:** Student's GPA upon high school graduation
- **Logic:** Correlated with SAT score and cumulative GPA; normally distributed

### `sat_score`
- **Description:** SAT score (if submitted)
- **Logic:** 25% of students are test-optional; scores range 800–1600

### `entry_term`
- **Description:** First semester enrolled
- **Values:** Ranges from Fall 2020 to Fall 2023 (Spring 2025 is snapshot term)

### `entry_status`
- **Description:** First-time full-time or transfer
- **Logic:** Tied to age, transfer credits, and initial residency

### `major_at_entry`
- **Description:** Declared major upon entry
- **Logic:** Students who recently entered are more likely undecided

### `current_major`
- **Description:** Current major in Spring 2025
- **Logic:** 80% remain in same major; 20% change

---

## Academic Progress & Performance

### `cumulative_gpa`
- **Description:** Overall GPA through Spring 2025
- **Logic:** Correlated with support use, alerts, and HS GPA

### `term_gpa`
- **Description:** GPA for Spring 2025 only
- **Logic:** Closely tied to cumulative GPA, with adjustments for housing and support

### `academic_standing`
- **Description:** Student’s official standing
- **Values:** Good, Probation, Suspension
- **Logic:** Based on GPA thresholds (2.0/1.0)

### `orientation_attended`
- **Description:** Whether student attended orientation
- **Logic:** ~90% of students attended

### `academic_advising_visits`
- **Description:** Number of advising sessions
- **Logic:** Poisson distribution (λ = 2); affects GPA positively

### `tutoring_sessions_attended`
- **Description:** Number of tutoring sessions
- **Logic:** Poisson distribution (λ = 1); moderate correlation with GPA

### `student_org_participation`
- **Description:** Number of student organizations involved in
- **Logic:** Poisson distribution; moderate engagement improves GPA

### `early_alerts_flagged`
- **Description:** Whether flagged by early alert system
- **Logic:** More likely if GPA < 2.5

### `retained`
- **Description:** Still enrolled as of Spring 2025
- **Values:** All set to "Yes" for this snapshot

---

## Degree Progress

### `credits_completed`
- **Description:** Total credits completed
- **Logic:** Based on number of terms completed and transfer credits

### `transfer_credits`
- **Description:** Credits transferred into university
- **Logic:** Present only for transfer students

### `graduated`
- **Description:** Whether the student has graduated by Spring 2025
- **Logic:** Must meet credit and GPA minimums; mostly those who entered in 2020–2021

### `time_to_degree`
- **Description:** Years taken to complete degree (if graduated)
- **Logic:** Normally distributed around 4.2 years (2.5 to 7.0 range)

---

## Financial Aid & Need Indicators

### `pell_grant_received`
- **Description:** Received federal Pell grant
- **Logic:** Likely if EFC < $6,000

### `estimated_family_contribution`
- **Description:** Simulated EFC value
- **Logic:** Normal distribution centered around $10,000

### `scholarship_amount`
- **Description:** Total scholarship aid received (need + merit)
- **Logic:** Linked to GPA and SAT scores

### `food_insecurity_reported`
- **Description:** Whether student reports food insecurity
- **Logic:** Higher likelihood if low-income, first-gen, or Pell recipient

### `housing_insecurity_reported`
- **Description:** Whether student reports housing insecurity
- **Logic:** Correlated with low income and EFC

### `opportunity_program_participant`
- **Description:** Participates in a college opportunity program (e.g., EOP)
- **Logic:** Based on EFC, Pell, residency, first-gen, and income indicators

---

## Living Situation

### `housing_status`
- **Description:** Whether student lives on campus or commutes
- **Values:** On-campus, Off-campus
- **Logic:** Depends on entry status, age, financial status, and residency

