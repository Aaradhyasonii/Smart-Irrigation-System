# Week 2
# Farm Irrigation System - Machine Learning Project

This project uses machine learning to predict the activation of irrigation parcels (sprinklers/pumps) based on sensor data. The workflow includes data preprocessing, model training, evaluation, and visualization.

## Project Structure

- `Irrigation_System.ipynb` - Main Jupyter notebook containing all code for data processing, model training, evaluation, and visualization.
- `irrigation_machine.csv` - Dataset containing sensor readings and parcel activation labels.
- `Farm_Irrigation_System.pkl` - Saved trained model for future inference.

## How It Works

1. **Data Loading & Preprocessing**
   - Loads data from `irrigation_machine.csv`.
   - Drops unnecessary columns and scales sensor features using MinMaxScaler.

2. **Feature & Label Definition**
   - Features: First 20 columns (sensor_0 to sensor_19).
   - Labels: Last 3 columns (`parcel_0`, `parcel_1`, `parcel_2`).

3. **Model Training**
   - Splits data into training and test sets.
   - Trains a `MultiOutputClassifier` with a `RandomForestClassifier` (custom hyperparameters).

4. **Evaluation**
   - Evaluates the model using a classification report.

5. **Visualization**
   - Plots parcel activation and pump activity over time.

6. **Model Saving**
   - Saves the trained model as `Farm_Irrigation_System.pkl` using `joblib`.

## Requirements

- Python 3.12+
- pandas
- matplotlib
- seaborn
- scikit-learn
- joblib

Install dependencies with:
```sh
pip install pandas matplotlib seaborn scikit-learn joblib
```

## Usage

1. Open `Irrigation_System.ipynb` in Jupyter Notebook or VS Code.
2. Run all cells to preprocess data, train the model, evaluate, visualize, and save the model.

## Notes

- Update the dataset filename in the notebook if your CSV is named differently.
- The model is saved as `Farm_Irrigation_System.pkl` for later use.

---