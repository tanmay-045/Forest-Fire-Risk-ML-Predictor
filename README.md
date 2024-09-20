## Algerian Forest Fire FWI Prediction

This web application predicts the Fire Weather Index (FWI) for Algerian forest fires using a machine learning model. The FWI is an important metric used to estimate the risk of forest fires, based on several environmental factors.

https://github.com/user-attachments/assets/b00438a6-4662-4a59-aa1f-9c53f8288dbe

### Aim 

*to predict the Fire Weather Index (FWI), a critical indicator used in fire management to assess the likelihood of fire spread and intensity.*

### Dataset Description

The dataset contains observations of forest fires in Algeria, along with various meteorological features that influence fire activity. Key features include:
- **Temperature**
- **Relative Humidity (RH)**
- **Wind Speed (Ws)**
- **Rain**
- **Fine Fuel Moisture Code (FFMC)**
- **Drought Code (DMC)**
- **Initial Spread Index (ISI)**
- **Classes**: Fire severity classification
- **Region**: Specific regions in Algeria

### Machine Learning Approach

I used Ridge Regression, a regularized linear regression model, to predict the FWI. Here’s how I approached the problem:
1. **Data Preprocessing**: The data was scaled using `StandardScaler` to ensure all features contribute proportionally to the model.
2. **Model Selection**: Ridge Regression was chosen due to its effectiveness in handling multicollinearity and regularization, which prevents overfitting.
3. **Flask Integration**: The trained model was saved using `pickle` and integrated into a Flask web application. The app allows users to input the environmental parameters, which are then scaled and passed to the Ridge regression model to predict the FWI.

The app consists of two main components:
- **Frontend**: A simple HTML form where users can input their data.
- **Backend**: Flask handles the requests, performs scaling and predictions, and displays the results.

### What Does This App Achieve?

This app provides a quick and easy way for users to estimate the Fire Weather Index based on real-time meteorological data. By predicting FWI, fire management authorities and concerned agencies can take preventive measures to mitigate fire risks.

### How to Use the App?

1. Clone the repository and install the necessary dependencies.
    ```bash
    git clone https://github.com/tanmay-045/Forest-Fire-Risk-ML-Predictor.git
    cd <repository-folder>
    pip install -r requirements.txt
    ```
2. Run the Flask app.
    ```bash
    python application.py
    ```
3. Access the app in your browser at `http://127.0.0.1:5000/`.
