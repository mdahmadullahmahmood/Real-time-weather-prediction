This project is a Python-based weather prediction application that fetches current weather data using the OpenWeatherMap API and predicts future weather conditions, including temperature, humidity, and rain probability. It uses historical weather data to train machine learning models (Random Forest Classifier for rain prediction and Random Forest Regressor for temperature and humidity forecasting). The project is implemented in a Jupyter Notebook.

Features:
1-Current Weather Data: Fetches real-time weather data for any city using the OpenWeatherMap API.
2-Rain Prediction: Uses a Random Forest Classifier to predict whether it will rain based on historical weather data.
3-Temperature and Humidity Forecasting: Employs Random Forest Regressor to predict future temperature and humidity for the next five hours.
4-Data Preprocessing: Handles missing values, duplicates, and categorical data encoding for robust model training.
5-User-Friendly Output: Displays current weather details and future predictions in a clear format.

Prerequisites:
To run this project, you need the following:
Python 3.6 or higher
Jupyter Notebook or JupyterLab
An active internet connection for API requests


Usage:
Run the weather_view() function in the notebook.
When prompted, enter the name of a city (e.g., Kyiv).
The program will:
Fetch current weather data for the specified city.
Train machine learning models using the historical data.
Display current weather details (temperature, humidity, etc.).
Predict the likelihood of rain.
Provide temperature and humidity forecasts for the next five hours.
An OpenWeatherMap API key (sign up at OpenWeatherMap to get one)

How It Works:
Data Fetching: Uses the OpenWeatherMap API to retrieve current weather data (temperature, humidity, wind speed, etc.) for the user-specified city.
Historical Data Processing: Reads a CSV file containing historical weather data, removes missing values and duplicates, and encodes categorical variables (e.g., WindGustDir, RainTomorrow) using LabelEncoder.
Rain Prediction: Trains a Random Forest Classifier to predict whether it will rain based on features like temperature, humidity, and wind speed.
Temperature and Humidity Forecasting: Uses Random Forest Regressor models to predict future temperature and humidity values based on historical trends.
Output: Combines current weather data with predictions and displays them in a user-friendly format.

Notes:
Ensure your weather.csv file has the required columns and consistent data to avoid errors during model training.
The API key must be valid and active to fetch current weather data.
The project assumes the timezone Asia/Karachi for future prediction timestamps. Modify the timezone variable in the weather_view function if needed.

Future Improvements:
Add support for multiple cities in a single run.
Incorporate more advanced weather features (e.g., cloud cover, precipitation amount).
Implement visualization of predictions using libraries like Matplotlib or Seaborn.
Add error handling for invalid city names or API failures.
