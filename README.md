# IPL Data Analysis and Match Outcome Prediction

![IPL Logo](https://upload.wikimedia.org/wikipedia/en/thumb/8/84/Indian_Premier_League_Official_Logo.svg/1200px-Indian_Premier_League_Official_Logo.svg.png)

## Project Overview

**Author:** Venkateswara Rao Addala

Cricket isn't just a sport in India—it's a religion with the IPL sitting at its heart. It has the largest cricket fan base in the world, and IPL franchises, sponsors, and enthusiasts constantly seek data-driven insights. This project analyzes historical IPL match and player statistics (2008-2024) to:

- Help team management and auction strategists bid smartly for players each season
- Guide sponsors to identify and support high-impact players and teams based on performance metrics
- Enable bettors and analysts to forecast match outcomes with greater confidence

## Data Information

### Sources
- **Matches.csv** - Contains match-level data including teams, venue, toss information, and results
- **Deliveries.csv** - Ball-by-ball data with detailed information about each delivery bowled

### Processing Steps
- Focused only on completed matches (filtered out super-overs and no-result matches)
- Merged ball-by-ball data with match details and cleaned missing/invalid entries
- Created comprehensive statistical profiles for teams, players, and venues

## Methodology

The analysis followed a structured approach:

1. **Data Collection & Cleaning**: Gathered IPL match dataset (2008-24) from Kaggle and filtered out incomplete games to focus on clear results
2. **Feature Engineering**: Created practical features for each match record including:
   - Toss information (winner and decision)
   - Team performance metrics (runs, run rates, bowling economy)
   - Historical win percentages (overall, venue-specific, head-to-head)
   - Player form indicators
   - Home ground advantage
3. **Model Training**: Split dataset into training and test portions, used a pipeline to standardize numerical values and encoded categorical information
4. **Model Evaluation**: Assessed performance using cross-validation, test-set accuracy, feature importance, confusion matrices, and ROC curves


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
 ![image](https://github.com/user-attachments/assets/ddc583ae-b1b0-4bac-b5a2-3b431c48c05d)

- **Top Bowlers by Wickets and Economy**: Highlighted the leading Wicket-Takers and Economy leaders.
   ![image](https://github.com/user-attachments/assets/ccca52be-f84b-4776-88d5-36fd95401a27)
   ![image](https://github.com/user-attachments/assets/e645083a-cbf8-4312-8f99-e126373b1a81)

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


## ROC AUC scores confirmed XGBoost as the top performer.
<img width="353" alt="image" src="https://github.com/user-attachments/assets/4bd60fad-e11f-4b34-9230-8c26338c4800" />

## Feature Engineering Details

The prediction models used a mix of categorical and numerical features:

### Categorical Features
- `toss_winner` and `toss_decision` to capture pre-game strategic choices

### Numerical Features
- **Team Performance**: team1_runs, team2_run_rate, team1_econ, etc.
- **Historical Form**: team1_win_pct, team2_venue_win_pct, team1_vs_team2_pct (head-to-head)
- **Player Quality**: team1_top_player flags if a star "Player of the Match" is on the side
- **Contextual Factors**: team1_home marks home-ground advantage
- **Depth Metrics**: team1_bowler_str averages the top three bowlers' economies; team2_bat_form averages the top five run-scorers' tallies

## Conclusion

The analysis successfully predicted IPL match winners with XGBoost achieving 74.5% accuracy on test data. By combining match statistics, team history, and player performance metrics, this project created a reliable forecasting system.

### Next Steps
Future enhancements could include:
- Fine-tuning the models to improve prediction accuracy
- Adding real-time data like weather and pitch conditions
- Including player availability updates and team news
- Developing a user-friendly dashboard for live predictions


---
## Usage Guide
1. **Clone the repository**:
   ```bash
   git clone https://github.com/username/repo-name.git
   cd repo-name
2. **Install dependencies**:
    ```bash
   pip install <libraries>
3. **Download and prepare source data**:
   Unzip datasets.zip into data/, ensuring the following files are present:
   ```bash
   matches.csv
   deliveries.csv
   india_states_geo.json
  If you place them elsewhere, update the file paths in notebooks/IPL_EDA_Final.ipynb and ML_DMM_II.ipynb configuration\n
4. **Clone the repository**:
   ```bash
   git clone https://github.com/username/repo-name.git
   cd repo-name
5. **Install dependencies**:
   ```bash
   pip install <libraries>
6. **Download and prepare source data**:
   Unzip datasets.zip into data/, ensuring the following files are present:
   ```bash
   matches.csv
   deliveries.csv
   india_states_geo.json
  If you place them elsewhere, update the file paths in notebooks/IPL_EDA_Final.ipynb and ML_DMM_II.ipynb configuration.
7.**Launch the Notebooks**:
   ```bash
   jupyter notebook notebooks/IPL_EDA_Final.ipynb
   jupyter notebook notebooks/ML_DMM_II.ipynb
8. **View results and plots**

## References

IPL Complete Dataset (2008–2024) – Patrick B. Kumar, Kaggle
Scikit-Learn: Machine Learning in Python
Pandas: Python Data Analysis Library – Wes McKinney
Matplotlib: Visualization with Python – John D. Hunter

Contact Information
For questions or collaboration opportunities, please contact:

Venkateswara Rao Addala
LinkedIn Profile <https://www.linkedin.com/in/venkatesh48/>
Email <venkatesh.addala98@gmail.com>

