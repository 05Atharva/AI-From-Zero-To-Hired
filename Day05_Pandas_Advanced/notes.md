# 📘 Day 5: Pandas Advanced

## merge()
- Combines rows from different DataFrames using keys
- SQL-style joins: `inner`, `left`, `right`, `outer`


merged_df = pd.merge(df1, df2, on='ID', how='inner')

## concat()
-Stack DataFrames vertically or horizontally

-Default: vertical (axis=0)

concat_df = pd.concat([df1, df2])

## groupby()
-Group data and apply aggregations like mean, sum, etc.

grouped = df.groupby('Department')['Marks'].mean()

## Pivot Table
-Summarize data in matrix form

-Use pivot_table() for grouped summary

df.pivot_table(index='Name', columns='Subject', values='Score', aggfunc='mean')

## Missing Data Handling
-isnull() to check

-fillna() to replace

-dropna() to remove

df.fillna("Unknown")
df.dropna()

## Data Type Conversion
-Convert data types for cleaning
df['Age'] = df['Age'].astype(int)
df['JoinDate'] = pd.to_datetime(df['JoinDate'])