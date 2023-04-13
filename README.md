# Advanced-stats-4

# Interpretation of PCA

This document discusses the interpretation of PCA, specifically how to find the unit vector u that minimizes the squared distance between the projection of a set of unit vectors X along u and each individual vector x in X. It can be shown that the unit vector u that minimizes this distance corresponds to the first principal component of X. Additionally, it can be shown that the k dimension subspace spanned by the first k PCA components minimizes the squared distance between the projection and the original data.

# Image Compression using PCA

This document demonstrates how to use PCA for image compression using the jpeg package. First, the photo of a tiger is read in using the readJPEG() command, resulting in a 3-dimensional matrix of RGB color values. PCA is then applied to all three matrices to compress the data by dropping columns corresponding to smaller eigenvalues. The fraction of variance is plotted as k increases, and the new image is saved and its size noted. The compression ratio is then plotted as a function of k to show how the size of the new image compares to the size of the original image.

# Dimension Reduction vs Regularization
This document compares the performance of PCR and PLS on the Boston dataset in the ISLR2 package. The dataset is split into a training set and a test set with an 80:20 split. A PCR model is fit on the training set with M chosen by cross-validation, and the test error and value of M selected are reported. A PLS model is also fit on the training set with M chosen by cross-validation, and the test error and value of M selected are reported. Additionally, a ridge regression model and a lasso model are fit on the training set with lambda chosen by cross-validation, and their respective test errors and number of non-zero coefficient estimates are reported. The results are then compared to determine how accurately the crime rate can be predicted and if there is much difference among the test errors resulting from these approaches.

# Weighted Linear Regression
This document uses weighted linear regression to correct for the non-constant variance in the first problem for (Advanced-stats3 repo). The range of Field is split into 12 groups of size nine (except for the last group which has only eight values), and the variance of Lab is computed within each group. The mean of Field is also computed within each group. The variance in the response is then linked to the predictor by regressing log(varlab) on log(meanfield) to estimate a0 and a1 (excluding the last point). These estimates are used to determine appropriate weights in WLS for Lab on Field, and the regression summary is shown.
