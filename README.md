# 🎵 Music Metadata: Track Count Prediction

## 📄 Overview

This take-home assignment is designed for a **junior data engineer** role. You'll work with a real-world music metadata dataset to:

- Perform data cleaning and transformation
- Create a reproducible ETL pipeline
- Train a basic regression model to predict the number of tracks on a release

**Estimated time**: 1 to 2 hours

---

## 📅 Dataset

Use the [Records: A Comprehensive Music Metadata Dataset](https://www.kaggle.com/datasets/fleshmetal/records-a-comprehensive-music-metadata-dataset) from Kaggle.

Download the dataset and extract the file `records.csv` into the root of your project directory.

---

## 🔧 Task Breakdown

### 1. 📊 Data Cleaning & Transformation (ETL)

Use either the provided `etl_script.py` or a Jupyter notebook to perform the following:

- Load `records.csv` using `pandas`
- Remove rows with missing `artist_name`, `release_name`, or `track_count`
- Parse the `release_date` into a new column called `release_year`
- Clean and normalize the `genres` column:
  - Remove brackets and quotes
  - Convert to lowercase
  - Split into list
- Create a new column `num_genres` representing the number of genres per release
- Drop duplicates
- Save the cleaned data to a file called `cleaned_music_metadata.csv`

---

### 2. 🤖 Model Training: Predict `track_count`

Train a regression model using the cleaned dataset.

#### Target Variable:
- `track_count`

#### Suggested Features:
- `release_year`
- `num_genres`

#### Choose ONE regression model from `scikit-learn`:
- `LinearRegression`
- `DecisionTreeRegressor`
- `RandomForestRegressor`

#### Evaluation:
- Split the data into training and testing sets (e.g., 80/20 split)
- Report:
  - **Mean Absolute Error (MAE)**
  - **R² score**
- (Optional) Plot actual vs predicted `track_count`

All modeling work should be done in `model_training.ipynb`.

---
## 📦 Dependency Management (Required)

Please include a `requirements.txt` file listing all the libraries needed to run your ETL and modeling code.
---

## 📦 Deliverables

Please submit a GitHub repository or zipped folder with the following contents:

<yourfullname>-music-track-count-assignment/
├── records.csv                   # Raw input from Kaggle
├── etl_script.py                 # OR etl_notebook.ipynb
├── model_training.ipynb         # Your ML notebook
├── cleaned_music_metadata.csv   # Output of your ETL process
└── README.md                    # This file

---

## 🚀 Bonus (Optional)

- Use `argparse` in your ETL script to allow configurable input/output paths
- Add a helper test function (e.g., `test_clean_genres()`)
- Plot feature importances from your trained model

---

## 📚 Allowed Tools

- Python 3.x
- `pandas`, `numpy`
- `scikit-learn`
- `matplotlib` / `seaborn`
- `ChatGPT` / `Cursor` / `Or any other AI tool`

---

## 💡 Tips

- Focus on writing clean, well-documented code
- You do not need to perform hyperparameter tuning
- Explain your decisions in markdown cells within notebooks

Good luck and have fun! 🎧