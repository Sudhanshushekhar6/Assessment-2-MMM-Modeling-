# 📊 Marketing Mix Modeling with Mediation Analysis

A Marketing Mix Model (MMM) that treats Google Ads spend as a mediator between social media channels (Facebook, TikTok, Snapchat, Instagram) and revenue.

## 🚀 Quick Start

### Prerequisites
```bash
pip install pandas numpy scikit-learn matplotlib seaborn joblib jupyter
```

### Installation & Setup
1. Clone this repository
2. Install dependencies: `pip install -r requirements.txt` (or use the command above)
3. Place your dataset as `data/dataset.csv`

### Running the Notebooks

**Option 1: Jupyter Notebook (Browser)**
```bash
jupyter notebook
```
Navigate to `notebooks/` folder and open the files.

**Option 2: VS Code (Recommended)**
1. Install VS Code with Python + Jupyter extensions
2. Open project folder in VS Code
3. Select Python kernel and run cells with Shift+Enter

### Workflow
1. **Data Preparation**: Run `1_data_preparation.ipynb`
   - Data preprocessing & transformations
   - Feature engineering (lag features, scaling)
   - Seasonality adjustments

2. **Modeling**: Run `2_modeling.ipynb`
   - Train mediator model (Google Spend prediction)
   - Train revenue model (with Google as mediator)
   - Model evaluation and performance metrics

## 📂 Project Structure
```
├── data/
│   └── dataset.csv           # Your marketing dataset
├── notebooks/
│   ├── 1_data_preparation.ipynb
│   └── 2_modeling.ipynb
├── models/                   # Saved trained models
├── README.md
└── requirements.txt
```

## 📈 Key Outputs
- **Performance Metrics**: RMSE, R², residual analysis
- **Model Coefficients**: Feature importance and elasticity
- **Visualizations**: Predicted vs actual revenue plots
- **Business Insights**: Price sensitivity, promotion lift, media channel effectiveness

## 📋 Requirements
- Python 3.8+
- Key libraries: pandas, numpy, scikit-learn, matplotlib, seaborn, joblib

## 🎯 Model Overview
This MMM uses a **causal mediation framework** where:
- **Mediator**: Google Ads spend
- **Treatment**: Social media channels (Facebook, TikTok, Snapchat, Instagram)
- **Outcome**: Revenue
- **Controls**: Price, promotions, seasonality
