## 1. Importing Seaborn & Dataset
'''python

import seaborn as sns
import matplotlib.pyplot as plt

## Load sample dataset from seaborn
'''python

df = sns.load_dataset('tips')
seaborn is imported as sns (convention).

** We also import matplotlib.pyplot to enable .show().

** sns.load_dataset('tips') loads a built-in dataset with info about restaurant bills and tips.

## 2. Histplot — Visualize Distribution of Tips
'''python

sns.histplot(data=df, x='tip', kde=True, bins=20, color='skyblue')
plt.title("Distribution of Tips")
plt.xlabel("Tip Amount")
plt.ylabel("Frequency")
plt.show()

# Explanation:

data=df: using the tips dataset.

x='tip': plot the 'tip' column.

kde=True: overlay a smooth density curve.

bins=20: divide data into 20 bins (intervals).

color='skyblue': custom color.

plt.title, xlabel, ylabel: labeling for clarity.

## 3. Boxplot — Tip Amount by Gender
'''python

sns.boxplot(data=df, x='sex', y='tip', palette='Set2')
plt.title("Boxplot of Tips by Gender")
plt.show()

# Explanation:

boxplot: shows median, quartiles, outliers.

x='sex': category on x-axis (Male/Female).

y='tip': numerical variable.

palette='Set2': pastel color palette.

## 4. Violin Plot — Bill Distribution by Day
'''python

sns.violinplot(data=df, x='day', y='total_bill', hue='sex', split=True)
plt.title("Violin Plot of Total Bill by Day and Gender")
plt.show()

# Explanation:

violinplot: like a boxplot + KDE (density curve).

hue='sex': divide each violin by gender.

split=True: draws both genders on same side (compare).

## 5. Pairplot — Visualize All Pairwise Relations
'''python

sns.pairplot(df, hue='sex')
plt.suptitle("Pairplot of Tips Dataset", y=1.02)
plt.show()

# Explanation:

Automatically creates scatterplots between all numerical columns.

hue='sex': color-code by gender.

suptitle: title for full figure.

## 6. Heatmap — Correlation Matrix
'''python

corr = df.corr(numeric_only=True)
sns.heatmap(corr, annot=True, cmap='coolwarm', fmt=".2f")
plt.title("Correlation Matrix Heatmap")
plt.show()

# Explanation:

df.corr(): compute correlation matrix of numerical columns.

annot=True: display correlation values on cells.

cmap='coolwarm': color gradient.

fmt=".2f": format numbers to 2 decimal places.

##  Optional Practice Challenges (with Ideas)
✅ Challenge 1:
Plot a catplot showing the average tip given based on time (Lunch/Dinner) and smoker status.

✅ Challenge 2:
Create a scatter plot (sns.scatterplot) of total_bill vs tip, colored by day.

✅ Challenge 3:
Draw a heatmap showing the average tip by day and gender (pivoted).


✅ Day 7 Summary:
Concept	Understood
Seaborn Setup	✅
Histplot / KDE	✅
Boxplot & Violinplot	✅
Pairplot	✅
Heatmap	✅