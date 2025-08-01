# Smart Irrigation System ML Project

This project uses machine learning to predict and visualize the activation of irrigation pumps for three farm parcels based on sensor data.

## Project Structure

- `Irrigation_System.ipynb` – Main Jupyter notebook for data analysis, model training, evaluation, and visualization.
- `irrigation_machine.csv` – Dataset containing sensor readings and parcel activation labels.
- `Farm_Irrigation_System.pkl` – Saved trained model (RandomForest-based MultiOutputClassifier).
- `app.py` – (Optional) Application script for deploying or using the trained model.

## Workflow Overview

1. **Data Loading & Preprocessing**
   - Loads `irrigation_machine.csv` using pandas.
   - Drops unnecessary columns (e.g., `Unnamed: 0`).
   - Splits data into features (`sensor_0` to `sensor_19`) and labels (`parcel_0`, `parcel_1`, `parcel_2`).
   - Scales features using MinMaxScaler.

2. **Model Training**
   - Splits data into train/test sets.
   - Trains a RandomForest-based MultiOutputClassifier to predict parcel activation.

3. **Evaluation**
   - Prints classification report for each parcel.
   - Visualizes parcel and pump activation over time.

4. **Model Saving**
   - Saves the trained model as `Farm_Irrigation_System.pkl` using joblib.

## How to Run

1. Open `Irrigation_System.ipynb` in Jupyter or VS Code.
2. Run all cells to execute the workflow.
3. The notebook will output evaluation metrics and plots.

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

- Use the notebook for experimentation and visualization.
- Load `Farm_Irrigation_System.pkl` in your application (e.g., `app.py`) for predictions on new sensor data.

## Data Format

- **Features:** `sensor_0` to `sensor_19` (float values)
- **Labels:** `parcel_0`, `parcel_1`, `parcel_2` (binary: 0=OFF, 1=ON)

## License

This project is for educational purposes.