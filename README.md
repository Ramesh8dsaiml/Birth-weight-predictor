# Birth-weight-predictor web application 
  
### End-to-End Machine Learning Web Application

### Web Interface

<img width="1920" height="1200" alt="{E845443C-DEDA-4B01-86F4-F975262CA58D}" src="https://github.com/user-attachments/assets/495f7c5c-d9ef-42fb-81a2-c49c4ed80a4f" />


### Deployment (Render)

<img width="1920" height="1134" alt="{610E850D-E0A7-4852-886A-53D25D171B53}" src="https://github.com/user-attachments/assets/243d2e8e-9c8b-4b87-b3b2-9760aefeb3d8" />

<img width="1920" height="974" alt="image" src="https://github.com/user-attachments/assets/9f6caf61-1786-41a5-a8fe-3fd9251cfffd" />



# **Live Application:**  
https://birth-weight-predictor-3-g60m.onrender.com  

A production-ready Machine Learning web application that predicts a baby’s birth weight (in ounces) using maternal and pregnancy-related features.

This project demonstrates the complete ML lifecycle:
Data Collection → Data Preprocessing → EDA → Model Training → Model Serialization → Flask API Integration → Frontend Development → Deployment on Render.

---

##  Dataset Information

- **Source:** Kaggle  
- **File Used:** `babies.csv`

The dataset contains maternal and pregnancy-related attributes used to predict birth weight.

### Features Used:

| Feature | Description |
|----------|-------------|
| Gestation | Length of pregnancy (days) |
| Parity | 0 = First pregnancy |
| Age | Mother’s age (years) |
| Height | Mother’s height (inches) |
| Weight | Mother’s weight (pounds) |
| Smoke | 1 = Smoker, 0 = Non-smoker |
| Bwt | Birth weight (ounces) – Target Variable |

---

##  Data Preprocessing

- Checked dataset structure and data types  
- Handled missing values  
- Removed duplicate records  
- Performed correlation analysis  
- Selected relevant features  

Libraries Used:
- Pandas  
- NumPy  
- Matplotlib  

---

##  Exploratory Data Analysis (EDA)

- Distribution visualization  
- Correlation heatmap  
- Smoking impact on birth weight  
- Gestation vs Birth weight analysis  

---
##  Model Development

###  Train-Test Split
Used `train_test_split()` from Scikit-learn.

###  Algorithms Implemented

- Linear Regression (Baseline Model)
- Lasso Regression (L1 Regularization)
- Ridge Regression (L2 Regularization)

Regularization techniques were applied to reduce overfitting and improve generalization.

###  Model Evaluation

Models were compared using:

- RMSE (Root Mean Squared Error)
- R² Score

The best-performing model was selected for deployment.

###  Model Serialization

The final trained model was saved as:

model/model.pkl

Using:

pickle.dump()

##  ML API Integration (Flask)

The trained model is integrated into a Flask web application.

### API Workflow:

1. Load serialized model using `pickle.load()`  
2. Accept user input via HTML form  
3. Convert input into Pandas DataFrame  
4. Generate prediction using `model.predict()`  
5. Return result to frontend


##  Deployment

The application is deployed using:

- GitHub (Version Control)  
- Render (Cloud Hosting)  
- Gunicorn (Production WSGI Server)  


### Start Command Used:

gunicorn app:app

##  Tech Stack

- Python  
- Pandas  
- NumPy  
- Scikit-learn  
- Flask  
- HTML  
- CSS  
- Gunicorn  
- Render  

##  Project Structure

Machine_learning_model/
│
├── datasets/
│     └── babies.csv
├── model/
│     └── model.pkl
├── templates/
│     └── index.html
├── app.py
├── model_training.ipynb
├── requirements.txt

##  Author

Ramesh Kumar  
Data Science & Machine Learning Enthusiast
















