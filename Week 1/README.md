# Smart_Irrigation_AICTE_Shell
This is an AICTE Internship Cycle 2
# Smart Irrigation

This project is part of the AICTE Internship Cycle 2 and demonstrates a machine learning approach to smart irrigation using sensor data.

## Project Structure

- `irrigation_machine.csv`: Dataset containing sensor readings and irrigation labels.
- `Irrigation_System.ipynb`: Jupyter notebook for data analysis, preprocessing, and model training.

## Workflow

1. **Data Loading**: The dataset is loaded using pandas.
2. **Exploration**: Initial exploration includes viewing the first few rows, checking info, and statistics.
3. **Preprocessing**: Unnecessary columns are dropped, and features/labels are defined.
4. **Feature Selection**: Sensor data (columns 0-19) are used as features.
5. **Label Selection**: Columns 20 onwards are used as labels for multi-output classification.
6. **Modeling**: Random Forest Classifier is used for prediction.
7. **Evaluation**: Model performance is evaluated using classification metrics.

## Usage

Open `Irrigation_System.ipynb` in Jupyter or VS Code and run the cells to reproduce the analysis and model training.

## Requirements

- Python 3.x
- pandas
- matplotlib
- seaborn
- scikit-learn
- joblib

Install dependencies with:

```sh
pip install pandas matplotlib seaborn scikit-learn joblib