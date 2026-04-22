🎬 Movie Recommendation System (Machine Learning Project)
📌 Project Overview

This project is a machine learning-based movie recommendation system built in Python.
It analyzes user-movie rating behavior and predicts whether a user will like a movie or not (binary classification).

The system was developed as part of a machine learning course project and focuses on model comparison, performance evaluation, and data analysis using real-world datasets.

📊 Dataset

The project uses two datasets:

rating.csv – user ratings for movies
movie.csv – movie metadata (titles, genres)

After merging:

~20 million ratings
138,000+ users
26,000+ movies
Preprocessing steps:
Merged ratings and movie metadata
Removed unnecessary columns (e.g. timestamp)
Converted ratings into binary labels:
1 → rating ≥ 4.0 (Liked)
0 → rating < 4.0 (Not Liked)
Encoded categorical variables (userId, movieId)
Used sampled subsets (100k train / 20k test) for efficiency
🤖 Models Used
1. K-Nearest Neighbors (KNN)
Tested with multiple:
Distance metrics: Euclidean, Manhattan, Cosine
Values of k: 5, 6, 7
Train-test splits: 60/40, 70/30, 80/20
Evaluated performance sensitivity to distance metric and neighbor count
2. Random Forest Classifier
Ensemble model using decision trees
Tested across all data splits
Provided stable baseline performance
3. XGBoost Classifier
Gradient boosting model optimized for structured data
Achieved strong performance across all splits
Tuned using default parameters for comparison
4. LightGBM Classifier
High-performance gradient boosting model
Fast training and competitive accuracy
Evaluated under same experimental conditions
📈 Evaluation Metrics

All models were evaluated using:

Accuracy
F1-Score
Precision & Recall (for detailed analysis)
📊 Experiments Conducted

The project includes a full comparison across:

✔ Train-Test Splits
60/40
70/30
80/20
✔ Model Comparison
KNN (multiple configurations)
Random Forest
XGBoost
LightGBM
✔ Visual Analysis
Bar charts for accuracy comparison
Heatmaps for F1-score distribution
Performance comparison across models and splits
🏆 Key Results
Best overall models: XGBoost and LightGBM
Best KNN performance: Manhattan / Euclidean with k=6 or 7
KNN performed close to baseline (~50–53% accuracy)
Ensemble models significantly improved performance (~57–58% accuracy)
📊 Conclusion
Simple distance-based models (KNN) are limited for large sparse datasets
Ensemble methods (Random Forest, XGBoost, LightGBM) perform better
LightGBM and XGBoost provided the best balance of accuracy and F1-score
Feature simplicity (userId, movieId only) limits model performance, suggesting room for improvement with:
Collaborative filtering features
Matrix factorization
Deep learning models
🛠 Technologies Used
Python
Pandas
NumPy
Scikit-learn
XGBoost
LightGBM
Matplotlib
Seaborn
🚀 Future Improvements
Add collaborative filtering (SVD / Matrix Factorization)
Include genre-based features
Deploy as a web app (Flask / FastAPI)
Build hybrid recommender system

👨‍💻 Author

Developed as a Machine Learning academic project focusing on model comparison and recommendation systems.
