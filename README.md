# LogicDepthAI

## Overview
This project predicts the **combinational logic depth** of a signal in an **RTL module** without running full synthesis. It uses a **Random Forest model** trained on RTL signal data extracted from synthesis reports.

## Prerequisites
To run this project, you need:
- Python 3.x
- Required libraries:
  - `scikit-learn`
  - `pandas`
  - `numpy`
  - `pickle`

## Setting Up the Environment

1. **Create a virtual environment:**
2. **Install dependencies:**

## Running the Code

### **Step 1: Load the Model**
Ensure the trained **Random Forest model** (`final_random_forest_model.pkl`) is in the project directory.

### **Step 2: Run the Prediction Script**
Execute the script to predict logic depth:
```sh
python rtl.py
```

### **Step 3: Input New RTL Signal Data**
Modify `rtl.py` to add new RTL signal data before running.

### **Step 4: View Predictions**
The script outputs predicted **logic depth** for given RTL signals.

## Project Structure
```
├── final_random_forest_model.pkl  # Trained model
├── rtl.py                     # Script to load model & predict
├── rtl_dataset.csv                    # Training dataset (if available)
├── README.md                      # This file
```

## Future Improvements
- Support for **multiple machine learning models**.
- Better **data preprocessing** to improve accuracy.
- Integration with a **web-based interface** for easy predictions.



