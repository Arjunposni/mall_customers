#  K-Means Clustering: Mall Customer Segmentation

##  Objective

Perform unsupervised learning using the **K-Means clustering algorithm** to segment mall customers based on their behavior and characteristics.

##  Dataset

- Dataset: Mall Customer Segmentation Data
- Columns Used:
  - `Gender` (converted to numerical)
  - `Age`
  - `Annual Income (k$)`
  - `Spending Score (1–100)`

## Tools & Libraries

- Python
- `pandas` – data handling
- `scikit-learn` – ML and clustering
- `matplotlib`, `seaborn` – visualization
- `PCA` – dimensionality reduction for plotting

---

##  Steps Followed

### 1. Data Preprocessing
- Dropped `CustomerID` (not useful for learning).
- Converted `Gender` to numerical (Male = 0, Female = 1).
- Scaled all features using `StandardScaler` to normalize values.

### 2. Elbow Method
- Plotted `Inertia` vs. `K` (1–10) to find the optimal number of clusters.
- The curve showed improvement slowing down after K=5, but needed deeper evaluation.

### 3. Silhouette Score Evaluation
- Tested K values from 2 to 109.
- Calculated Silhouette Score for each value to find the optimal cluster count.

###  **Best K Found: 18**
-  **Silhouette Score at K=18: 0.4345**
- This indicates well-separated, meaningful clusters.

### 4. Final K-Means Clustering
- Applied KMeans with `n_clusters = 18`.
- Assigned cluster labels to each customer.
- Visualized clusters using PCA-reduced 2D data.

---

##  Results

- **Optimal Clusters (K):** 18
- **Evaluation Metric:** Silhouette Score = **0.4345**
- **Visualization:** Done using PCA and `seaborn` scatterplot
- Customers grouped into 18 distinct segments for targeted marketing

---

##  Key Concepts Learned

| Concept | Explanation |
|--------|-------------|
| K-Means | Clustering algorithm that groups data by minimizing intra-group distances |
| Inertia | Total distance between points and their cluster center |
| Elbow Method | Helps identify where adding more clusters stops improving model |
| Silhouette Score | Metric to evaluate clustering quality (ranges from -1 to 1) |
| PCA | Used to reduce dimensions for 2D plotting |

---

##  Final Thoughts

The clustering performance improved significantly when we extended our K search space beyond 10. K=18 gave the best result with a clear structure in customer behavior, useful for personalized business strategies.

---
