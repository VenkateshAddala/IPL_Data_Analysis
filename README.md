# IPL_Data_Analysis
# IPL Data Analysis and Predicting Match Outcomes

## Executive Summary
Cricket is more than just a sport in India—it's a cultural phenomenon with the IPL at its core. This analysis (2008–2024) uncovers team and player trends and uses machine learning to predict match winners before the game starts.

## Table of Contents
- [Executive Summary](#executive-summary)
- [Dataset & Preprocessing](#dataset--preprocessing)
- [Exploratory Data Analysis](#exploratory-data-analysis)
  - [IPL Titles by Team](#ipl-titles-by-team)
  - [Head-to-Head Wins](#head-to-head-wins)
  - [Top 10 Batsmen by Total Runs](#top-10-batsmen-by-total-runs)
  - [Century-Scorers (2008–2024)](#century-scorers-2008–2024)
  - [Top Run Scorer Each Season](#top-run-scorer-each-season)
  - [Top Wicket-Taker Each Season](#top-wicket-taker-each-season)
  - [Venue Statistics Treemap](#venue-statistics-treemap)
  - [Geographic Venue Map](#geographic-venue-map)
- [Feature Engineering](#feature-engineering)
- [Modeling & Evaluation](#modeling--evaluation)
  - [Model Performance Comparison](#model-performance-comparison)
  - [ROC Curves](#roc-curves)
- [Future Work](#future-work)
- [License](#license)
- [Contact](#contact)

---

## Dataset & Preprocessing
- **Source:** Kaggle's IPL Complete Dataset (Matches.csv & Deliveries.csv)
- **Filters:** Removed super‑overs and incomplete games; merged ball‑by‑ball data with match metadata; cleaned missing/invalid entries.
- **Engineered Features:** Toss decisions, batting/bowling metrics, historical win percentages (overall/venue/head‑to‑head), star player flags, home advantage, depth metrics (top performers averages).

## Exploratory Data Analysis

### IPL Titles by Team
![IPL Titles by Team](images/plots/ipl_titles_by_team.png)
*Titles won by each franchise (2008–2024)*

### Head-to-Head Wins
![Head-to-Head Wins](images/plots/head_to_head_wins.png)
*Match win counts between each pair of teams*

### Top 10 Batsmen by Total Runs
![Top 10 Batsmen by Total Runs](images/plots/top_10_batsmen_by_runs.png)
*Overall run totals for leading batsmen*

### Century-Scorers (2008–2024)
![Century-Scorers (2008–2024)](images/plots/top_century_scorers.png)
*Number of centuries scored by top players*

### Top Run Scorer Each Season
![Top Run Scorer Each Season](images/plots/top_run_scorer_each_season.png)
*Orange Cap holders with total runs per season*

### Top Wicket-Taker Each Season
![Top Wicket-Taker Each Season](images/plots/top_wicket_taker_each_season.png)
*Purple Cap holders with wickets per season*

### Venue Statistics Treemap
![Venue Statistics Treemap](images/plots/venue_statistics_treemap.png)
*Tiled view of matches played and average scores by venue*

### Geographic Venue Map
![Geographic Venue Map](images/plots/venues_geographic_map.png)
*Map of IPL venues sized by total matches hosted*

## Feature Engineering
A comprehensive set of predictors capturing pre‑game toss strategy, team performance metrics, historical trends, and contextual factors like home advantage and star players.

## Modeling & Evaluation

### Model Performance Comparison
![Model Performance Comparison](images/plots/model_performance_comparison.png)
*Test-set accuracies: XGBoost (0.745), Gradient Boosting (0.694), Random Forest (0.597), Logistic Regression (0.449)*

### ROC Curves
![ROC Curves](images/plots/roc_curves.png)
*Micro-average ROC curves with AUCs: LogisticRegression (0.87), RandomForest (0.95), GradientBoosting (0.97), XGBoost (0.98)*

## Future Work
- Integrate real-time variables: weather conditions, player availability
- Develop an interactive dashboard for live predictions
- Experiment with ensemble and deep learning classifiers

## License
Released under the MIT License.

## Contact
- **Author:** Venkateswara Rao Addala
- **Email:** venkatesh.addala@example.com
- **GitHub:** [VenkateshAddala](https://github.com/VenkateshAddala)

