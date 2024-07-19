Used Car Price Prediction
Project Overview
This project aims to build a regression model to predict the price of used cars in Saudi Arabia. The model leverages a dataset from Syarah.com and includes features such as car type, region, make, gear type, origin, options, manufacturing year, engine size, mileage, negotiable status, and price. The primary focus is on predicting prices below 300k SAR to help car seller companies offer competitively priced vehicles.

Table of Contents
Installation
Dataset
Features
Model
Hyperparameter Tuning
Usage
Results
Contributing
License
Installation
Clone the repository:

bash
Copy code
git clone https://github.com/yourusername/used-car-price-prediction.git
cd used-car-price-prediction
Create a virtual environment and activate it:

bash
Copy code
python -m venv venv
source venv/bin/activate   # On Windows, use `venv\Scripts\activate`
Install the required dependencies:

bash
Copy code
pip install -r requirements.txt
Dataset
The dataset used for this project is sourced from Syarah.com and includes the following features:

Type: Type of used car.
Region: The region in which the used car was offered for sale.
Make: The company name.
Gear_Type: Gear type of the used car.
Origin: Origin of the used car.
Options: Options of the used car.
Year: Manufacturing year.
Engine_Size: The engine size of the used car.
Mileage: Mileage of the used car.
Negotiable: Indicates if the price is negotiable (True if the price is 0).
Price: Used car price.
Features
The features used in the model include:

Type
Region
Make
Gear_Type
Origin
Options
Year
Engine_Size
Mileage
Negotiable
These features were selected based on their potential impact on the car's price and the availability of data.

Model
The regression model used for this project is based on XGBoost. XGBoost was chosen for its high performance and ability to handle large datasets efficiently.

Hyperparameter Tuning
GridSearchCV was used for hyperparameter tuning to find the best parameters for the XGBoost model. The parameter grid included a variety of settings to ensure the best possible model performance.

Usage
Preprocess the dataset by running the preprocessing script:

bash
Copy code
python preprocess.py
Train the model:

bash
Copy code
python train.py
Evaluate the model:

bash
Copy code
python evaluate.py
Make predictions:

bash
Copy code
python predict.py --input input_data.csv --output predictions.csv
Results
The model was evaluated on a test set, focusing on predicting prices below 300k SAR. The results showed a satisfactory performance with a balanced trade-off between bias and variance.

Contributing
Contributions are welcome! Please fork the repository and create a pull request with your changes. Ensure your code adheres to the project's coding standards and includes appropriate tests.
