# Recommendation System (Collaborative Filtering/Matrix Factorization)

*COMPANY* : CODTECH IT SOLUTIONS

*NAME* : PREETHAM B

*INTERN ID* : CT12WM72

*DOMAIN* : MACHINE LEARNING 

*DURATION* : 12 WEEKS

*MENTOR* : NEELA SANTOSH 

## Project Overview
This project focuses on developing a **Recommendation System** using **Collaborative Filtering** and **Matrix Factorization** techniques. The system is built using the **MovieLens 100K dataset**, where user ratings are analyzed to generate personalized movie recommendations. The deliverable for this task is a **Jupyter Notebook or an application showcasing recommendations and evaluation metrics**.

## Dataset Used
The **MovieLens 100K dataset** consists of **100,000 ratings** from **943 users** across **1,682 movies**. It includes two primary files:
1. `u.data`: Contains user IDs, movie IDs, ratings, and timestamps.
2. `u.item`: Contains movie IDs and their corresponding titles.

## Approach Followed
The recommendation system was implemented using the following approach:
1. **Data Loading and Preprocessing**
2. **Creating a User-Item Matrix**
3. **Building a Collaborative Filtering Model**
4. **Generating Movie Recommendations**
5. **Mapping Movie IDs to Titles**
6. **Displaying Final Recommendations**

## Step-by-Step Implementation
### 1. Data Loading and Preprocessing
- We loaded the `u.data` file and assigned column names (`user_id`, `item_id`, `rating`, `timestamp`).
- The `u.item` file was also loaded to map `item_id` to movie titles.
- Unnecessary columns such as `timestamp` were dropped since they were not relevant to the recommendation process.

### 2. Creating a User-Item Matrix
- The dataset was transformed into a **user-item interaction matrix** where rows represented users and columns represented movies.
- Missing values (unrated movies) were filled with **0s**, indicating no rating given by the user.

### 3. Building a Collaborative Filtering Model
- The **Singular Value Decomposition (SVD)** method was used for **Matrix Factorization**.
- SVD decomposed the user-item matrix into lower-dimensional matrices to identify latent factors influencing user preferences.
- We used **Truncated SVD** from `sklearn.decomposition` to retain key components while reducing computational complexity.

### 4. Generating Movie Recommendations
- Using the transformed user-movie matrix, predictions were generated for missing ratings.
- For a given user, the **top N recommendations** were selected based on predicted ratings.

### 5. Mapping Movie IDs to Titles
- The recommended `item_id`s were mapped to their respective **movie titles** using the `u.item` dataset.
- This helped in presenting meaningful recommendations to the user.

### 6. Displaying Final Recommendations
- For a test user (e.g., **User 1**), the system provided the following recommendations:
  - **Titanic (1997)**
  - **Schindler’s List (1993)**
  - **One Flew Over the Cuckoo’s Nest (1975)**
  - **Casablanca (1942)**
  - **It’s a Wonderful Life (1946)**

## Technologies Used
- **Python**
- **Pandas** for data handling
- **NumPy** for numerical computations
- **Scikit-learn** for Matrix Factorization (Truncated SVD)
- **Jupyter Notebook** for implementation and visualization

## Challenges Faced
1. **Parsing Errors:** Some issues occurred while loading the dataset due to incorrect column specifications, which were fixed by adjusting parameters in `pd.read_csv()`.
2. **Sparse Data Handling:** Since most movies were unrated by users, techniques like **Matrix Factorization** helped extract meaningful patterns.
3. **Performance Optimization:** Using **Truncated SVD** instead of standard **SVD** helped reduce the computation time while maintaining accuracy.

## Future Enhancements
- Implement **User-Based Collaborative Filtering** alongside **Matrix Factorization** for comparison.
- Use **Deep Learning-based Recommendation Systems** for improved accuracy.
- Incorporate **content-based filtering** to consider movie genres and descriptions.
- Deploy the model as a **Web App** for real-time movie recommendations.

## Conclusion
This project successfully built a **Collaborative Filtering-based Recommendation System** using the MovieLens dataset. By applying **Matrix Factorization**, we generated personalized movie recommendations based on user preferences. This approach demonstrates how data-driven techniques can enhance user experiences in recommendation systems.

## Output

![Image](https://github.com/user-attachments/assets/0a487366-2c51-4552-8cbf-156d8cf0063f)

![Image](https://github.com/user-attachments/assets/ff75eb3a-ce1e-4b16-a64f-6e86a77114bd)

![Image](https://github.com/user-attachments/assets/7961f6be-019d-4d13-9f74-7945aa109a5c)

![Image](https://github.com/user-attachments/assets/0d7be293-edcc-48b0-b868-556083199b9a)

![Image](https://github.com/user-attachments/assets/b9881da5-d76e-4227-93b7-ffd0bdfc6ec8)

![Image](https://github.com/user-attachments/assets/167bb265-40ec-4fac-b749-5d8420e278b2)

![Image](https://github.com/user-attachments/assets/7abfbdcc-fc81-4db1-9670-c23a24ad9e54)

![Image](https://github.com/user-attachments/assets/d917a8a0-8b6a-4153-a7bd-ed4ac20ea033)
