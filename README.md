
# Customer Segmentation 

This project performs customer segmentation on the Mall Customers dataset. Customer segmentation is a process of dividing customers into groups based on shared characteristics to help businesses better target and serve their customers. In this project, clustering techniques are applied to group customers based on their purchasing behavior and demographics.

## Table of Contents

1. [Project Overview](#project-overview)
2. [Installation](#installation)
3. [Dataset](#dataset)
4. [Exploratory Data Analysis](#exploratory-data-analysis)
5. [Data Preprocessing](#data-preprocessing)
6. [Modeling](#modeling)
7. [Evaluation](#evaluation)
8. [Results](#results)
9. [Usage](#usage)
10. [Contributing](#contributing)
11. [License](#license)

---

## Project Overview

The goal of this project is to segment customers into distinct groups based on their spending patterns and demographic characteristics. This segmentation allows businesses to better understand customer behavior, design targeted marketing strategies, and enhance customer satisfaction.

## Installation

To run this project, ensure you have the following libraries installed:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

## Dataset

The dataset used is the **Mall Customers Dataset** available on [Kaggle](https://www.kaggle.com/datasets). It includes 200 entries, each representing a customer profile with the following features:

- **CustomerID**: Unique identifier for each customer.
- **Gender**: Gender of the customer.
- **Age**: Age of the customer.
- **Annual Income (k$)**: Annual income of the customer in thousands of dollars.
- **Spending Score (1-100)**: Score assigned by the mall based on customer behavior and spending.

## Exploratory Data Analysis

### Key Steps in EDA:
1. **Descriptive Statistics**: Summarize each feature (mean, median, standard deviation) to understand basic distribution.
2. **Visualizations**:
   - Distribution plots for each feature.
   - Box plots to identify outliers in features like age and income.
   - Pair plots to visualize relationships between variables and potential clusters.
   - Gender-based spending and income insights.

## Data Preprocessing

1. **Handling Missing Values**: Check for and handle any missing data if present.
2. **Encoding Categorical Data**: Convert the `Gender` feature to numerical values (e.g., Male = 1, Female = 0) if applicable.
3. **Feature Scaling**: Standardize features like age and income to ensure equal influence during clustering.

## Modeling

This project applies clustering techniques to segment customers based on their similarities.

### Techniques:
- **K-Means Clustering**:
   - K-Means is used to cluster customers by minimizing the variance within clusters.
   - Optimal number of clusters (`k`) is selected using the **Elbow Method** and **Silhouette Score**.
- **Hierarchical Clustering** (optional):
   - For additional insights, hierarchical clustering can be used to create a dendrogram and further understand the relationship between customers.

## Evaluation

- **Elbow Method**: Plots the within-cluster sum of squares against different values of `k` to identify the optimal number of clusters.
- **Silhouette Score**: Measures how similar a customer is to their own cluster compared to other clusters, indicating the quality of clustering.

## Results

The segmentation results help categorize customers into clusters based on shared characteristics. Each cluster may represent a different type of customer, such as:

1. **High Income & High Spending**: Likely high-value customers for targeted marketing.
2. **High Income & Low Spending**: Potential targets for increasing spending behavior.
3. **Low Income & High Spending**: Price-sensitive customers with high spending frequency.
4. **Low Income & Low Spending**: Cost-conscious customers.

Visualizations, such as scatter plots of clusters in two-dimensional space, can provide further insights into the segmentation.

## Usage

This segmentation model can be used for:

1. **Targeted Marketing**: Customizing marketing strategies to each segment based on their unique profiles.
2. **Customer Relationship Management**: Developing retention and engagement strategies tailored to specific customer types.
3. **Product Recommendations**: Offering products or services that align with the preferences of each segment.

## Contributing

Contributions are welcome! Please feel free to create a pull request if you have suggestions for improvement or new features.

## License

This project is licensed under the MIT License.

