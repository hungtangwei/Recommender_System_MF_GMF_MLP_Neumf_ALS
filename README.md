# Recommender_System_MF_GMF_MLP_Neumf_ALS

## Description
Kaggle challenge: https://www.kaggle.com/t/6d26bd75418742f5b2d2c605840e4637.

This dataset is collected from an online social network platform. People interact with others by making friends and posting reviews and ratings for different items. Please recommend a list of items to each user.

To finish this task, I will use three models which are alternating least squares model, matrix factorization model (with bias), and neural matrix factorization model to build the recommender system to recommend the top 10 items for each user.

## Matrix factorization Model (with bias):
The matrix factorization algorithm is decomposing the user-item interaction matrix into the product of two lower dimensionality rectangular matrices. In addition, due to variation in rating among different users, I add item bias and user bias to this matrix factorization model.

## Neural matrix factorization Model:
According the Neural Collaborative Filtering (He, X., Liao et al., 2017), the neural matrix factorization model is combining the generalized matrix factorization (GMF), a generalized version of matrix factorization that under neural collaborative filtering that uses the sigmoid function to output, and multi-layer perceptron model (MLP) which using a standard multi-layer perceptron to learn the interaction between user and item latent features by adding hidden layers on the concatenated vector to reinforce each other to better model the complex user-item interactions.
In addition, due to the objective function that uses gradient-based optimization method of Neural matrix factorization only find locally optimal solutions. I initialize Neural matrix factorization by using the pre-trained models of generalized matrix factorization model and multi-layer perceptron model.

## Alternating least squares (ALS) model:
The Alternating Least Squares model is a form of matrix factorization which could reduce user-item matrix into a very smaller amount of dimension called hidden or latent features.

## Data
The user item interaction data is the main data for this challenge. This data is further split into training, validation, and test sets.
- Training data: The training dataset contains a set of interactions between users and items. If a user engages with an item, then there will be a record in the dataset.
- Test data: Each user is provided with a list with 100 candidates in the test dataset, you will need to check the candidate list and recommend the top 10 items for each user.
- Validation data: Similar to the Test data, the difference is that the last column in the Validation dataset is the ground truth of the ratings. You can use this dataset to tune your model.

## Authors

Tangwei, Hung

## Contact
hung.tangwei@gmail.com
