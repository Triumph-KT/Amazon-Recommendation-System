# Amazon Product Recommendation System

Developed a recommendation system to predict and suggest relevant electronic products to Amazon users based on historical user-item interactions, using collaborative filtering and matrix factorization techniques.

## Project Overview

This project applies collaborative filtering methods and matrix factorization to recommend products to users on the basis of previous purchase and rating behaviors. By accurately predicting user preferences, the system enhances customer experience and supports business growth through personalized recommendations.

## Dataset

The dataset consists of Amazon product ratings with the following key fields:
- `user_id`: Unique identifier for each user.
- `prod_id`: Unique identifier for each product.
- `rating`: User’s rating of the product (1–5 scale).

## Objectives

- Build and compare different recommendation algorithms to predict user ratings.
- Optimize models for better performance through hyperparameter tuning.
- Identify and recommend top products for individual users.
- Provide insights into model performance and suggest further improvement strategies.

## Methods

- Data preprocessing and filtering of users/products with low interaction counts.
- Model development and comparison:
  - **Popularity-based Recommendation System**
  - **User-User Collaborative Filtering** (KNN with Mean Squared Difference and Cosine similarity)
  - **Item-Item Collaborative Filtering** (KNN with hyperparameter tuning)
  - **Matrix Factorization using Singular Value Decomposition (SVD)**
- Hyperparameter tuning using **GridSearchCV** for KNN and SVD models.
- Evaluation metrics:
  - Root Mean Squared Error (RMSE)
  - Precision
  - Recall
  - F1-Score

## Results

| Model                          | RMSE   | F1-Score |
|---------------------------------|--------|----------|
| User-User Collaborative (Tuned)| ~1.01  | 0.829    |
| Item-Item Collaborative (Tuned)| 0.969  | 0.816    |
| SVD (Tuned)                    | 0.8995 | 0.827    |

- **User-User Collaborative Filtering** showed the best F1-score for capturing relevant recommendations.
- **SVD** achieved the **lowest RMSE**, indicating superior prediction accuracy.
- Tuned models significantly outperformed baseline versions.

## Business Impact

- Personalized product recommendations to enhance the user experience.
- Increased potential sales by recommending highly rated, relevant products.
- Delivered optimized recommendation strategies through model comparison and tuning.
- Suggested further improvements including hybrid recommendation systems and real-time feedback integration.

## Technologies Used

- Python
- Pandas
- Scikit-learn
- Surprise (KNNBasic, SVD, GridSearchCV)
- Matplotlib
- Seaborn

## How to Run

1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/amazon-product-recommendation.git
    ```

2. Install required dependencies:
    ```bash
    pip install -r requirements.txt
    ```

3. Launch Jupyter Notebook:
    ```bash
    jupyter notebook
    ```

4. Open and run the notebook to train models and generate product recommendations.

## Future Work

- Integrate real-time recommendation capabilities.
- Implement hybrid recommendation systems combining collaborative filtering with content-based methods.
- Explore deep learning-based recommendation architectures for improved accuracy.
- Incorporate user feedback loops to continuously refine recommendations.
