# Used Car Price Prediction Application

![image](https://github.com/user-attachments/assets/8cffb0b4-5f1c-4a27-bd13-5a25f9dd1127)


## Overview

The **Used Car Price Prediction Application** is an interactive web tool built with Streamlit that allows users to predict the market price of used cars based on their brand/model, age, and mileage. This application uses machine learning (linear regression) to analyze historical car sales data and generate accurate price predictions.

## Features

### 💻 Interactive Web Interface
- Modern, responsive design
- Intuitive controls for entering car details
- Real-time price predictions

### 🤖 Machine Learning Powered
- Multiple linear regression model
- Feature importance analysis
- Model accuracy metrics

### 📊 Data Visualization
- Price distribution charts
- Similar cars comparison
- Model performance visualization

## Screenshots

### Price Prediction Results

![image](https://github.com/user-attachments/assets/19f16f37-66e3-426e-9178-27d1a5060227)
*A sample price prediction showing the estimated price and where it falls in the market distribution*

### Data Exploration View

![image](https://github.com/user-attachments/assets/ef817f75-bd9a-4fc8-8443-867ea97c3ce5)
*The correlation heatmap showing relationships between car features and price*

## Installation

### Prerequisites
- Python 3.7+
- pip package manager

### Setup Instructions

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/used-car-price-prediction.git
   cd used-car-price-prediction
   ```

2. **Create a virtual environment (recommended)**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install required packages**
   ```bash
   pip install -r requirements.txt
   ```

4. **Prepare your data**
   - Place your `used_cars_data.csv` file in the `data/` directory
   - Ensure it has columns for `Name`, `Year`, `Mileage`, and `Price`

5. **Run the application**
   ```bash
   streamlit run app.py
   ```

6. **Access the application**
   - Open your web browser and go to http://localhost:8501

## Data Format

The application expects a CSV file with the following structure:

| Name           | Year | Mileage      | Price |
|----------------|------|--------------|-------|
| Toyota Corolla | 2018 | 20.5 kmpl    | 9.75  |
| Honda City     | 2016 | 18.2 kmpl    | 8.5   |
| Maruti Swift   | 2020 | 23.7 kmpl    | 7.2   |
| ...            | ...  | ...          | ...   |

## How It Works

### 1. Data Processing
- Extracting numerical values from mileage data
- Calculating car age from manufacturing year
- Encoding car names/brands for machine learning

### 2. Model Training
- Building a multiple linear regression model
- Evaluating model performance with R² score
- Analyzing feature importance

### 3. Price Prediction
![image](https://github.com/user-attachments/assets/871a0462-6544-45dc-8254-99d23d5b7f50)

## Model Explanation

The application uses a multiple linear regression model with the following formula:

```
Price = (β₁ × Brand) + (β₂ × Age) + (β₃ × Mileage) + Intercept
```

Where:
- **Brand** is encoded as a numerical value representing brand reputation
- **Age** is the car's age in years (current year - manufacturing year)
- **Mileage** is fuel efficiency in kilometers per liter
- **β₁, β₂, β₃** are coefficients learned by the model
- **Intercept** is the base price when all other factors are zero

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- Data sourced from [your data source]
- Built with [Streamlit](https://streamlit.io/)
- Powered by [scikit-learn](https://scikit-learn.org/)

---

### Contact

For questions or support, please contact mohammedaazam757@gmail.com
