- 👋 Hi, I’m @Haya-S2046
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

<!---
Haya-S2046/Haya-S2046 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->import pandas as pd

import numpy as np

import matplotlib.pyplot as plt

import seaborn as sns

# Load the dataset

data = pd.read_csv("pathname")

# Display the first few rows of the dataset

print(data.head())

# Get information about the dataset

print(data.info())

# Summary statistics

print(data.describe())

# Distribution of wine quality

sns.countplot(data['quality'])

plt.title(" Wine Quality data set")

plt.show()

# Box plots for selected features by wine quality

features = ['alcohol', 'volatile acidity', 'citric acid', 'residual sugar']

for feature in features:

    plt.figure(figsize=(8, 6))

    sns.boxplot(x='quality', y=feature, data=data)

    plt.title(f'{feature} by Wine Quality')

    plt.show()

# Pair plot of selected features

sns.pairplot(data, vars=['alcohol', 'volatile acidity', 'citric acid', 'residual sugar'], hue='quality', diag_kind='kde')

plt.suptitle("Pair Plot of Selected Features")

plt.show()

# Correlation heatmap

corr_matrix = data.corr()

plt.figure(figsize=(10, 8))

sns.heatmap(corr_matrix, annot=True, cmap="coolwarm", fmt=".2f")

plt.title("Correlation Heatmap")

plt.show()

# Histograms of selected features

features = ['alcohol', 'volatile acidity', 'citric acid', 'residual sugar']

for feature in features:

    plt.figure(figsize=(6, 4))

    sns.histplot(data[feature], kde=True, bins=20)

    plt.title(f"Distribution of {feature}")

    plt.show()




