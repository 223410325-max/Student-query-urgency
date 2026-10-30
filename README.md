# Automated Urgency Classification of University Student Queries

CS316: Introduction to AI and Data Science (Term 261), Instructor: Dr. Heyfa Ammar

## Overview
Binary classifier (Urgent / Not Urgent) for university student queries, using TF-IDF features and linear models. Supports SDG 4 (Quality Education) and SDG 9 (Industry, Innovation and Infrastructure).

## Dataset
- Original: Smart University Query Classification Dataset (Kaggle, by wardabilal). Only 15 distinct query texts.
- Expanded: 165 distinct queries (15 original + 150 AI-generated, manually reviewed). Rows are marked in the `Data_Source` column.

## Files
- `University_Query_Classification_Final (1).ipynb`: full notebook (preprocessing, models, tuning, nested CV, error analysis, memory optimization)
- `university_query_train.xlsx` / `university_query_test.xlsx`: original data
- `university_query_train_expanded.xlsx`: expanded 165-query dataset
- `requirements.txt`: dependencies

## How to run
1. `pip install -r requirements.txt`
2. Put all files in the same folder.
3. Open the notebook in Jupyter or Google Colab and run all cells.

## Methods
TF-IDF + Logistic Regression, Naive Bayes, Linear SVM, Decision Tree, and a majority baseline. 5-fold cross-validation grouped by scenario (no paraphrase leakage), with GridSearchCV and nested CV.

## Results (grouped CV)
- Linear SVM: 96.49% accuracy
- Logistic Regression (final model): 95.46% accuracy, 98.57% urgent recall, 95.18% urgent F1

## Authors
Maha Alhayek 223410325
Baria Alsaikhan 223410397
Sebastian Nabeel 2234410349 

## Use of AI
150 of 165 queries were AI-generated and manually reviewed. AI assistance was also used for code suggestions. See the report for details.
