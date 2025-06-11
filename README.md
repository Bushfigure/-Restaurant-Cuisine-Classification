# A Restaurant Ratings Predictor
![Image](https://github.com/user-attachments/assets/4547ee31-77ce-448d-857b-52c9ae658d82)

## About Dataset

Introduction:
This dataset is designed for developing a machine learning model to classify restaurants based on their cuisines. 
It includes various attributes related to restaurants such as location, average cost, ratings, and services offered. 
The primary objective is to predict the cuisine type of a restaurant using these attributes.

Attributes:

1. Restaurant ID: Unique identifier for each restaurant.
2. Restaurant Name: Name of the restaurant.
3. Country Code: Country code where the restaurant is located.
4. City: City where the restaurant is situated.
5. Address: Address of the restaurant.
6. Locality: General locality of the restaurant.
7. Locality Verbose: Detailed locality description.
8. Longitude: Longitude coordinate of the restaurant's location.
9. Latitude: Latitude coordinate of the restaurant's location.
10. Cuisines: Type of cuisines offered by the restaurant (target variable).
11. Average Cost for Two: Average cost for two people dining at the restaurant.
12. Currency: Currency used for pricing.
13. Has Table Booking: Binary variable indicating if the restaurant accepts table bookings.
14. Has Online Delivery: Binary variable indicating if the restaurant offers online delivery.
15.Is Delivering Now: Binary variable indicating if the restaurant is currently delivering.
16. Switch to Order Menu: Binary variable indicating if the restaurant has an online menu ordering option.
17. Price Range: Range indicating the price level of the restaurant's menu items.
18. Aggregate Rating: Average rating of the restaurant based on customer reviews.
19. Rating Color: Color code representing the rating level.
20. Rating Text: Textual representation of the rating level.
21. Votes: Total number of votes received by the restaurant.

# Methodology

This project follows a structured pipeline for end-to-end machine learning development:

## Exploratory Data Analysis (EDA)

Objective: Understand feature distributions, relationships, and target behavior.

Steps Taken:

1. Loaded and inspected the dataset shape, types, and summary statistics.

2. Visualized numeric features like average_cost_for_two using histograms.

3. Plotted count distributions of categorical features like online_order, book_table, and price_range.

Used a heatmap to check correlations and potential multicollinearity.

 ## Data Cleaning

Actions:

Removed null values and duplicates.

Verified data types and corrected them as needed (e.g., price range as integer).

## Data Transformation

Encoding:

1. online_order, book_table: Binary encoding (Yes → 1, No → 0)

2. price_range: Retained as ordinal (1 to 4)

Scaling:

Applied StandardScaler to numerical features.

Saved the scaler using joblib (Scaler.pkl) for consistent preprocessing in deployment.

## Feature Engineering
Final Feature Set:

average_cost_for_two

book_table (encoded)

online_order (encoded)

price_range

These features were chosen based on domain intuition and correlation analysis.

## Model Training
Workflow:

Split data into training and testing sets.

Trained a regression model (please confirm: was it RandomForestRegressor, LinearRegression, etc.?).

Evaluated using metrics like RMSE and R².

Saved the trained model as mlmodel.pkl.

## Results & Discussion
 
Model Performance
Metrics: 

1. R² Score: 

2. RMSE: 

3. MAE: 

## Web App Features
The Streamlit app allows users to input:

Estimated average cost

Whether the restaurant offers table booking

Whether it supports online delivery

Price range (1 = Cheapest, 4 = Most Expensive)

The app:

Transforms inputs using Scaler.pkl

Predicts rating with mlmodel.pkl

## Conclusion
The dataset was thoroughly cleaned and preprocessed.

A regression model was trained to effectively predict restaurant ratings.

The model was deployed via a user-friendly Streamlit interface.

This project demonstrates the full pipeline from EDA to Deployment.
