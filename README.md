# Unvellling-patterns-of-dataset_Visuliazation-and-statistical-analysis

print(data.columns)


column_to_plot = "median_income"

plt.hist(data[column_to_plot], bins=30)
plt.xlabel(column_to_plot)
plt.ylabel("Frequency")
plt.title(f"Histogram of {column_to_plot}")
plt.show()

