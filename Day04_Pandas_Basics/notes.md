# Day 4: Pandas Basics 🐼

## ✅ Concepts Covered

| Concept            | What it Does                                           |
|--------------------|--------------------------------------------------------|
| Series             | One-dimensional data (like a column)                   |
| DataFrame          | Two-dimensional data (rows + columns)                  |
| read_csv()         | Read data from CSV files                               |
| head() / tail()    | Peek at the first/last rows                            |
| info() / describe()| Get data types, nulls, stats summary                   |
| .loc[] / .iloc[]   | Indexing by label or by position                       |
| Conditionals       | Filter rows based on logic                             |
| Add/Drop Columns   | Modify your data                                       |
| Rename / Sort      | Clean and organize your data                           |

---

## 📘 Detailed Notes

### 1. Series and DataFrame

```python
import pandas as pd

# Creating a Series
s = pd.Series([10, 20, 30])
print("Series:\n", s)

# Creating a DataFrame
data = {
    "Name": ["Atharva", "Nihal", "Reva"],
    "Age": [21, 22, 23],
    "City": ["Pune", "Mumbai", "Delhi"]
}
df = pd.DataFrame(data)
print("\nDataFrame:\n", df)

2. Reading CSV
df.to_csv("sample.csv", index=False)
print("✅ CSV saved!")

df = pd.read_csv("sample.csv")
print("📄 Loaded CSV:\n", df.head())

3. head() and tail()
print("🔼 First 2 rows:\n", df.head(2))
print("🔽 Last 2 rows:\n", df.tail(2))

4. info() and describe()
print("ℹ️ Info:\n")
print(df.info())

print("\n📊 Describe:\n", df.describe())

5. .loc[] and .iloc[]
# .loc uses labels
print("🔍 .loc for row 0:\n", df.loc[0])

# .iloc uses index position
print("🔍 .iloc for row 1:\n", df.iloc[1])

6. Conditional Filtering
# Get all rows where Age > 21
print("🧠 Rows where Age > 21:\n", df[df["Age"] > 21])

7. Add / Drop Columns
# Add a new column
df["Gender"] = ["M", "M", "F"]
print("➕ Added Gender:\n", df)

# Drop a column
df = df.drop("City", axis=1)
print("➖ Dropped City:\n", df)

8. Rename and Sort
# Rename column
df = df.rename(columns={"Name": "Full_Name"})
print("✏️ Renamed:\n", df)

# Sort by Age
df = df.sort_values(by="Age", ascending=False)
print("⬇️ Sorted by Age:\n", df)

🧠 Summary
Pandas Basics helps you:

Load and inspect your data.

Select and filter rows/columns.

Modify, clean, and export data easily.

