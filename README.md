# Metricon University Student Success Simulation (Spring 2025)

This repository contains two simulated datasets representing **undergraduate** and **graduate** students enrolled at Metricon University, a fictional large public R1 institution modeled after larger higher education system trends. The project is designed to support exploratory data analysis, predictive modeling, and the design of student success interventions in higher education.

---

## Dataset Overview

### Undergraduate Dataset
- **File**: `metricon_undergraduates_student_success_Spring_25.csv`
- **Snapshot Term**: Spring 2025
- **Population**: 10,000 undergraduate students
- **Focus**: Demographics, academic performance, financial indicators, student support usage, and graduation outcomes

### Graduate Dataset
- **File**: `metricon_graduate_student_success_Spring_25.csv`
- **Snapshot Term**: Spring 2025
- **Population**: 2,000 graduate students (Master’s and PhD)
- **Focus**: Program type, degree milestones, assistantship funding, academic productivity, time-to-degree, and wellness markers

---

## Use Cases

These datasets support:
- Educational data modeling and analysis
- Student success research and intervention design
- Institutional planning simulations
- Academic and career advising analytics
- Graduate student equity and funding studies

---

## Repository Structure

```
.
├── data/                       # Raw and processed CSV files
│   ├── metricon_graduate_student_success_Spring_25.csv
│   └── metricon_undergraduates_student_success_Spring_25.csv
│
├── docs/                      # Supporting documentation
│   ├── metricon_undergraduate_data_dictionary.md
│   └── metricon_graduate_data_dictionary.md
│
├── .gitignore                 # Files and patterns to exclude from version control
├── README.md                  # This project overview
└── LICENSE                    # MIT License
```

---

## Data Generation Logic

Each column was created using rule-based logic grounded in SUNY and national trends. Examples:

- `first_generation_status` is more likely among students with low EFC and Pell eligibility.
- `cumulative_gpa` is influenced by academic standing, early alerts, and engagement markers like tutoring or advising.
- `housing_status` relates to residency, income level, and age.
- `assistantship_type` is shaped by degree type (e.g., TA for humanities PhDs, RA for STEM PhDs).
- `ABD_status` is TRUE for PhD students who passed their proposal but have not defended their dissertation.

For a complete explanation of each column and the logic behind its generation, see the [Undergraduate Data Dictionary](docs/metricon_undergraduate_data_dictionary.md) and [Graduate Data Dictionary](docs/metricon_graduate_data_dictionary.md).

---

## Disclaimer

All data is **synthetically generated** for educational, research, and demonstration purposes. No real student data is used or referenced.
