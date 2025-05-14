# H4_data-visualization-exploratory-analysis

This project focuses on applying data visualization techniques and exploratory data analysis methods to extract meaningful insights from datasets, with a special emphasis on using visualization libraries to analyze and interpret relationships in data.

## Project Overview

This project demonstrates how proper data visualization transforms raw data into actionable insights. Using the "tips" dataset as a primary case study, the analysis explores relationships between variables such as total bill amount, tips, party size, time of day, and other factors that influence tipping behavior. Through various visualization techniques, hidden patterns and correlations are revealed and analyzed.

## Dataset Description

The primary dataset used is the "tips" dataset, which contains information about:

- **total_bill**: Total bill amount
- **tip**: Tip amount given by the customer
- **sex**: Gender of the bill payer
- **smoker**: Whether the party included smokers (Yes/No)
- **day**: Day of the week
- **time**: Time of day (Lunch/Dinner)
- **size**: Number of people in the party

This practical dataset allows for exploration of various visualization techniques to answer questions about consumer behavior and tipping patterns.

## Core Files

- `Hafta_4_Odev.ipynb`: **Main assignment notebook** containing:
  - Complete implementation of various visualization techniques
  - Relationship analysis using scatter plots
  - Distribution analysis with box plots
  - Categorical comparisons using bar plots
  - Time-series visualizations
  - Correlation analysis with heatmaps

- `Hafta_4_Case_Çözümü.ipynb`: **Case study solution** providing:
  - Practical implementation of visualization techniques
  - Step-by-step analysis of relationships in the tips dataset
  - Multi-variable visualization approaches

- Supporting files:
  - `Odev.txt`: Assignment requirements and tasks
  - `f.docx`: Additional documentation

## Key Visualization Techniques Demonstrated

### 1. Relationship Analysis
```python
# Scatter plot to show relationship between total bill and tip
sns.scatterplot(x="total_bill", y="tip", data=df, hue="smoker")
plt.title("Relationship Between Total Bill and Tip")
plt.xlabel("Total Bill")
plt.ylabel("Tip")
```

### 2. Distribution Analysis
```python
# Box plot to analyze distribution of bills by day
sns.boxplot(x="day", y="total_bill", data=df)
plt.title("Total Bill Distribution by Day")
```

### 3. Categorical Comparisons
```python
# Creating a tip percentage column
df['tip_rate'] = (df['tip'] / df['total_bill']) * 100

# Bar plot for average tip rate by table size
sns.barplot(x="size", y="tip_rate", data=df)
plt.title("Average Tip Rate by Table Size")
```

### 4. Correlation Visualization
```python
# Creating a correlation heatmap
correlation = df[['total_bill', 'tip', 'size']].corr()
sns.heatmap(correlation, annot=True, cmap='coolwarm')
plt.title("Correlation Between Variables")
```

## Key Insights

The analysis reveals several important patterns:
- There is a positive correlation between total bill amount and tip amount
- Tipping behavior varies significantly by day of the week
- Table size affects tip rate, with certain group sizes showing more generous tipping
- Time of day (lunch vs. dinner) impacts tipping patterns
- Correlation analysis shows the strength of relationships between numerical variables

## Technical Challenges

- **Data Cleaning**: Handling missing values and outliers before visualization
- **Visual Encoding**: Selecting appropriate visual elements to represent different data types
- **Plot Customization**: Enhancing readability and interpretability of visualizations
- **Multi-variable Analysis**: Effectively showing relationships between multiple variables simultaneously

## Libraries Used

- **Matplotlib**: For creating fundamental visualizations
- **Seaborn**: For advanced statistical visualizations
- **Pandas**: For data manipulation and preprocessing
- **NumPy**: For numerical operations

## Best Practices Implemented

- Selection of appropriate chart types based on data characteristics
- Consistent color schemes and styling for visual coherence
- Clear labeling of axes, titles, and legends
- Use of color and size to encode additional dimensions of data
- Balancing information density with visual clarity

This project demonstrates how visualization techniques can transform raw data into actionable insights, a critical skill in data analysis, machine learning, and business intelligence. 