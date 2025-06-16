# 🎓 Metricon University Graduate Student Data Dictionary

This document provides a detailed explanation of all variables included in the graduate student success dataset.

Each entry describes:
- **Type** (e.g., Boolean, Float, Categorical)
- **Description** (What the variable measures)
- **Logic** (How the value was simulated or derived)

## Graduate Student Dataset (2,000 Students)

### `student_id`
- **Type:** String
- **Description:** Unique identifier for each student.
- **Logic:** Randomly generated unique ID.

### `program_name`
- **Type:** Categorical
- **Description:** Graduate program of enrollment.
- **Logic:** Drawn from STEM, social science, and humanities fields. Used to influence time to degree and assistantship likelihood.

### `degree_type`
- **Type:** Categorical
- **Description:** Type of degree pursued (Master’s or PhD).
- **Logic:** Used to determine progression stages and funding.

### `gender`
- **Type:** Categorical
- **Description:** Self-reported gender identity.
- **Logic:** Sampled to reflect SUNY-wide graduate gender ratios. Majority female.

### `race_ethnicity`
- **Type:** Categorical
- **Description:** Student-reported race/ethnicity.
- **Logic:** Sampled to match graduate diversity statistics across public SUNY institutions.

### `age_at_entry`
- **Type:** Integer
- **Description:** Age when entering graduate program.
- **Logic:** Ranges from 21–35 with PhD skewing slightly older.

### `domestic_or_international`
- **Type:** Categorical
- **Description:** Student residency type.
- **Logic:** 34% international, consistent with Binghamton trends.

### `first_generation_status`
- **Type:** Boolean
- **Description:** First in family to attend graduate school.
- **Logic:** More common among domestic students.

### `undergraduate_institution_type`
- **Type:** Categorical
- **Description:** Type of undergraduate institution attended.
- **Logic:** Domestic students skew public; international skew private or foreign.

### `attended_orientation`
- **Type:** Boolean
- **Description:** Attended graduate orientation.
- **Logic:** High participation for newer students; optional for older cohorts.

### `prof_dev_workshops_attended`
- **Type:** Integer
- **Description:** Number of professional development workshops attended.
- **Logic:** Varies with academic stage. Higher in earlier years and near job market preparation.

### `used_writing_center`
- **Type:** Integer
- **Description:** Number of times student accessed writing support services.
- **Logic:** Correlated with conference output and publication efforts.

### `used_graduate_advising`
- **Type:** Integer
- **Description:** Times student met with graduate advisors.
- **Logic:** Higher usage by students flagged for academic difficulty.

### `publication_count`
- **Type:** Integer
- **Description:** Total peer-reviewed publications.
- **Logic:** Varies by field and degree stage; more common among PhD students.

### `high_impact_publication`
- **Type:** Boolean
- **Description:** At least one publication in a high-impact journal.
- **Logic:** 10–15% of publishing students.

### `conference_presentations`
- **Type:** Integer
- **Description:** Number of academic conference presentations.
- **Logic:** Skewed higher for PhD students nearing completion.

### `mental_health_referrals`
- **Type:** Integer
- **Description:** Referrals or engagements with mental health services.
- **Logic:** Discretely sampled across all years and demographics.

### `food_insecurity_reported`
- **Type:** Boolean
- **Description:** Student reported food insecurity.
- **Logic:** Linked to funding levels and assistantship type.

### `housing_insecurity_reported`
- **Type:** Boolean
- **Description:** Student reported housing insecurity.
- **Logic:** Correlated with stipend amount and assistantship type.

### `admit_term`
- **Type:** String
- **Description:** Term student entered the program.
- **Logic:** Drives expected progress through milestones.

### `full_time_status`
- **Type:** Boolean
- **Description:** Whether the student is full-time.
- **Logic:** Most students are full-time unless in advanced stages or working over 30 hours.

### `advisor_assigned`
- **Type:** Boolean
- **Description:** Assigned faculty advisor.
- **Logic:** Nearly universal after year 1.

### `cumulative_gpa`
- **Type:** Float
- **Description:** Overall graduate GPA.
- **Logic:** Most between 3.3–4.0; values <3.0 may trigger intervention.

### `credits_completed`
- **Type:** Integer
- **Description:** Total graduate credits earned.
- **Logic:** Aligned with admit term and progression benchmarks.

### `qualifying_exam_passed`
- **Type:** Boolean
- **Description:** Whether qualifying exams were passed (PhD only).
- **Logic:** Tied to year in program and PhD-only filter.

### `proposal_defended`
- **Type:** Boolean
- **Description:** Dissertation proposal successfully defended.
- **Logic:** Occurs after qualifying exam and before dissertation defense.

### `dissertation_defended`
- **Type:** Boolean
- **Description:** Final dissertation defense completed.
- **Logic:** Only TRUE for PhD students nearing or at graduation.

### `thesis_submitted`
- **Type:** Boolean
- **Description:** Indicates if a Master’s thesis was submitted.
- **Logic:** Required for some Master’s programs; tied to department rules.

### `abd_status`
- **Type:** Boolean
- **Description:** Indicates student is ABD (All But Dissertation).
- **Logic:** TRUE if proposal is defended but dissertation not yet completed.

### `graduated`
- **Type:** Boolean
- **Description:** Whether student has graduated by Spring 2025.
- **Logic:** PhD students typically take 5–7 years; Master’s take 2–3 years. Driven by admit_term and degree_type.

### `time_to_degree`
- **Type:** Float
- **Description:** Total time taken to complete degree, in years.
- **Logic:** Populated only for graduated students.

### `assistantship_type`
- **Type:** Categorical
- **Description:** Type of funding/assistantship (TA, RA, GA, or none).
- **Logic:** TA more common in Humanities; RA in STEM. None for unfunded.

### `funding_status`
- **Type:** Categorical
- **Description:** Fully, partially, or unfunded.
- **Logic:** Tied to assistantship type and degree program.

### `stipend_amount`
- **Type:** Float
- **Description:** Annual stipend received.
- **Logic:** Ranges from $5,000 (partial) to $30,000 (full funding).

### `hours_worked_per_week`
- **Type:** Integer
- **Description:** Hours worked in on/off-campus jobs.
- **Logic:** Correlated with funding level; <20 hrs for most funded students.

