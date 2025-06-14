# Netflix Data Cleaning

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg) ![License](https://img.shields.io/badge/License-MIT-green.svg)

## Overview
This project demonstrates data cleaning and exploratory data analysis (EDA) on the Netflix titles dataset using Python in a Jupyter Notebook. The goal is to prepare the dataset for analysis by addressing missing values, duplicates, and inconsistent formats, enabling insights into Netflix’s movie and TV show catalog.

**Dataset**: [Netflix Movies and TV Shows](https://www.kaggle.com/datasets/shivamb/netflix-shows) by Shivam Bansal, containing ~8,800 rows with columns: `show_id`, `type`, `title`, `director`, `cast`, `country`, `date_added`, `release_year`, `rating`, `listed_in`, `description`.

**Skills Demonstrated**:
- Data cleaning with pandas
- Handling missing values and standardizing formats
- Feature engineering (e.g., extracting years, splitting genres)
- Visualization with seaborn and matplotlib
- Reproducible Jupyter Notebook workflow

## Table of Contents
- [Features](#features)
- [Cleaning Steps](#cleaning-steps)
- [File Structure](#file-structure)
- [How to Use](#how-to-use)
- [Installation](#installation)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)
- [Acknowledgments](#acknowledgments)

## Features
- **Comprehensive Cleaning**: Addresses missing values, duplicates, and format inconsistencies.
- **Documented Process**: Markdown cells explain each step and its rationale.
- **Reproducible**: Runs in Google Colab or locally with the provided dataset.
- **Visual Insights**: Includes plots like missing value heatmaps and release year distributions.

## Cleaning Steps
1. **Loaded Data**: Imported the dataset using `pandas.read_csv()`.
2. **Explored Data**: Used `df.info()` and `df.isnull().sum()` to identify issues (~30% missing in `director`, 9% in `cast`, `country`).
3. **Handled Missing Values**:
   - Filled `director`, `cast`, and `country` with "Unknown".
   - Dropped rows with missing `title` or `date_added`.
4. **Removed Duplicates**: Dropped duplicates based on `title`.
5. **Standardized Formats**:
   - Converted `date_added` to datetime.
   - Normalized text in `title` and `listed_in`.
6. **Corrected Data Types**:
   - Ensured `release_year` is an integer.
   - Extracted numeric `duration` (minutes for movies, seasons for shows).
7. **Feature Engineering**:
   - Added `year_added` and `month_added` from `date_added`.
   - Split `listed_in` into genre lists.
8. **Visualizations**: Created heatmaps and histograms (e.g., release year distribution).
9. **Saved Output**: Exported cleaned data to `netflix_cleaned.csv`.

See [NETFLIX_DATA_CLEANING.ipynb](NETFLIX_DATA_CLEANING.ipynb) for details.

## File Structure

EDA-NETFLIX-/├── README.md├── NETFLIX_DATA_CLEANING.ipynb├── netflix_titles.csv          # Original dataset├── netflix_cleaned.csv         # Cleaned dataset (optional)└── requirements.txt            # Dependencies

## How to Use
1. **Run in Colab**:
   - Open: [Netflix Data Cleaning](https://colab.research.google.com/drive/18MUm8D4bfSzqY-uEf59QabnbqfYrMJHL?usp=sharing).
   - Click “Copy to Drive” to edit.
   - Execute cells to run cleaning and view plots.
2. **Run Locally**:
   - Download `NETFLIX_DATA_CLEANING.ipynb` and `netflix_titles.csv`.
   - Install dependencies (see [Installation](#installation)).
   - Open in Jupyter: `jupyter notebook NETFLIX_DATA_CLEANING.ipynb`.
3. **Access the Dataset**:
   - Use `netflix_titles.csv` from the repo or download from [Kaggle](https://www.kaggle.com/datasets/shivamb/netflix-shows).
   - Alternatively, load via:
     ```python
     url = 'https://raw.githubusercontent.com/Sharath432/EDA-NETFLIX-/main/netflix_titles.csv'
     df = pd.read_csv(url)
     ```

## Installation
For local execution:
1. Install Python 3.8+.
2. Install dependencies:
   ```bash
   pip install -r requirements.txt


Install Jupyter Notebook:pip install jupyter


Run the notebook:jupyter notebook NETFLIX_DATA_CLEANING.ipynb



requirements.txt:
pandas==1.5.3
numpy==1.24.3
seaborn==0.12.2
matplotlib==3.7.1

Results

Cleaned Dataset: Reduced missing values by ~90%, standardized formats, and added features like year_added.
Insights: Ready for analyzing trends (e.g., content growth by year, genre distribution).
Output: netflix_cleaned.csv contains the processed dataset.

Contributing
Contributions are welcome! To contribute:

Fork the repository.
Create a branch: git checkout -b feature/new-cleaning-step.
Commit changes: git commit -m "Add cleaning for ratings".
Push: git push origin feature/new-cleaning-step.
Open a pull request.

Please follow the code of conduct.
License
This project is licensed under the MIT License. See LICENSE for details.
Acknowledgments

Dataset: Netflix Movies and TV Shows by Shivam Bansal.
Inspiration: Kaggle community and data science tutorials.
Created by Sharath432 (https://github.com/Sharath432).

Contact
For questions or feedback, please open an issue on this repository or contact the project maintainer at [rsarath16new@gmail.com].
