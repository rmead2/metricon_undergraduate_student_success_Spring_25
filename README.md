# Metricon University Spring 2025 Undergraduate Student Success Simulation

This repository contains a simulated dataset representing 10,000 undergraduate students enrolled at **Metricon University**, a fictional large public R1 institution modeled after SUNY system trends. The project is designed to support exploratory data analysis, predictive modeling, and the design of student success interventions in higher education.

## Dataset Overview

- **Name:** `metricon_undergraduates_full_final.csv`
- **Snapshot Term:** Spring 2025
- **Population:** 10,000 undergraduate students
- **Institution Type:** Fictional public R1 university
- **Use Case:** Educational data modeling, student success research, academic analytics training

The dataset includes variables such as:
- **Demographics** (race/ethnicity, gender, age at entry, first-gen status, etc.)
- **Academic performance** (GPA, credits, academic standing)
- **Financial indicators** (EFC, Pell, scholarships, opportunity program)
- **Support engagement** (advising visits, tutoring sessions)
- **Basic needs and housing** (food/housing insecurity, housing status)
- **Enrollment history** (entry term, entry status, major changes, graduation status)

All data is **synthetically generated** using probabilistic rules based on national and SUNY-specific trends. No real student data is used.

## Repository Structure

```text
.
├── data/                       # Raw and processed CSV files
│   └── metricon_undergraduates_full_final.csv
│
├── notebooks/                 # RMarkdown analysis notebooks
│   └── data_exploration.Rmd
│
├── docs/                      # Supporting documentation
│   └── data_dictionary.md
│
├── scripts/                   # R scripts used to generate data
│   └── generate_students.R
│
├── README.md                  # This project overview
└── LICENSE                    # MIT License
```

## Data Generation Logic

Each column in the dataset was generated using rules grounded in real-world enrollment, engagement, and student success trends from public R1 universities (e.g., SUNY system). For example:

- `first_generation_status` is more likely among students with low EFC and Pell eligibility.
- `cumulative_gpa` is linked to engagement factors like tutoring, advising, and early alerts.
- `housing_status` is based on age, entry status, income level, and residency.
- `opportunity_program_participant` is tied to financial, demographic, and academic equity markers.

For a full explanation of all columns and generation rules, see the [Data Dictionary](./docs/data_dictionary.md).
