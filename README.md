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
   ```sh
   python -m venv rtl_env
   source rtl_env/bin/activate  # On Windows use: rtl_env\Scripts\activate
   ```

2. **Install dependencies:**
   ```sh
   pip install -r requirements.txt
   ```
   If `requirements.txt` is missing, manually install dependencies:
   ```sh
   pip install scikit-learn pandas numpy pickle-mixin
   ```

## Running the Code

### **Step 1: Load the Model**
Ensure the trained **Random Forest model** (`final_random_forest_model.pkl`) is in the project directory.

### **Step 2: Run the Prediction Script**
Execute the script to predict logic depth:
```sh
python predict.py
```

### **Step 3: Input New RTL Signal Data**
Modify `predict.py` to add new RTL signal data before running.

### **Step 4: View Predictions**
The script outputs predicted **logic depth** for given RTL signals.

## Project Structure
```
├── final_random_forest_model.pkl  # Trained model
├── predict.py                     # Script to load model & predict
├── dataset.csv                    # Training dataset (if available)
├── README.md                      # This file
├── requirements.txt                # Required dependencies
```

## Troubleshooting
### **Common Errors & Fixes**
1. **FileNotFoundError: No such file or directory: 'final_random_forest_model.pkl'**
   - Ensure the `.pkl` file exists in the same directory.
2. **ModuleNotFoundError: No module named 'sklearn'**
   - Install missing dependencies: `pip install scikit-learn`
3. **KeyError: 'logic_depth' not found in axis**
   - Check if `dataset.csv` is properly formatted with expected column names.

## Future Improvements
- Support for **multiple machine learning models**.
- Better **data preprocessing** to improve accuracy.
- Integration with a **web-based interface** for easy predictions.



