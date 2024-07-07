# Unvellling-patterns-of-dataset_Visuliazation-and-statistical-analysis
# HISTOGRAM
print(data.columns)


column_to_plot = "median_income"

plt.hist(data[column_to_plot], bins=30)
plt.xlabel(column_to_plot)
plt.ylabel("Frequency")
plt.title(f"Histogram of {column_to_plot}")
plt.show()

# BOXPLOT

plt.boxplot(data[column_to_plot])
plt.xlabel(column_to_plot)
plt.ylabel("Values")
plt.title("Boxplot of " + column_to_plot)
plt.show()


#  SCATTER PLOT

x_axis = "longitude"
y_axis = "latitude"

#Create the scatter plot
plt.scatter(data[x_axis], data[y_axis])

#Add labels and title to the plot
plt.xlabel(x_axis)
plt.ylabel(y_axis)
plt.title("Scatter Plot of " + x_axis + " vs " + y_axis)

#Display the scatter plot
plt.show()

# LINE CHART
x_axis = "longitude"
y_axis = "latitude"

#Create the line chart
plt.plot(data[x_axis], data[y_axis])
plt.xlabel(x_axis)
plt.ylabel(y_axis)
plt.title("Line Chart - " + y_axis + " vs " + x_axis)
plt.show()


# BAR GRAPH
x_axis_column = "longitude"
y_axis_column = "latitude"

#Create the bar graph
plt.bar(data[x_axis_column], data[y_axis_column])

#Add labels and title to the plot
plt.xlabel(x_axis_column)
plt.ylabel(y_axis_column)
plt.title("Bar Graph of " + y_axis_column + " vs " + x_axis_column)

#Display the bar graph
plt.show()



# PIE CHART

category_column = "longitude"
value_column = "latitude"
#Create the pie chart
plt.pie(data[value_column], labels=data[category_column], autopct="%1.1f%%")

#Add title to the plot (optional)
plt.title("Pie Chart")

#Display the pie chart
plt.show()

# AREA FILL CHART

category_column = "longitude"
value_column = "latitude"
#Create the pie chart
plt.pie(data[value_column], labels=data[category_column], autopct="%1.1f%%")
#Add title to the plot (optional)
plt.title("Pie Chart")
#Display the pie chart
plt.show()


# MEAN VALUE

mean_value = df.mean()
print(mean_value)

# MEDIAN
import statistics
median = statistics.median(data)
print("The median of the dataset is:", median)

# MODE
try:
  # mode() function might raise an error for empty data
  mode_value = statistics.mode(data)
  print("The mode of the data is:", mode_value)
except StatisticsError:
  print("The data is empty or has no mode.")

# CORRELATION
correlation_matrix = df.corr()

#Print the correlation matrix
print(correlation_matrix)
column1 = 'longitude'
column2 = 'latitude'
correlation_value = correlation_matrix[column1][column2]

print(f"Correlation between {column1} and {column2}: {correlation_value}")



















