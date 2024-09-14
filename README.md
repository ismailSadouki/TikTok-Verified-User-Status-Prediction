# TikTok-Verified-User-Status-Prediction
**Predicting Verified User Status Using Logistic Regression on TikTok Data**

This project involves building a logistic regression model to predict whether a TikTok user is verified based on video characteristics. The dataset includes features such as video duration, view counts, likes, and comments. The model aims to assist TikTok in reducing the backlog of user reports by predicting verification status and improving content moderation efficiency.



### [Summary](https://github.com/ismailSadouki/TikTok-Verified-User-Status-Prediction/blob/main/summary.pdf)

### [Jupyter Notebook](https://github.com/ismailSadouki/TikTok-Verified-User-Status-Prediction/blob/main/TikTok%20project%20.ipynb)
### [Jupyter Notebook PDF](https://github.com/ismailSadouki/TikTok-Verified-User-Status-Prediction/blob/main/TikTok%20project%20.pdf)

### [Data](https://github.com/ismailSadouki/TikTok-Verified-User-Status-Prediction/blob/main/tiktok_dataset.csv)

## Project Overview
The main objective of this project is to develop a logistic regression model to predict whether a TikTok user is verified. By analyzing various features, the model provides insights into the correlation between video characteristics and verified user status. The model achieved a predictive accuracy of 65%.

## Business Understanding
The operations team at TikTok is interested in understanding how user verification is associated with video content and characteristics. By predicting user verification, the model can prioritize flagged content more effectively. This helps in reducing operational backlog and improving the user reporting process on TikTok.

## Data Understanding
The dataset used in this project contains the following key features:
- **Video Duration**: The length of the video in seconds.
- **View Count**: Total number of views for the video.
- **Like Count**: Total number of likes the video received.
- **Share Count**: Number of times the video was shared.
- **Download Count**: Number of times the video was downloaded.
- **Comment Count**: Total number of comments on the video.
- **Verified Status**: Whether the user is verified or not (target variable).

The dataset consists of 19,382 observations and 12 features. Some exploratory data analysis (EDA) was conducted to check for missing values, outliers, and class imbalances.

### Data Limitations
- **Imbalanced Target Variable**: The dataset was highly imbalanced, with 94.2% of videos posted by unverified users and only 5.8% by verified users. This required resampling techniques to balance the classes.
- **Outliers**: Outliers were handled in key numerical features such as video likes and comments.

## Modeling and Evaluation
- **Model Used**: Logistic Regression
- **Evaluation Metrics**:
  - Accuracy: 65%
  - Precision: 61% (for "not verified" class)
  - Recall: 84% (for "not verified" class)
  - F1-Score: 0.71 (for "not verified" class)

The logistic regression model was selected due to its interpretability and efficiency for binary classification tasks. One-hot encoding was applied to categorical features, and the model was evaluated using a confusion matrix and classification report.

## Conclusion
The logistic regression model provides a decent level of accuracy (65%) in predicting whether a TikTok user is verified based on video features. While the precision is less than ideal, the high recall (84%) for the target class suggests that the model is effective at identifying unverified users.

### Recommendations
Further improvements could be made by:
- Testing other classification models (e.g., Random Forest, XGBoost) to compare performance.
- Gathering more data to reduce class imbalance and improve generalization.
- Incorporating additional features such as user profile characteristics or engagement metrics.
