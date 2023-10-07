# Facial-Matching
Machine Learning Algorithms utilizing  PCA (Principal Component Analysis) and KPCA (Kernel Principal Component Analysis)  to facilitate facial matching

# Facial Matching with PCA and KPCA

The core idea is to determine if two given facial images correspond to the same person even if they have different facial expressions. Traditional facial matching approaches used basic methods like template matching; however, with the advent of machine learning and dimensionality reduction techniques, more efficient and accurate methods have emerged.

In this repository, I explore how Machine Learning techniques like PCA (Principal Component Analysis) and KPCA (Kernel Principal Component Analysis) can be used to facilitate facial matching.

## How It Works

1. **Feature Extraction**: PCA and KPCA provide us a way to represent facial images in a lower-dimensional space. In this space, the most significant features (or components) that capture the maximum variance in the dataset are retained.

2. **Distance Metric**: Once we have the reduced representation, we can compute distances between faces. The closer the faces are in this feature space, the more likely they belong to the same person. Commonly used distance metrics include Euclidean distance.

3. **Visualization**: Visualizing faces in a reduced feature space can help in understanding the clustering of similar faces and the separation between different faces.

## Why PCA and KPCA for Facial Matching?

- **Dimensionality Reduction**: Faces are represented as high-dimensional data, especially when considering raw pixel values. PCA and KPCA reduce the dimensionality, making computation and storage more efficient.

- **Noise Reduction**: PCA and KPCA, by focusing on components that capture the most variance, inherently ignore noise.

- **Non-linear Relationships with KPCA**: While PCA is linear, KPCA can capture non-linear relationships in the data using different kernel functions. This is especially useful when the data is not linearly separable.

- **Enhanced Accuracy**: In many cases, representing faces in the reduced feature space can enhance the accuracy of matching as irrelevant features or noise is removed.

## Results 

I implemented both PCA and KPCA from scratch and applied them to a facial dataset. Using a simple nearest-neighbor classifier, we were able to achieve commendable accuracy in face matching. We also visualized the "closest match" for test faces, showing how a test face compares to the most similar face in the training dataset.

Our results are summarized in the form of accuracies achieved using different methods. These accuracy metrics give us confidence in our facial matching systems:

1. PCA:
-Our Implementation: Achieved an accuracy of 95% using our custom PCA implementation.
-Scikit-learn's Implementation: Achieved an accuracy close to our custom implementation.
2. KPCA with rbf kernel:
-Our Implementation: The accuracy was slightly better than PCA, indicating the benefit of capturing non-linear relationships.
-Scikit-learn's Implementation: Comparable accuracy with our custom implementation.

## Conclusion

PCA and KPCA are powerful tools for facial matching, providing a compact representation of faces and aiding in efficient and accurate face recognition.
