---
{"dg-publish":true,"permalink":"/machine-learning/lecture-1/clustering/","dgPassFrontmatter":true}
---

---
#### **Homogeneity:**

- Homogeneity measures the extent to which all clusters contain only data points that are members of a single class. A higher homogeneity score indicates that each cluster predominantly contains data points from a single class. The mathematical formula to calculate homogeneity is given by:
## $h = 1 - \frac{H(C|K)}{H(C)}$
- where $H(C|K)$ is the conditional entropy of the class distribution given the cluster assignments, and $H(C)$ is the entropy of the class distribution.
    

#### **Silhouette Score:**

- The Silhouette Score is a measure of how similar an object is to its own cluster compared to other clusters. The silhouette score ranges from -1 to 1, where a high value indicates that the object is well matched to its own cluster and poorly matched to neighboring clusters. The formula for silhouette score is as follows:
- For each sample: $a(i) =$ the average distance between $i$ and all other data points in the same cluster, $b(i) =$ the smallest average distance between $i$ and all data points in any other cluster.
## $Silhouette(i) = \frac{b(i) - a(i)}{\max{a(i), b(i)}}$
- The average Silhouette Score is the mean Silhouette score for all samples.
    

#### **Completeness:**

- Completeness measures the degree to which all data points that are members of a given class are elements of the same cluster. A higher completeness score indicates that all data points from the same class are clustered closely together. The mathematical formula to calculate completeness is:
## $c = 1 - \frac{H(K|C)}{H(K)}$
- where $H(K|C)$ is the conditional entropy of the cluster assignments given class labels, and $H(K)$ is the entropy of the cluster assignments.
---

## View Next Topics:

### [[Machine Learning/Lecture 1/Training the Model\|Training the Model]]: