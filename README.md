# 📈 Advertising Sales Prediction

A comprehensive machine learning project for predicting product **sales** based on advertising spend across **TV**, **Radio**, and **Newspaper** channels. This project includes exploratory data analysis, feature engineering, model comparison, and an interactive **Power BI** dashboard.

![Dashboard Preview](Dashboard/image.png)

## 📋 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Project Structure](#project-structure)
- [Dataset](#dataset)
- [Technologies Used](#technologies-used)
- [Installation](#installation)
- [Usage](#usage)
- [Model Performance](#model-performance)
- [Dashboard](#dashboard)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)
- [Author](#author)
- [Acknowledgments](#acknowledgments)

<a id="overview"></a>
## 🎯 Overview

This project aims to predict **Sales** based on advertising budgets in TV/Radio/Newspaper. It follows a complete ML pipeline from data exploration to feature engineering, training multiple regression models, and comparing performance.

<a id="features"></a>
## ✨ Features

- **Comprehensive EDA**: Exploratory analysis with visualizations (distributions, correlations, relationships)
- **Data Cleaning**: Remove index-like column (`Unnamed: 0`), check missing values and duplicates
- **Multiple ML Models**: Linear Regression, Decision Tree Regressor, and Support Vector Regression (SVR)
- **Feature Engineering**: Create an interaction feature `TV_Radio = TV * Radio`
- **Model Evaluation**: MAE, RMSE, and R²
- **Interactive Dashboard**: Power BI dashboard file + preview image

<a id="project-structure"></a>
## 📁 Project Structure

```text
CodeAlpha_Advertising_Sales_Prediction/
│
├── Dataset/
│   └── Advertising.csv          # Advertising spend + sales dataset
│
├── Dashboard/
│   ├── Advertising.pbix         # Power BI dashboard file
│   └── image.png                # Dashboard preview image
│
├── notebook.ipynb               # Main Jupyter notebook (EDA + models)
├── requirements.txt             # Python dependencies
└── README.md                    # Project documentation
```

<a id="dataset"></a>
## 📊 Dataset

The dataset contains **200 records** with the following columns:

- **TV**: TV advertising budget
- **Radio**: Radio advertising budget
- **Newspaper**: Newspaper advertising budget
- **Sales**: Target variable (sales)

> Note: the raw CSV includes an index-like column (`Unnamed: 0`) which is removed in the notebook.

<a id="technologies-used"></a>
## 🛠️ Technologies Used

- **Python 3.x**
- **Pandas**: Data manipulation and analysis
- **NumPy**: Numerical computing
- **Matplotlib**: Data visualization
- **Seaborn**: Statistical data visualization
- **Scikit-learn**: Machine learning models and evaluation
- **Jupyter Notebook**: Interactive development environment
- **Power BI**: Dashboard creation and visualization

<a id="installation"></a>
## 📦 Installation

1. **Clone the repository**

```bash
git clone <repository-url>
cd CodeAlpha_Advertising_Sales_Prediction
```

2. **(Recommended) Create and activate a virtual environment**

```bash
python -m venv .venv
```

**Windows (PowerShell):**

```bash
.\.venv\Scripts\Activate.ps1
```

**macOS / Linux:**

```bash
source .venv/bin/activate
```

3. **Install required packages**

```bash
pip install -r requirements.txt
```

<a id="usage"></a>
## 🚀 Usage

1. **Open the Jupyter Notebook**

```bash
jupyter notebook notebook.ipynb
```

2. **Run all cells** to execute the complete pipeline:
   - Data loading and exploration
   - Cleaning checks (missing values / duplicates) + drop `Unnamed: 0`
   - Feature engineering (`TV_Radio`)
   - Model training and evaluation
   - Visualization generation

<a id="model-performance"></a>
## 📈 Model Performance

The project compares three regression models on a held-out test set (`test_size=0.2`, `random_state=42`):

| Model | MAE | RMSE | R² Score |
|------|----:|-----:|---------:|
| **Linear Regression** | 0.67 | 0.90 | 0.97 |
| **Decision Tree** | 0.96 | 1.21 | 0.95 |
| **SVM (SVR)** | 0.96 | 1.44 | 0.93 |

**Best Model**: **Linear Regression** achieved the highest R² score (~0.97) and the lowest errors in this notebook.

<a id="dashboard"></a>
## 📊 Dashboard

To explore the Power BI dashboard:

- Open `Dashboard/Advertising.pbix` using **Power BI Desktop**
- Preview image is available at `Dashboard/image.png`

<a id="results"></a>
## 📝 Results

- Built a complete ML workflow for sales prediction
- Achieved strong predictive performance (**R² ≈ 0.97**) using Linear Regression
- Identified relationships between advertising channels and sales
- Included a Power BI dashboard for presentation and insights

<a id="contributing"></a>
## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

<a id="license"></a>
## 📄 License

This project is open source and available under the [MIT License](LICENSE).

<a id="author"></a>
## 👤 Author

**Mohamed Younis**

<a id="acknowledgments"></a>
## 🙏 Acknowledgments

- CodeAlpha for the project opportunity
- Open source community for the amazing Python ecosystem

