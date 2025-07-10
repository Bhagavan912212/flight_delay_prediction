# ✈️ Flight Delay Prediction

A web application that predicts flight arrival delays using a machine learning model. This tool helps travelers, airlines, and analysts estimate the likelihood and extent of flight delays based on flight details.

---

## 🚀 Example Use Case

Suppose you are planning to travel from New York (JFK) to Los Angeles (LAX) on Delta Airlines, flight number 1234, scheduled to depart on **July 15, 2025, at 10:30 AM**.  
You want to know if your flight is likely to be delayed and by how much.

**With this application, you can enter:**
- **Origin Airport:** JFK
- **Destination Airport:** LAX
- **Airline:** Delta
- **Flight Number:** 1234
- **Date:** 2025-07-15
- **Scheduled Departure Time:** 10:30

The app will process your input, use a trained machine learning model, and display a prediction such as:
- **Predicted Delay:** 18 minutes
- **Status:** Short Delay

---

## 🛠️ How It Works

1. **User Input:** Enter flight details in the web form.
2. **Prediction:** The app uses a machine learning model to estimate the delay.
3. **Result:** The predicted delay and its category (On Time, Short Delay, etc.) are shown.

---

## 📁 Project Structure

```
project/
│
├── data/
│   ├── airlines.csv
│   ├── airports.csv
│   └── flights.csv
│
├── notebooks/
│   ├── app.py                # Main Flask application
│   └── templates/
│       ├── index.html        # Home page form
│       ├── result.html       # Prediction result page
│       └── error.html        # Error display page
│
├── notebooks/flight_delay_regressor.pkl    # Trained ML model (Git LFS)
├── notebooks/label_encoders.pkl            # Label encoders (Git LFS)
│
└── .vscode/
    └── launch.json           # VS Code launch configuration
```

---

## ⚡ Getting Started

### Prerequisites

- Python 3.7+
- pip
- [Git LFS](https://git-lfs.github.com/) (for model files)

### Installation

1. **Clone the repository:**
    ```bash
    git clone git https://github.com/Bhagavan912212/flight_delay_prediction.git
    cd flight_delay_prediction
    ```

2. **Install dependencies:**
    ```bash
    pip install flask pandas numpy joblib
    ```

3. **(If using Git LFS) Pull large files:**
    ```bash
    git lfs install
    git lfs pull
    ```

4. **Run the application:**
    ```bash
    python notebooks/app.py
    ```

5. **Open your browser and go to:**  
   [http://localhost:8080](http://localhost:8080)

---

## 📊 Model Details

- Trained on historical flight data.
- Uses features like year, month, day, flight number, airline, origin, destination, distance, and scheduled departure time.
- Categorical features are encoded using label encoders.
- Output: Predicted delay in minutes, categorized for clarity.

---

## 🧩 Customization

- **Web Interface:** Modify HTML templates in `notebooks/templates/`.
- **Model:** Retrain and replace `flight_delay_regressor.pkl` and update `label_encoders.pkl` as needed.
- **Data:** Update or replace CSV files in the `data/` directory for further analysis or retraining.

---

## 📄 License

This project is for educational and demonstration purposes.
