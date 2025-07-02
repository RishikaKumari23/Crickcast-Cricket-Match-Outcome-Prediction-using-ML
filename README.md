# 🏏 CrickCast – Cricket Match Outcome Prediction

A machine learning model that predicts cricket match outcomes using match-level data, team strength, toss results, and head-to-head stats. Built using LightGBM and hyperparameter tuning.

## 📌 Features
- Predicts outcome using 8+ engineered cricket-relevant features.
- Uses LightGBM classifier with `GridSearchCV` tuning.
- Achieves 65.1% test accuracy on historical IPL match data.
- Domain-informed features: venue advantage, recent win %, batting strength, toss influence, etc.

## 📁 Project Structure
crickcast
├── data
│   ├── matches.csv                        # Match-level data with teams, toss, venue, result
│   └── most_runs_average_strikerate.csv   # Player performance stats (average, strike rate)
├── Crickcast_Prediction.ipynb             # Main Colab notebook with full ML pipeline
├── requirements.txt                       # List of required Python packages
├── README.md                              # Project overview and documentation


## 🧪 How to Run

1. Clone the repo  
   `git clone https://github.com/yourusername/crickcast.git`

2. Open `Crickcast_Prediction.ipynb` in Google Colab or Jupyter

3. Upload the `data/` folder or update paths if needed

## 🔧 Requirements

- pandas
- lightgbm
- matplotlib
- scikit-learn

## 🔧 Features Engineered

| Feature                  | Description                                           |
|--------------------------|-------------------------------------------------------|
| `toss_win_match_win`     | Whether toss winner also won the match                |
| `team1_home`             | Whether team1 was playing at home                     |
| `team1_recent_win_pct`   | Recent win % of team1 in last 5 games                 |
| `team2_recent_win_pct`   | Same for team2                                        |
| `team1_batting_strength` | Avg batting score of top 5 players in team1           |
| `team2_batting_strength` | Same for team2                                        |
| `team1_win_ratio`        | Historical head-to-head win ratio vs team2            |

## 📊 Model and Evaluation

- **Model**: LightGBM Classifier
- **Tuning**: GridSearchCV on `num_leaves`, `max_depth`, `learning_rate`, `n_estimators`
- **Metric**: Accuracy on 20% test split
- **Final Accuracy**: **65.10%**
  
## 📢 Acknowledgments

1. Data from Kaggle and ESPN Cricinfo archives
2. LightGBM by Microsoft
3. Project inspired by real-world sports analytics


