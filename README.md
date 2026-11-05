# Task17
Overview
This project demonstrates how to filter rows and sort values in a Pandas DataFrame using Python.
Objective
Learn how to retrieve specific records from a dataset using Boolean conditions and arrange records in ascending or descending order.
Tools Used
Python
Pandas
Jupyter Notebook
Dataset
A small sample student dataset is used below. The same techniques can also be applied to datasets such as Titanic or Superstore.
Python Code
import pandas as pd

data = {
    "Name": ["Asha", "Ravi", "Kiran", "Meena", "Arjun"],
    "Age": [20, 22, 19, 21, 23],
    "Marks": [85, 72, 90, 65, 78],
    "City": ["Vijayawada", "Guntur", "Vijayawada", "Hyderabad", "Guntur"]
}

df = pd.DataFrame(data)
print("Original DataFrame:")
print(df)

# Filtering examples
print(df[df["Age"] > 20])
print(df[df["Marks"] >= 80])
print(df[df["City"] == "Guntur"])
print(df[(df["Age"] > 20) & (df["Marks"] > 70)])
print(df[(df["City"] == "Vijayawada") | (df["Marks"] >= 80)])

# Sorting examples
print(df.sort_values(by="Marks"))
print(df.sort_values(by="Marks", ascending=False))
print(df.sort_values(by=["Age", "Marks"]))
print(df.sort_values(by=["City", "Marks"], ascending=[True, False]))
Key Concepts
Boolean conditions select rows that match a requirement.
& combines conditions using AND.
| combines conditions using OR.
sort_values() arranges rows by one or more columns.
ascending=False sorts in descending order.
Analysis
Filtering helps identify records that meet specific conditions, such as students scoring at least 80 marks or students from a particular city. Sorting makes it easier to compare records, such as viewing the highest marks first or arranging students by city and marks.
Conclusion
This task introduced five filtering examples and multiple sorting methods using Pandas. These techniques are useful for exploring and analyzing datasets efficiently.
