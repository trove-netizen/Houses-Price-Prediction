# 🏠 Houses Price Prediction with Machine Learning

This project demonstrates the use of various regression algorithms to predict house prices based on features such as zip code, area, number of rooms, longitude, and latitude. The goal is to train and evaluate models that can accurately forecast real estate prices using historical housing data.

---

## 📌 Objective

To build and evaluate machine learning regression models that estimate the price of a house based on key attributes. The project covers data preprocessing, model training, performance evaluation, and price prediction for new input data.

---

## 🛠️ Tools & Technologies

- **Programming Language:** Python  
- **Libraries:** 
  - pandas
  - numpy
  - matplotlib
  - seaborn
  - scikit-learn  
- **Models Used:**  
  - Random Forest Regressor  
  - Extra Trees Regressor  
  - Decision Tree Regressor  
- **Metrics:**  
  - R² Score  
  - Mean Absolute Error (MAE)  
  - Mean Squared Error (MSE)

---

## 📊 Dataset

The dataset is stored in `hosing.csv` and contains the following columns:
- `Zip` – Zip code of the house location
- `Area` – Total square area of the house
- `Room` – Number of rooms
- `Lon` – Longitude coordinate
- `Lat` – Latitude coordinate
- `Price` – Target variable, the actual price of the house

---

## 📁 Project Structure
houses-price-prediction/
├── hosing.csv # Dataset
├── housing_price_prediction.py # Main ML script
├── model_joblib_random.pkl # Saved Random Forest model
├── model_joblib_extral.pkl # Saved Extra Trees model
├── model_joblib_decision.pkl # Saved Decision Tree model
├── README.md # Project documentation
├── requirements.txt # Python dependencies



---

## 🧠 Machine Learning Workflow

1. **Load and Inspect Data**
   - Load CSV into a DataFrame
   - Check shape, null values, and types

2. **Data Preprocessing**
   - Separate features (`x`) and target (`y`)
   - Handle any missing values
   - Train-test split

3. **Model Training**
   - Fit Random Forest, Extra Trees, and Decision Tree regressors

4. **Model Evaluation**
   - Evaluate each model using:
     - R² Score
     - Mean Absolute Error (MAE)
     - Mean Squared Error (MSE)
   - Visual comparison of predictions vs actual prices

5. **New Prediction**
   - Input: {'Zip':1097, 'Area':109, 'Room':4, 'Lon':4.944774, 'Lat':52.343782}
   - Output: Predicted housing price

---

## 📈 Model Performance

Example metrics (your values may differ):

| Model           | R² Score | MAE      | MSE       |
|----------------|----------|----------|-----------|
| Random Forest  | 0.87     | 13240.50 | 310000000 |
| Extra Trees    | 0.86     | 14123.70 | 325000000 |
| Decision Tree  | 0.78     | 15890.10 | 400000000 |

---

## 📉 Visualization

The project includes `matplotlib` plots showing:
- Actual vs predicted housing prices for each model  
- Side-by-side comparison for easy interpretation

---

## 💾 Model Deployment

The best-performing models are saved using `joblib` for future use:

```python
import joblib

joblib.dump(random, 'model_joblib_random.pkl')

