# 🌍 Urban Environmental Correlation Engine

A comprehensive Streamlit-based application for analyzing relationships between environmental variables including wind speed, land surface temperature (LST), and NO₂ pollution levels.

## 📋 Table of Contents

- [Features](#features)
- [Quick Start](#quick-start)
- [Installation](#installation)
- [Running on Streamlit](#running-on-streamlit)
- [Usage Guide](#usage-guide)
- [Datasets](#datasets)
- [Technical Stack](#technical-stack)
- [Troubleshooting](#troubleshooting)

## ✨ Features

### 📊 Data Fusion & KPIs
- Merge multiple environmental datasets
- Generate key performance indicators
- Missing value audit and analysis
- Temporal coverage analysis
- Descriptive statistics
- Feature distribution exploration
- Time series visualization

### 📈 Correlation Analytics
- Correlation heatmaps
- Pearson correlation analysis
- Spearman correlation analysis
- Scatter plots with trend lines
- Automated relationship interpretation
- Pollution relationship analysis

### 📉 Lag Analysis & Significance Testing
- Weather impact significance tests
- Lag correlation analysis (1 & 2 period lags)
- Environmental impact matrices
- Statistical interpretation

### 🤖 Pattern Recognition & Prediction
- KMeans clustering for pattern detection
- Cluster visualization and profiling
- Anomaly detection using Isolation Forest
- Environmental event detection
- Random Forest forecasting
- Feature importance analysis
- 30-day future predictions

---

## 🚀 Quick Start (Copy & Paste)

### Step 1: Clone Repository
```bash
git clone https://github.com/Aishwarya2006-bot/air-quality-.git
cd air-quality-
```

### Step 2: Create Virtual Environment

**On Windows:**
```bash
python -m venv venv
venv\Scripts\activate
```

**On macOS/Linux:**
```bash
python -m venv venv
source venv/bin/activate
```

### Step 3: Install Dependencies
```bash
pip install streamlit pandas numpy matplotlib seaborn scikit-learn scipy
```

### Step 4: Run on Streamlit
```bash
streamlit run utils/utils/utils/app.py
```

The application will automatically open in your browser at `http://localhost:8501`

---

## 🛠 Installation

### Prerequisites
- Python 3.8 or higher
- pip package manager
- Git (for cloning)

### Full Installation Steps

```bash
# 1. Clone the repository
git clone https://github.com/Aishwarya2006-bot/air-quality-.git
cd air-quality-

# 2. Create virtual environment
python -m venv venv

# 3. Activate virtual environment
# Windows:
venv\Scripts\activate
# macOS/Linux:
source venv/bin/activate

# 4. Upgrade pip (optional but recommended)
pip install --upgrade pip

# 5. Install all required packages
pip install streamlit pandas numpy matplotlib seaborn scikit-learn scipy

# 6. Verify installation
streamlit --version
```

---

## 📱 Running on Streamlit

### Basic Command
```bash
streamlit run utils/utils/utils/app.py
```

### With Custom Settings
```bash
streamlit run utils/utils/utils/app.py --logger.level=debug
```

### Streamlit Configuration Options

Create a `~/.streamlit/config.toml` file for custom settings:

```toml
[theme]
primaryColor = "#1f77b4"
backgroundColor = "#FFFFFF"
secondaryBackgroundColor = "#F0F2F6"
textColor = "#262730"
font = "sans serif"

[client]
showErrorDetails = true

[server]
maxUploadSize = 200
```

### Stopping the Application
Press `Ctrl+C` in the terminal where Streamlit is running.

### Accessing the App
- Local: `http://localhost:8501`
- Remote: `http://<your-ip>:8501` (if running on remote server)

---

## 📖 Usage Guide

### 1️⃣ Upload or Generate Data

**Option A: Upload Your Datasets**
- Click **📂 Upload Datasets** in the left sidebar
- Upload three CSV files in order:
  1. Wind Dataset
  2. NO₂ Dataset
  3. LST Dataset

**Option B: Generate Sample Data**
- If files are missing, you'll see a warning
- Click **"Generate & Load 3 Sample Interrelated Datasets"**
- Perfect for testing and learning!

---

### 2️⃣ Tab 1: 📊 Data Fusion & KPIs

**What You'll See:**
```
✓ Merged dataset preview (first 20 rows)
✓ Key metrics (mean values for numeric columns)
✓ Dataset dimensions (rows × columns)
✓ Numeric features count
✓ Missing values analysis with percentages
✓ Temporal coverage (start and end dates)
✓ Descriptive statistics table
✓ Feature distribution histograms
✓ Time series plots
✓ Strongest relationships ranking
```

**How to Use:**
1. Review the merged data preview at the top
2. Check the KPI metrics cards
3. Scroll down to see missing values audit
4. Select variables from dropdowns to explore:
   - Feature distributions
   - Time series trends

---

### 3️⃣ Tab 2: 📈 Correlation Analytics

**What You'll See:**
```
✓ Correlation heatmap of all variables
✓ Pearson correlation coefficient & p-value
✓ Spearman correlation coefficient & p-value
✓ Scatter plot with trend line
✓ Automated interpretation of relationships
✓ Strongest correlations ranking
✓ Pollution variable relationships
```

**How to Use:**
1. View the correlation heatmap (red = positive, blue = negative)
2. Select X and Y variables from dropdowns
3. Compare Pearson vs Spearman results
4. Review the scatter plot for visual relationship
5. Read the automated interpretation
6. Scroll to see top correlations table

---

### 4️⃣ Tab 3: 📉 Lag Analysis & Significance Testing

**What You'll See:**
```
✓ Weather impact significance test results
✓ Significance summary (Total, Significant, Not Significant)
✓ Lag correlation analysis (1 & 2 period delays)
✓ Lag correlation visualization
✓ Strongest lag relationships ranking
✓ Environmental impact matrix heatmap
✓ Statistical interpretation
```

**How to Use:**
1. Review significance test results table
2. Check significance summary cards
3. Look at lag correlations
4. View the impact matrix heatmap
5. Read the interpretation at the bottom

---

### 5️⃣ Tab 4: 🤖 Pattern & Prediction

**What You'll See:**
```
✓ KMeans cluster profiles
✓ Cluster visualization (2D scatter plot)
✓ Cluster distribution (pie chart)
✓ Top 15 anomalies detected
✓ Environmental events detected
✓ Model metrics (R², MAE, RMSE)
✓ Actual vs Predicted plot
✓ Feature importance ranking
✓ 30-day forecast with dates
✓ Download button for merged dataset
```

**How to Use:**
1. Review cluster profiles
2. Select X and Y axes for cluster visualization
3. Check cluster distribution pie chart
4. Review top anomalies
5. Check environmental events
6. Select the NO₂ variable to forecast
7. Review model metrics
8. View actual vs predicted plot
9. Check feature importance
10. See 30-day forecast
11. Download merged CSV file

---

## 📊 Datasets

### CSV Format Requirements

Each CSV file must have:
- A `date` column (YYYY-MM-DD format recommended)
- One or more numeric measurement columns
- Optional: location, station_id, or metadata

### Example CSV Files

**wind_data.csv**
```
date,wind_speed,wind_direction
2024-01-01,12.5,45
2024-01-02,14.3,50
2024-01-03,11.8,42
2024-01-04,15.2,55
2024-01-05,13.1,48
```

**no2_data.csv**
```
date,no2_concentration,no2_level
2024-01-01,45.2,moderate
2024-01-02,52.1,high
2024-01-03,38.9,moderate
2024-01-04,61.5,high
2024-01-05,42.3,moderate
```

**lst_data.csv**
```
date,land_surface_temperature
2024-01-01,15.5
2024-01-02,16.1
2024-01-03,14.9
2024-01-04,17.2
2024-01-05,15.8
```

### Tips for Dataset Preparation

```
✓ Keep date format consistent (YYYY-MM-DD)
✓ Use numeric values only in measurement columns
✓ Remove extra spaces and special characters
✓ Ensure all three CSVs have overlapping dates
✓ Minimum 10 rows recommended
✓ Maximum 10,000 rows for optimal performance
✓ No empty rows between data
```

---

## 🏗 Technical Stack

| Technology | Version | Purpose |
|-----------|---------|---------|
| **Streamlit** | 1.28+ | Web interface |
| **Pandas** | 2.0+ | Data manipulation |
| **NumPy** | 1.24+ | Numerical computing |
| **Matplotlib** | 3.7+ | Visualizations |
| **Seaborn** | 0.12+ | Statistical graphics |
| **Scikit-learn** | 1.3+ | Machine learning |
| **SciPy** | 1.11+ | Statistical functions |

---

## 📁 Project Structure

```
air-quality-/
├── utils/
│   ├── utils/
│   ├── utils/
│   └── utils/
│       ├── app.py                 ← Run this file!
│       ├── data_loader.py
│       ├── statistics.py
│       ├── clustering.py
│       └── forecasting.py
└── README.md
```

---

## 🔧 Common Tasks

### Task: Change Number of Clusters
Edit in Tab 4 code:
```python
build_pattern_recognition_pipeline(merged_df, n_clusters=5)  # Change 4 to 5
```

### Task: Change Forecast Days
Edit in Tab 4 code:
```python
forecast_future_values(merged_df, forecast_target, periods=60)  # Change 30 to 60
```

### Task: Test Different Lag Periods
Edit in Tab 3 code:
```python
lag_correlation_analysis(merged_df, ..., lags=[1, 2, 3])  # Add lag 3
```

---

## ⚠️ Troubleshooting

### ❌ Error: "ModuleNotFoundError: No module named 'streamlit'"
**Solution:**
```bash
pip install streamlit
```

### ❌ Error: "Missing required column"
**Solution:**
- Check your CSV has a `date` column
- Ensure numeric measurement columns exist
- No special characters in column names

### ❌ Error: "Port 8501 already in use"
**Solution:**
```bash
streamlit run utils/utils/utils/app.py --server.port 8502
```

### ❌ Application crashes when uploading
**Solution:**
- Check CSV file is not corrupted
- Verify date format is consistent
- Try with sample data first

### ❌ "No data displayed" after upload
**Solution:**
- All three files must be uploaded
- Check file sizes are reasonable
- Verify date columns overlap

### ❌ Forecasting model fails
**Solution:**
- Ensure at least 50 rows of data
- Check for missing values
- Verify numeric columns are all numbers

### ❌ Streamlit not opening browser
**Manual fix:**
```
Open http://localhost:8501 in your browser
```

---

## 📊 Understanding the Analysis Results

### Correlation Values
- **±1.0** = Perfect correlation
- **±0.8-0.99** = Very Strong
- **±0.6-0.79** = Strong
- **±0.4-0.59** = Moderate
- **±0.2-0.39** = Weak
- **±0.0-0.19** = Very Weak
- **0.0** = No correlation

### P-Values (Significance)
- **< 0.05** = Statistically Significant ✓
- **> 0.05** = Not Statistically Significant ✗

### Model Performance Metrics
- **R² (0-1)** = Higher is better (explains variance)
- **MAE** = Mean Absolute Error (lower is better)
- **RMSE** = Root Mean Square Error (lower is better)

---

## 💾 Exporting Results

### Download Merged Dataset
- Go to Tab 4 (Pattern & Prediction)
- Scroll to **⬇ Download Results**
- Click **"Download Merged Dataset"**
- File saved as `merged_environmental_data.csv`

### Save Analysis Results
- Screenshots: Use Streamlit's camera icon
- Charts: Right-click → Save image
- Data: Use download buttons in each tab

---

## 🎯 Example Workflows

### Workflow 1: First-Time Users
```
1. Open app with sample data
2. Explore Tab 1 (Data overview)
3. Browse Tab 2 (Correlation heatmap)
4. Check Tab 4 (Forecast example)
5. Download sample results
```

### Workflow 2: Data Analysis
```
1. Upload your three CSV files
2. Tab 1: Verify data quality
3. Tab 2: Explore relationships
4. Tab 3: Test significance
5. Tab 4: Train forecast model
```

### Workflow 3: Research Presentation
```
1. Upload research datasets
2. Generate all analyses
3. Take screenshots of each tab
4. Download merged data CSV
5. Use results in reports/presentations
```

---

## 📞 Getting Help

### If Something Doesn't Work:
1. **Check Streamlit is running**: Look at terminal for errors
2. **Try sample data**: Generate & load sample datasets
3. **Check dataset format**: Use example CSVs provided
4. **Restart app**: Ctrl+C and run again
5. **Clear cache**: Delete `.streamlit` folder in home directory

### Common Issues Checklist:
- [ ] Python 3.8+ installed?
- [ ] Virtual environment activated?
- [ ] All packages installed (`pip list`)?
- [ ] CSV files have `date` column?
- [ ] Date format is consistent?
- [ ] Numeric columns have only numbers?

---

## 📝 Requirements Summary

### Minimum System Requirements
- **RAM**: 2GB minimum, 4GB recommended
- **Storage**: 500MB free space
- **Python**: 3.8 or higher
- **Internet**: For initial setup only

### Dependencies Installation
```bash
pip install streamlit pandas numpy matplotlib seaborn scikit-learn scipy
```

### Verify Installation
```bash
streamlit --version
python -c "import pandas, numpy, sklearn, scipy; print('All packages installed!')"
```

---

## 🚀 Next Steps

1. **Install and run the app** using Quick Start above
2. **Generate sample data** to explore features
3. **Prepare your own CSV files** following the format
4. **Upload and analyze** your environmental data
5. **Share results** and findings

---

## 📜 Version Info

- **Version**: 1.0.0
- **Python**: 3.8+
- **Last Updated**: June 2026
- **Status**: Active & Maintained

---

## 📄 License

This project is open source and available for educational and research purposes.

---

## 🤝 Support

Found a bug or have a feature request? Open an issue on GitHub!

For questions, please refer to the [Troubleshooting](#troubleshooting) section above.

---

**Happy Analyzing! 🌍📊📈**
