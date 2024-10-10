# CMSC 320

## GPT Midterm Exam

### 10/09/2024

### Name: 

### UID:


## 1. Definitions (10 points)

<ol>
    <li>Central Limit Theorem
        <ul>
            <li>When constructing a sampling distribution, as n -> infinity where n is the number of data points (sample means), the distribution will be approximately normal and can be used to make inferences about the population - a safe threshold is where n > 30, it is safe to assume the sampling distribution will be normal
        </ul>
    <li> Confounder
        <ul>
            <li>A variable that may affect the dependent variable as it plays a extraneous role in an experiment that may lead to unrealistic/surpriusing results if not controlled/removed
        </ul>
    </ol>


3. Bernoulli Distribution
4. Null Hypothesis
5. One-hot Encoding
6. Histogram
7. Alpha Value
8. Z-score


## 2. Data Analysis using Pandas (20 points)

You are given a dataset related to product sales in a store. It contains the following columns:

- Product (String): The product name
- Price (Float): The price of the product
- Quantity Sold (Int): The number of units sold
- Date (String): The date of sale in the format "YYYY-MM-DD"
- Category (String): The product category

Write Pandas code to do the following:

(a) Change the "Date" column to datetime format.
```bash
df['Date'] = pd.to_datetime(df['Date'])
```
(b) Group the data by "Category" and find the total revenue (Price * Quantity Sold) for each category.
```bash
df['Total Revenue'] = df.groupby('Category')[['Price', 'Quantity Sold']].prod()
```

(c) Filter the dataframe to include only records where "Quantity Sold" is greater than 50.
```bash
df[df['Quantity Sold'] > 50]
```

(d) Create a new column, "Discounted Price," which is 90% of the original price.
```bash
df['Discounted Price'] = df['Price'] * 0.9
```

(e) Print out the number of unique product categories.
```bash
df['Categories'].value_counts().size
```

## 3. Visualization (10 points)

Given the same product sales dataset, answer the following:

(a) To display the relationship between "Price" and "Quantity Sold," which type of graph would you use?
<br>
Scatter Plot

(b) You want to examine how sales have changed over time. Which visualization would be most suitable?
<br>
Histogram

(c) Create a scatter plot to visualize the correlation between "Price" and "Quantity Sold" and explain what the pattern might indicate.
<br>
...


## 4. Hypothesis Testing (15 points)

You are conducting a study to determine if there is a difference in average sales between two different branches of a store, Branch A and Branch B. You have the sales data from both branches for the past year.

(a) State the null and alternative hypotheses.

(b) Which statistical test would be most appropriate to compare the average sales between the two branches? Why?

(c) Describe what a p-value represents in this context.

## 5. Distributions and Statistics (15 points)

(a) What type of distribution would best represent the waiting time between customer arrivals at a bank?

(b) If you have a dataset with a median significantly lower than the mean, what does this indicate about the distribution of your data?

(c) The number of customers entering a store each hour follows a Poisson distribution with λ = 10. Draw the general shape of this distribution and describe its characteristics.

## 6. Experiment Design (10 points)

You are designing an experiment to test whether a new tutoring program improves students' grades.

(a) Describe one potential confounding variable in this experiment.

(b) How would you randomize the assignment of students to the tutoring program or control group?

## 7. Feature Engineering (10 points)

(a) Given a dataset containing student grades ("Grade"), explain how you could use binning to create a categorical variable for "Grade".

(b) Explain what one-hot encoding is and give an example of when it might be necessary.


## 8. K-Means Clustering (10 points)

(a) Explain what the K-means algorithm aims to achieve.

(b) Given a dataset of customer spending behavior, how would you decide on the number of clusters (k) to use?

(c) Describe one situation where K-means might not be the best clustering method and explain why.


## 9. Data Cleaning (10 points)

You are analyzing a dataset with missing values and outliers.

(a) When would mean imputation be a poor choice for handling missing values?

(b) Describe how you might detect and handle outliers in a dataset with continuous variables.

