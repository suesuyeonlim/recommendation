# Recommending Movies from User Ratings
## I. Project Background
In this project, I train models to recommend movies for users based on their existing ratings for different movies. I use collaborative filtering methods, both model-based and memory-based. The following lists the different methods used in this project.
- Model-Based Methods
  - Alternating Least Squares ("ALS")
  - Singular Value Decomposition ("SVD")
- Memory-Based Methods
  - KNNBasic
  - KNN-w-Means
  - KNN-w-Baseline
 
## II. Data
The training is done on the [MovieLens](https://grouplens.org/datasets/movielens/) data of approximately 100,000 ratings between 1996 and 2018 for 600 users and 9,000 movies in total. Below is an excerpt of the data.

<img width="394" alt="image" src="https://github.com/suesuyeonlim/recommendation/assets/19903898/9ad75a0f-f6da-4df9-8596-b5ec3a0d369d">

## III. Models
- Model-Based Collaborative Filtering: Model-based matrix factorization separates a rating into a user component and an item component. An item component has factors related to an item, and a user component has sensitivities to those factors. See the diagram below.

  ![image](https://github.com/suesuyeonlim/recommendation/assets/19903898/76b99f08-7829-4fa3-b776-00e82602c9d3)
  
  - ALS: ALS minimizes errors by alternating between holding the user embedding matrix constant and the item embedding matrix constant.
    
    <img width="854" alt="image" src="https://github.com/suesuyeonlim/recommendation/assets/19903898/2a524dd7-1494-4d24-ad04-42e211f8a024">

  - SVD: SVD is a commonly used matrix factorization method. It is decomposed in the following form.

    ![image](https://github.com/suesuyeonlim/recommendation/assets/19903898/61e9c358-482e-4f97-a865-6448796f8153)

- Memory-Based Collaborative Filtering: Memory-based collaborative filtering consists of two approaches: item-based and user-based filtering. Item-based filtering connects users based on the products that they purchased in common, and recommend the products frequently purchased by other similar users. User-based filtering finds users that are most similar based on the purchases, and recommend products purchased by the similar user.

  <img width="478" alt="image" src="https://github.com/suesuyeonlim/recommendation/assets/19903898/d4dc8eff-b0e7-4fa5-b563-8989f47fe003">

  - KNN-Basic: a basic KNN-based collaborative filtering algorithm that utilizes distance measurements between samples and other data points in a dataset to predict ratings. It identifies the K-nearest neighbors and utilizes majority voting to make rating predictions.
  - KNN-w-Baseline: a basic KNN-based collaborative filtering algorithm that takes into account a baseline rating to discover the functional connections between an input and output for rating prediction.
  - KNN-w-Means: a basic KNN-based collaborative filtering algorithm that takes into account the mean ratings of each user. It computes the mean values for both item and user ratings and uses them to predict ratings.

## IV. Training & Result
  
## V. Conclusion

## VI. Next Steps

## VII. Location of Data/Analysis
- Data: See "Data" folder. 
- Analysis: See "Code.ipynb". 
- Analysis Summary: See "Project 3 Presentation.pdf".
