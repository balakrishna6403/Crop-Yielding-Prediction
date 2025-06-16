🌾 Crop Yield Prediction using Machine Learning
Incorporating Meteorological Data and Pesticide Information to Forecast Crop Yields
📂 Project Structure

crop_yield_predictor/
├── backend/
│   ├── model/
│   │   ├── train_model.py
│   │   └── cleaned_crop_yield.csv
│   ├── main.py  ← FastAPI backend
│   └── best_model/
│       └── model.pkl
├── frontend/
│   ├── src/
│   │   └── YieldForm.js
├── README.md
    
📦 Requirements
🔧 Python Dependencies (Backend)
Install using pip:
Install all packages using the following command:

bash
pip install -r requirements.txt

- pandas – Data manipulation  
- numpy – Numerical computing  
- scikit-learn – Preprocessing, modeling, evaluation  
- xgboost – Advanced regression algorithm  
- fastapi – Backend web framework  
- uvicorn – ASGI server for FastAPI

🖥️ Node Packages (Frontend)
In your frontend folder:
npm install
npm install axios framer-motion

- axios – HTTP requests  
- framer-motion – Animations  
- react – Web UI

🚀 Execution Steps
1️⃣ Train the ML Model
Navigate to the backend model folder and run:
python train_model.py

This script:
- Loads the dataset (cleaned_crop_yield.csv)
- Preprocesses the data (scaling, encoding)
- Trains XGBoost and Random Forest
- Evaluates models (R², MAE, RMSE)
- Saves the best model as model.pkl
  
2️⃣ Start FastAPI Backend
Navigate to the backend directory:
uvicorn main:app --reload
The API will be available at http://localhost:8000/predict

3️⃣ Run React Frontend
Navigate to the frontend directory:
npm start
This starts your UI on http://localhost:3000

📊 Features
- React frontend with dropdown-based data entry
- FastAPI backend with trained ML model
- XGBoost/Random Forest regression model
- Smart fertilizer and pesticide recommendations
- Real-time prediction display

📌 Notes
- The dataset is sourced from: Kaggle - Indian Crop Yield Dataset
- Predictions are based on cleaned and engineered features
- You can retrain the model anytime by modifying and re-running train_model.py

