# Zomato Data Analysis Using Python
## Project Overview
This project performs exploratory data analysis (EDA) on a Zomato restaurant dataset using Python. It utilizes various Python libraries for data manipulation, visualization, and statistical analysis to uncover insights into restaurant preferences, pricing trends, and online ordering habits.

# Tech Stack
Python

# Libraries Used:

NumPy: Efficient numerical operations

Pandas: Data manipulation and analysis

Matplotlib: Data visualization

Seaborn: Statistical graphics

# Project Tasks
1. Data Import and Preprocessing

2. Load data using Pandas

3. Check for null values and data types

4. Convert 'rate' column to float for numerical analysis

5. Clean and format columns as needed

# Exploratory Data Analysis

A. Analyze:

1. Online vs Offline order availability

2. Most preferred restaurant types

3. Average pricing trends for couples dining out

4. Highest-rated restaurants

5. Ratings distribution

6. Popular price ranges

7. Correlation between online ordering and restaurant ratings

B. Data Visualization

1. Count plots

2. Histograms

3. Boxplots

4. Line plots

6. Heatmaps

# Key Questions Addressed
1. Do more restaurants offer online delivery or offline services?

2. Which types of restaurants are most favored by customers?

3. What price range is preferred by couples for dinner?

4. Which restaurants received the highest votes?

5. How do online and offline orders affect restaurant ratings?

# Key Insights
A. Majority of restaurants fall under the dining category.

B. Dining restaurants tend to receive more offline orders, while cafes see more online orders.

C. Most restaurants receive ratings between 3.5 to 4.0.

D. The approximate cost for two people is usually around ₹300.

E. Online orders typically receive higher ratings compared to offline orders.

## How to Run the Project
Install required libraries


pip install pandas numpy matplotlib seaborn
Download the dataset
(Add your dataset link or upload instructions here)

Run the analysis in a Jupyter Notebook or Google Colab

Execute the notebook step by step to view the data analysis and visualization outputs.

![image](https://github.com/user-attachments/assets/501d5dc4-44ed-490a-a95f-e1b815a9ecc2)


import pandas as pd

import numpy as np

import matplotlib.pyplot as plt

import seaborn as sns  

### Load data
dataframe = pd.read_csv("Zomato data.csv")

### Convert 'rate' column to float
def handleRate(value):

    value = str(value).split('/')
    
    return float(value[0])

dataframe['rate'] = dataframe['rate'].apply(handleRate)

### Plot ratings distribution
plt.hist(dataframe['rate'], bins=5)

plt.title('Ratings Distribution')

plt.show()
