# Assessment Item Difficulty Study

**Pathway:** Generative AI & Data Science (Beginner Stag)  
**Capstone Project:** Assessment Item Difficulty Study 

## Overview
Teachers often review overall exam averages without knowing which individual questions are poorly worded, overly easy, too difficult, or misleading. 

## Project Files & Deliverables
- `generate_dataset.py` — Generates synthetic student-item response data (`raw_quiz_responses.csv`) with realistic missing values, duplicates, and edge-case question.
- `item_difficulty_study.ipynb` — Main Jupyter Notebook covering data cleaning, difficulty and discrimination calculations, visualizations, and the rule-based item review assistance.
- `item_difficulty_study.html` — Exported HTML version of the executed notebook.
- `data/raw_quiz_responses.csv` — Raw synthetic response dataset.
- `data/cleaned_quiz_responses.csv` — Deduplicated and validated dataset produced during cleaning.
- `outputs/item_review_report.csv` — Computed item metrics, review flags, notes, and uncertainty details.
- `outputs/difficulty_vs_discrimination.png` — Scatter/quadrant chart comparing item difficulty and flagged item.
- `outputs/item_difficulty_overview.png` — Ranked horizontal bar chart of item difficulty aan_39](end_span).
- Presentation PDF: Assessment_Item_Difficulty_Study.pdf
- Demo Video (3–5 mins): `[Add demo.span_Generate the synthetic dataset
## Generate the synthetic dataset
python generate_dataset.py

## to run
Open item_difficulty_study.ipynb in jupyter, click restart and run all, and verify all cell run cleanly.

## Data Source & Cleaning
​Data Privacy: All records are synthetic/mock data generated locally—no real student personal data or API keys are included.  
​Cleaning Steps: Duplicate (student_id, question_id) entries are removed, blank/missing responses are tracked separately from attempted items, and score fields are validated before saving data/cleaned_quiz_responses.csv.  


## Methodology, Findings & Limitations
​Metrics: Item difficulty (p_attempted and p_total), upper-lower discrimination index (discrimination_D), and corrected item-total correlation (item_total_corr) are computed and visualized in outputs/.  

​Key Takeaways: Flagged items (such as very easy items, very hard items, high-omission items, or items with low/negative discrimination) are surfaced for teacher inspection rather than automatic removal.  

​Limitations: Multiple-choice guessing baselines, small subgroup sizes, and extreme item difficulty can constrain metric behavior, so statistical flags require human review.


## AI-Use Reflection
​What I Built Independently: Data generation, cleaning logic, psychometric calculations, visualizations, and verification checks.  
​How AI Assisted: Used AI guidance to structure the workflow, refine explanations, and draft code and documentation.  
​How I Verified Results: Re-ran the full notebook end-to-end, checked generated files in data/ and outputs/, and inspected raw response/option distributions on flagged item
