# 🏏 IPL Match Analysis with Python

This project provides a comprehensive analysis of the Indian Premier League (IPL) using Python and pandas. Using historical match data, it uncovers insights into team performance, win patterns, toss outcomes, and more.

---

## 📁 Dataset

**File**: `IPL_matches.csv`

**Columns include:**

* `team1`, `team2`: Competing teams
* `winner`: Match winner
* `win_by_runs`, `win_by_wickets`: Victory margin
* `toss_winner`, `toss_decision`: Toss outcome
* `venue`, `city`, `season`
* `player_of_match`, `umpires`

---

## 🧪 Technologies Used

* **Python**
* **Jupyter Notebook**
* **pandas**, **matplotlib**, **seaborn**

---

## 📊 Key Visualizations

### 1. Most Successful Teams

```python
import seaborn as sns
import matplotlib.pyplot as plt

top_teams = ipl_df['winner'].value_counts().head(10)
sns.barplot(y=top_teams.index, x=top_teams.values, palette='viridis')
plt.title('Top 10 Most Successful IPL Teams')
plt.xlabel('Wins')
plt.ylabel('Team')
plt.show()
```

### 2. Toss Decision Analysis

```python
sns.countplot(data=ipl_df, x='toss_decision', hue='season')
plt.title('Toss Decisions Over the Seasons')
plt.xticks(rotation=45)
plt.show()
```

### 3. Win by Runs vs Wickets

```python
fig, axs = plt.subplots(1, 2, figsize=(12,5))
sns.histplot(ipl_df['win_by_runs'], kde=True, ax=axs[0], color='blue')
axs[0].set_title('Distribution of Wins by Runs')

sns.histplot(ipl_df['win_by_wickets'], kde=True, ax=axs[1], color='green')
axs[1].set_title('Distribution of Wins by Wickets')

plt.tight_layout()
plt.show()
```

---

## 🔍 Insights

* **Toss Advantage**: Teams winning the toss often chose to field, especially in recent seasons.
* **Dominant Teams**: \[Fill in the most successful team based on your analysis].
* **Close Matches**: Many matches were won by narrow margins, adding to the league’s excitement.

---

## ▶️ How to Run

1. Clone the repo:

   ```bash
   git clone https://github.com/your-username/IPL-Analysis.git
   ```
2. Open `IPL_data.ipynb` in Jupyter Notebook.
3. Run cells to explore and visualize the data.

---

## 🙌 Contribution

Feel free to fork the project and enhance it—add new visuals, use different machine learning models, or update the dataset.

---

## 📢 Contact

For questions or suggestions, reach out via \[your email here].
