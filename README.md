# EG DIB Validation

## Dataset: EG DIB Main Student Data

This dataset comes from IDinsight's three-year impact evaluation of the Educate Girls Development Impact Bond (EG DIB), a clustered randomized controlled trial conducted across 332 schools in 282 rural villages in Bhilwara District, Rajasthan, India (Mandalgarh, Bijoliya, and Jahajpur blocks). The evaluation compared students in treatment villages (where Educate Girls operated) against students in matched control villages.

The dataset (`data/raw/EG DIB_Main Student Data.dta`) contains 6,837 students who were assessed at baseline, with ASER learning scores in Hindi, Math, and English recorded at each assessment round.

### Cohorts and Assessment Timing

IDinsight tracked five grade cohorts, each labeled by the student's grade at Baseline (Year 1). Cohorts are referred to throughout the evaluation report using a "Y1" suffix convention — for example, "Grade 3_Y1" refers to students who were in Grade 3 at Baseline, progressed to Grade 4 by Year 2 Endline, and Grade 5 by Year 3 Endline.

| Cohort label | Grade at Baseline | Grade at Y1 Endline | Grade at Y2 Endline | Grade at Y3 Endline | Years exposed to EG program |
| ------------ | ----------------- | ------------------- | ------------------- | ------------------- | --------------------------- |
| Grade 1_Y1   | 1                 | 1*                  | 2*                  | 3                   | 1                           |
| Grade 2_Y1   | 2                 | 2*                  | 3                   | 4                   | 2                           |
| Grade 3_Y1   | 3                 | 3                   | 4                   | 5                   | 3                           |
| Grade 4_Y1   | 4                 | 4                   | 5                   | 6*                  | 2                           |
| Grade 5_Y1   | 5                 | 5                   | 6*                  | 7*                  | 1                           |

Cells with an asterisk indicate that the cohort was not assessed in that round.

EG's program targeted students in Grades 3–5, so cohort exposure to EG programming varies: Grade 3_Y1 students were the only cohort exposed for all three years.

Assessment dates:

| Round          | Variable suffix in data | Date                |
| -------------- | ----------------------- | ------------------- |
| Baseline       | `_bl`                   | September 2015      |
| Year 1 Endline | `_ely1`                 | February 2016       |
| Year 2 Endline | `_ely2`                 | February 2017       |
| Year 3 Endline | `_ely3`                 | February 2–28, 2018 |

Not all students were assessed at every round. Of the 6,837 students assessed at Baseline, 4,069 (60%) were assessed at the Year 1 Endline, 3,871 (57%) at Year 2, and 3,571 (52%) at Year 3. The `assessed_ely1`, `assessed_ely2`, and `assessed_ely3` indicator variables in the data flag which students were assessed at each round and 

### ASER Score Coding

ASER assessments measure the highest competency level a student can demonstrate. Each subject is scored on an ordered scale; a higher value always indicates a higher level of reading or numeracy. The `_diff_*` variables record the change in level from Baseline to a given endline round.

**Hindi** (`hindi_bl`, `hindi_ely1`, `hindi_ely2`, `hindi_ely3`) — 6 levels:

| Value | Label |
| ----- | ----------- |
| 1 | Beginner |
| 2 | Letter |
| 3 | Word |
| 4 | Paragraph |
| 5 | Story |
| 6 | Story Plus |

**Math** (`math_bl`, `math_ely1`, `math_ely2`, `math_ely3`) — 5 levels:

| Value | Label |
| ----- | ------------- |
| 1 | Beginner |
| 2 | Numbers 1–9 |
| 3 | Numbers 10–99 |
| 4 | Subtraction |
| 5 | Division |

**English** (`english_bl`, `english_ely1`, `english_ely2`, `english_ely3`) — 5 levels:

| Value | Label |
| ----- | -------------- |
| 1 | Beginner |
| 2 | Capital letter |
| 3 | Small letter |
| 4 | Word |
| 5 | Sentence |