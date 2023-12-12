# Singular-decomposition-for-face-recognition
This script demonstrates the concept of face recognition using Singular Value Decomposition (SVD).

## Prerequisites

- NumPy
- Pandas
- Matplotlib
- OpenCV

## Description


1. Load the face images from the dataset folder.
2. Data Preprocessing
3. Calculate the correlation matrix
4. Singular Value Decomposition (SVD): Perform SVD on the data matrix to decompose it into three matrices: U, Σ, and V*. Here, U contains the eigenvectors of the covariance matrix, Σ is a diagonal matrix with singular values, and V* contains the transpose of the right singular vectors.
5. Eigenface Calculation: Calculate the eigenfaces by considering the principal components (eigenvectors) obtained from the SVD. These eigenfaces capture the most significant variations in the dataset.
6. Face Reconstruction: Reconstruct faces using a subset of eigenfaces. Vary the number of eigenfaces used and visualize the reconstructed faces at different levels of approximation.
7. Face Recognition: Apply the recognition algorithm using eigenfaces. This involves projecting new faces onto the eigenfaces and comparing the distances or similarities to recognize or classify them.
8. Reconstruct the test face using a subset of eigenfaces and the weights.

## Results

The script will display the original test face and the reconstructed faces using different rank levels. You can observe how the quality of the reconstruction improves as more eigenfaces are used, however, SVD hasnt achieve a
a good approximation becuase it only considers linear relations between faces, and in the dataset I used, there are rotations and flips that cannot be consider correctly by the SVD technique.
