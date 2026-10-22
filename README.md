ML & Data Engineering Mini-Pipeline 

This project demonstrates the integration of Data Engineering (DE) and Machine Learning (ML) practices through a modular Python application. It serves as an example of clean architecture for automated data validation and training a linear regression model.

Project Architecture

The project is divided into two independent, modular layers following OOP (Object-Oriented Programming) principles:

ml-de-mini-pipeline/
│
├── data/
│   └── dataset.csv             # Input dataset
│
├── src/
│   ├── __init__.py             # Package initialization
│   ├── data_pipeline.py        # DE Layer: Data validation and cleaning
│   └── ml_trainer.py           # ML Layer: Model training and evaluation
│
├── main.py                     # Main execution entry point
├── requirements.txt            # Project dependencies
├── .gitignore                  # Git ignore rules
└── README.md                   # Project documentation


Features & Components

1. Data Engineering Layer (DataPipeline)

File Existence Check: Prevents application crash if the input file is missing.

Schema Validation: Verifies the presence of all required columns.

Data Type Enforcement: Automatically casts columns to numeric types.

Missing Value Handling: Fills empty (NaN) fields with the column mean.

2. Machine Learning Layer (MLModelTrainer)

Data Splitting: Splits dataset into training (80%) and testing (20%) sets via train_test_split.

Model Training: Uses LinearRegression from scikit-learn.

Evaluation: Calculates Mean Squared Error (MSE) and R² Score.

Inference: Provides a dedicated method for single-value predictions on new data.

 Getting Started

1. Clone the repository

git clone https://github.com/YOUR_USERNAME/ml-de-mini-pipeline.git
cd ml-de-mini-pipeline


2. Create and activate a virtual environment

# Windows
python -m venv .venv
.venv\Scripts\activate

# Linux / MacOS
python3 -m venv .venv
source .venv/bin/activate


3. Install dependencies

pip install -r requirements.txt


4. Run the pipeline

python main.py


Sample Output (Terminal)

--- 1. DE Sloj: Pokretanje validacije i čišćenja podataka ---
Validacija uspešna: Podaci su čisti i šema je ispravna.

--- 2. ML Sloj: Trening i evaluacija modela ---
Model je uspešno istreniran.
Koeficijent nagiba (Slope): 7.45
Presek (Intercept): 41.20
Mean Squared Error (MSE): 4.15
R2 Score: 0.95

[Test Predviđanja] Za učeno vreme od 5.5h, predviđena ocena je: 82.18


Tech Stack

Language: Python 3.8+

Data Processing: Pandas

Machine Learning: Scikit-Learn
