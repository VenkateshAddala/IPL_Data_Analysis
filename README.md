# Cricket Data Analysis and Match Outcome Prediction

## Introduction
This project analyzes historical IPL match data (2008–2024) to uncover insights at team, player, and venue levels, and leverages machine learning models to predict match outcomes before play begins.

## Exploratory Data Analysis (EDA)
Comprehensive EDA was performed to understand trends and distributions across matches, players, and venues, utilizing visualizations such as bar charts, heat maps, treemaps, and geographic maps.

## Team-wise Analysis
- **Titles by Franchise**: Ranked franchises by total IPL wins from 2008–2024
  ![image](https://github.com/user-attachments/assets/a757549d-f981-4d48-a09e-3c943240d1ce)
- **Head-to-Head Records**: Visualized win counts between every pair of teams.
  <img width="485" alt="image" src="https://github.com/user-attachments/assets/05361135-ab6d-440b-9c29-08ea5ba8aae7" />

- **Win Percentage**: Compared overall win rates to identify the most consistent performers.
  <img width="401" alt="image" src="https://github.com/user-attachments/assets/3b2a4139-477b-4a55-b5b8-1632024d296c" />


## Player-wise Analysis
- **Top Batsmen by Runs**: Highlighted the leading run-scorers and strike-rate leaders. 
 ![image](https://github.com/user-attachments/assets/9f3100a0-b97b-4a10-ad61-db6c05a3c86b)
 ![image](https://github.com/user-attachments/assets/05385a12-7596-46b9-9093-02ee0a754953)


- **Century and Fifty Counts**: Counted 50+ and 100+ scores for top contributors.
   ![image](https://github.com/user-attachments/assets/503ba84b-6cc0-41d2-970c-d4485d11a391)
   ![image](https://github.com/user-attachments/assets/ccf45431-4fcf-434f-aba9-528c37c9e27c)


- **Seasonal Orange Cap Holders**: Tracked top run-scorer each season.
   ![image](https://github.com/user-attachments/assets/25589708-406c-4ac0-8fd6-8a33bd8c5ac6)

- **Seasonal Purple Cap Holders**: Tracked top wicket-taker each season.
<img width="468" alt="image" src="https://github.com/user-attachments/assets/c44cf476-dc1a-411d-bee3-489ff659fb12" />

## Venue-wise Analysis
- **Matches by Venue**: Mapped total matches hosted per stadium.
  <img width="468" alt="image" src="https://github.com/user-attachments/assets/02c72f0a-77ee-4de3-b7d0-b1cd4d81534c" />

   

- **Venue Performance Treemap**: Showed matches count, average runs, and high/low scores per venue.
![image](https://github.com/user-attachments/assets/f53d2bf0-6958-438a-9472-042a0cf83e52)


## ML Model Evaluation and Results
Benchmarked four classifiers:
1. **Logistic Regression** – Test accuracy: 44.9%
2. **Random Forest** – Test accuracy: 59.7%
3. **Gradient Boosting** – Test accuracy: 69.4%
4. **XGBoost** – Test accuracy: 74.5%

    ![image](https://github.com/user-attachments/assets/aecdeada-8f1f-4736-b6b4-71ff0c44e31f)
   ![image](https://github.com/user-attachments/assets/f292bfcb-b723-4125-b752-025f5cc18171)




ROC AUC scores confirmed XGBoost as the top performer.
<img width="353" alt="image" src="https://github.com/user-attachments/assets/417b7913-6371-41a8-898f-e6a73e68160d" />



