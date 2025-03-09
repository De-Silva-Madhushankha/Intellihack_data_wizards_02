# Intellihack_data_wizards_02 - Customer Segmentation

## Overview
This task involves segmenting customers based on their behavior on an e-commerce platform. The dataset includes customer interactions, purchases, and browsing patterns, and the goal is to identify three distinct customer segments:
- **Bargain Hunters**: Frequent buyers who rely on discounts.
- **High Spenders**: Customers who make fewer but high-value purchases.
- **Window Shoppers**: Users who browse a lot but rarely purchase.

### Description of Columns

*   **total\_purchases:** The total number of purchases a customer makes.
*   **avg\_cart\_value:** The average value of items in the customer's cart.
*   **total\_time\_spent:** The total time (in unspecified units) a customer spent on the platform.
*   **product\_click:** The number of times a customer clicks on a product.
*   **discount\_counts:** The number of discounts a customer has used.
*   **customer\_id:** A unique identifier for each customer.

### Data Sample

| total_purchases | avg_cart_value | total_time_spent | product_click | discount_counts | customer_id |
|-----------------|----------------|-------------------|---------------|-----------------|-------------|
| 7.0             | 129.34         | 52.17             | 18.0          | 0.0             | CM00000     |
| 22.0            | 24.18          | 9.19              | 15.0          | 7.0             | CM00001     |
| 2.0             | 32.18          | 90.69             | 50.0          | 2.0             | CM00002     |
| 25.0            | 26.85          | 11.22             | 16.0          | 10.0            | CM00003     |
| 7.0             | 125.45         | 34.19             | 30.0          | 3.0             | CM00004     |

## Approach
### 1. Data Loading
- Loaded the dataset using Pandas.
- Checked for missing values and inconsistent data types.

### 2. Data Cleaning
- Handled missing values by imputing or removing them based on analysis.
- Checked for and handled outliers using statistical methods and visualizations.

### 3. Data Preprocessing
- **Encoding**: Ensured object features were properly encoded.
- **Scaling**: Applied standard scaling to standardize numerical features for clustering.

### 4. Exploratory Data Analysis (EDA)
- **Statistical Summary**: Computed mean, median, and distributions for each feature.
- **Visualizations**: Used histograms, box plots, and scatter plots to understand data distributions and correlations.

### 5. Feature Engineering
- **Dimensionality Reduction**: Used Principal Component Analysis (PCA) to visualize clusters in a lower-dimensional space.

### 6. Clustering Model Selection
  Used the elbow method to determine the optimal number of clusters
- **K-Means Clustering**: as initial clustering model.
- **Hierarchical Clustering**: Compared results with K-Means.

### 7. Model Evaluation
- **Silhouette Score**: Measured cluster cohesion and separation.
- **Cluster Visualization**: Used scatter plots and PCA to visualize cluster separation.

## Results
- Successfully identified three clusters representing the expected customer segments.
- **Bargain Hunters**: Customers with frequent purchases, low cart value, and high discount usage.
- **High Spenders**: Customers with fewer high-value purchases and low discount dependency.
- **Window Shoppers**: Customers who browse a lot but rarely make purchases.

## Dependencies
- Python 3.x
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn

## How to Run the Notebook
1. Clone the repository:
   ```bash
   git clone https://github.com/De-Silva-Madhushankha/Intellihack_data_wizards_02.git
   ```
2. Navigate to the project folder:
   ```bash
   cd Intellihack_data_wizards_02
   ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
4. Open the Jupyter Notebook:
   ```bash
   jupyter notebook intellihack-data-wizards-02.ipynb
   ```
5. Run all cells to execute the analysis.

## Future Improvements
- Improve clustering by experimenting with additional algorithms like Gaussian Mixture Models (GMM).
- Integrate advanced feature engineering, such as customer lifetime value (CLV) prediction.
- Deploy as an API for real-time customer segmentation.

## Author
- **Madhushankha De Silva**


