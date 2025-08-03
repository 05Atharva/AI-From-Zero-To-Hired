# 📊 Day 6: Matplotlib - Data Visualization

## ✅ Topics Covered
- Line Plot
- Bar Chart
- Scatter Plot
- Histogram
- Subplots
- Customizations (labels, title, legend, color)

---

## 1. Importing

import matplotlib.pyplot as plt
import numpy as np

## 2. Line Plot

x = np.arange(0, 10)
y = np.sin(x)
plt.plot(x, y)
plt.title("Line Plot of sin(x)")
plt.xlabel("x")
plt.ylabel("sin(x)")
plt.grid(True)
plt.show()

## 3. Bar Plot

categories = ['Python', 'C++', 'Java']
students = [60, 45, 30]
plt.bar(categories, students, color='orange')
plt.title("Bar Plot: Language Popularity")
plt.ylabel("Number of Students")
plt.show()

## 4. Scatter Plot

x = np.random.rand(50)
y = np.random.rand(50)
plt.scatter(x, y, color='green')
plt.title("Random Scatter Plot")
plt.xlabel("X")
plt.ylabel("Y")
plt.show()

## 5. Histogram

data = np.random.randn(1000)
plt.hist(data, bins=30, color='purple')
plt.title("Histogram of Normal Distribution")
plt.xlabel("Value")
plt.ylabel("Frequency")
plt.show()

## 6. Subplots

x = np.linspace(0, 10, 100)
plt.subplot(1, 2, 1)
plt.plot(x, np.sin(x), 'b--')
plt.title("Sine")

plt.subplot(1, 2, 2)
plt.plot(x, np.cos(x), 'r-.')
plt.title("Cosine")

plt.tight_layout()
plt.show()

## 7. Custom Plot

x = np.linspace(0, 10, 100)
y = np.sin(x)
plt.plot(x, y, linestyle='-.', color='red', label='sin(x)')
plt.title("Customized Plot")
plt.xlabel("Angle in rad")
plt.ylabel("sin value")
plt.legend()
plt.grid(True)
plt.show()

## 🧪 Optional Challenges
✅ Horizontal bar chart (Sports)

✅ Plot sin, cos, tan on same graph with legends

✅ Scatter plot with 100 color-coded dots

## 🚀 Summary
Matplotlib helps you visualize your data clearly with line plots, bar charts, scatter plots, histograms, and more. Customization lets you make your plots presentation-ready for reports and dashboards.