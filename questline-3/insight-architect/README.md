#  Insight Architect - Exploratory Data Analysis (EDA)
### Objective
Perform Exploratory Data Analysis (EDA) to discover patterns, relationships, and trends within the dataset using effective visualizations.


## Visualizations:
1. **Histogram**: Plotted the distribution of math scores to see how the overall class performed.
2. **Bar Chart**📊: Compared average math scores between students who completed the test prep course vs. those who skipped it.
3. **Box Plot**: Looked at reading scores across different parental education levels to check for score gaps and outliers.
4. **Scatter Plot**: Plotted reading scores against writing scores (split by gender) to see if doing well in one meant doing well in the other.
5. **Heatmap**: Built a correlation matrix for math, reading, and writing scores to check how closely tied the three subjects are.

---
## How Each Visualization Helps
* **Histogram**: Quickly reveals whether most students passed or failed and shows overall score distribution.
* **Bar Chart**: Directly measures if taking the prep course actually improved student results.
* **Box Plot**: Shows if higher parental education gives students a clear score advantage.
* **Scatter Plot**: Checks if strong readers are also strong writers and reveals gender trends.
* **Heatmap**: Sums up all score relationships in one grid to highlight overall academic patterns.
  
## Observations:
1. **Math Scores form a Bell Curve**: Most students scored between 60 and 70. A few struggled badly (with scores dropping near 0), which slightly pulled down the overall average.
2. **Test Prep Actually Works**: Students who finished the preparation course scored around 5–8 points higher in math on average compared to those who didn't take it.
3. **Parental Education Level Matters**: Kids whose parents hold a Bachelor's or Master's degree generally pulled higher median reading scores than those whose parents only finished high school.
4. **Reading and Writing go Hand-in-Hand**: There is a super strong linear relationship between reading and writing scores ($r > 0.90$). If a student did well in reading, they almost always did well in writing too.
5. **Subject Trends by Gender**: Female students tended to score slightly higher on average in reading and writing, while male students averaged a bit higher in math.
6. **Good in One, Usually Good in All**: All three test scores showed high positive correlations with each other, meaning overall strong academic habits carried across subjects.
