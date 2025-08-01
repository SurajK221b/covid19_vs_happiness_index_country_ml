# COVID-19 vs Happiness Index Country Analysis

![Python](https://img.shields.io/badge/python-v3.8+-blue.svg)
![Jupyter Notebook](https://img.shields.io/badge/jupyter-%23FA0F00.svg?style=flat&logo=jupyter&logoColor=white)
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=flat&logo=pandas&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-%23ffffff.svg?style=flat&logo=Matplotlib&logoColor=black)
![Seaborn](https://img.shields.io/badge/seaborn-%2301577B.svg?style=flat&logo=python&logoColor=white)

## 📊 Project Overview

This comprehensive data analysis project explores the relationship between COVID-19 confirmed cases and happiness indices across countries worldwide. The analysis transforms daily COVID-19 data into monthly aggregations and investigates potential correlations with national happiness scores through advanced statistical methods and data visualization techniques.

## 🎯 Key Objectives

- **Data Transformation**: Convert daily COVID-19 data to monthly aggregated format
- **Statistical Analysis**: Perform correlation analysis between COVID-19 impact and happiness indices
- **Visualization**: Create comprehensive charts and plots for data insights
- **Regional Analysis**: Examine continental patterns and distributions
- **Growth Analysis**: Calculate month-over-month growth rates and trends

## 📁 Project Structure

```
covid19_vs_happiness_index_country_ml/
│
├── Data/
│   ├── RAW_global_confirmed_cases.csv     # Daily COVID-19 confirmed cases data
│   └── worldwide_happiness_report.csv     # World Happiness Report data
│
├── experiment.ipynb                       # Main analysis notebook
└── README.md                             # Project documentation
```

## 📈 Dataset Information

### COVID-19 Dataset
- **Source**: Global confirmed cases data
- **Time Period**: January 2020 - December 2020
- **Coverage**: 191+ countries/regions
- **Format**: Daily cumulative confirmed cases
- **Features**: Country/Region, Province/State, Latitude, Longitude, Daily case counts

### Happiness Dataset
- **Source**: World Happiness Report
- **Coverage**: Global happiness indices by country
- **Features**: Country name, Happiness score, Various happiness factors

## 🛠️ Technologies & Libraries

### Core Libraries
- **Pandas**: Data manipulation and analysis
- **NumPy**: Numerical computing
- **Matplotlib**: Static data visualization
- **Seaborn**: Statistical data visualization
- **SciPy**: Scientific computing for statistical analysis

### Analysis Techniques
- Data cleaning and preprocessing
- Time series analysis
- Statistical correlation analysis
- Pareto analysis (80/20 rule)
- Growth rate calculations
- Multi-dimensional plotting

## 🔍 Key Features & Analysis

### 1. Data Preprocessing
- ✅ Removal of unnecessary columns (Latitude, Longitude)
- ✅ Country-level data aggregation
- ✅ Monthly data transformation from daily records
- ✅ Missing value handling and data cleaning

### 2. Monthly Data Transformation
Transform daily COVID-19 data into monthly format:
```
Country/Region | Jan 2020 | Feb 2020 | Mar 2020 | ... | Dec 2020 | Total Cases
Afghanistan    | 0        | 1        | 175      | ... | 49681    | 49681
India          | 1        | 3        | 1397     | ... | 10031223 | 10031223
```

### 3. Advanced Visualizations

#### 📊 Growth Rate Heatmap
- Month-over-month percentage growth analysis
- Color-coded visualization for top 10 countries
- Identification of outbreak phases and patterns

#### 🌍 Regional Analysis Dashboard
- Continental distribution pie charts
- Average cases per country by region
- Statistical distribution box plots
- Geographic pattern identification

#### 📈 Statistical Analysis Suite
- Distribution histograms with density curves
- Log-scale transformations
- Pareto analysis validation
- Global progression trends

#### 💡 Correlation Analysis
- COVID-19 cases vs Happiness Index scatter plots
- Linear and log-scale correlation coefficients
- Categorical analysis by case severity
- Top countries comparative analysis

### 4. Key Statistical Insights

#### Global Statistics
- **Total Countries Analyzed**: 191
- **Time Period Coverage**: 12 months (2020)
- **Data Points**: 333 daily observations per country
- **Regional Coverage**: 6 continents

#### Pareto Analysis
- Validation of 80/20 rule in global case distribution
- Identification of high-impact countries
- Statistical concentration analysis

#### Growth Pattern Analysis
- Month-over-month growth rate calculations
- Peak growth period identification
- Country-specific outbreak patterns

## 📊 Sample Visualizations

### Monthly COVID-19 Cases Progression
- Line plots showing temporal trends
- Comparative analysis between countries
- Growth trajectory visualization

### Regional Distribution Analysis
- Pie charts for continental case distribution
- Bar charts for average cases per country
- Box plots for statistical distribution

### Correlation Analysis
- Scatter plots with correlation coefficients
- Category-based happiness distribution
- Dual-axis comparative charts

## 🚀 Getting Started

### Prerequisites
```bash
Python 3.8+
Jupyter Notebook
pandas
numpy
matplotlib
seaborn
scipy
```

### Installation
1. **Clone the repository**
```bash
git clone https://github.com/SurajK221b/covid19_vs_happiness_index_country_ml.git
cd covid19_vs_happiness_index_country_ml
```

2. **Install required packages**
```bash
pip install pandas numpy matplotlib seaborn scipy jupyter
```

3. **Launch Jupyter Notebook**
```bash
jupyter notebook experiment.ipynb
```

### Usage
1. Open `experiment.ipynb` in Jupyter Notebook
2. Run cells sequentially to reproduce the analysis
3. Modify parameters and countries as needed
4. Explore additional visualizations and insights

## 📋 Analysis Workflow

### Step 1: Data Loading & Exploration
```python
# Load datasets
df_covid = pd.read_csv('data/RAW_global_confirmed_cases.csv')
df_happiness = pd.read_csv('data/worldwide_happiness_report.csv')

# Explore data structure and quality
df_covid.head()
df_covid.info()
```

### Step 2: Data Preprocessing
```python
# Remove unnecessary columns
df_covid_clean = df_covid.drop(columns=['Lat', 'Long'], axis=1)

# Aggregate by country
covid_country_agg = df_covid_clean.groupby('Country/Region').sum().reset_index()
```

### Step 3: Monthly Transformation
```python
# Convert daily data to monthly aggregations
monthly_covid_data = create_monthly_dataset(covid_country_agg)
```

### Step 4: Statistical Analysis
```python
# Calculate correlations
correlation = analyze_happiness_correlation(monthly_covid_data, df_happiness)

# Growth rate analysis
growth_rates = calculate_growth_rates(monthly_covid_data)
```

### Step 5: Visualization
```python
# Create comprehensive visualizations
create_heatmap(growth_rates)
regional_analysis(monthly_covid_data)
correlation_plots(covid_happiness_merged)
```

## 📊 Key Results & Findings

### Data Processing Achievements
- ✅ Successfully processed 191 countries/regions
- ✅ Converted 333 daily columns to 12 monthly aggregations
- ✅ Handled geographic inconsistencies and missing values
- ✅ Created analysis-ready datasets

### Statistical Insights
- **Global Case Distribution**: Identified concentration patterns
- **Regional Variations**: Quantified continental differences
- **Growth Patterns**: Mapped outbreak progression phases
- **Correlation Analysis**: Explored happiness-COVID relationships

### Visualization Accomplishments
- 📊 12+ distinct visualization types
- 🎨 Professional multi-subplot layouts
- 📈 Interactive correlation analysis
- 🌍 Geographic and temporal insights

## 🔬 Technical Skills Demonstrated

### Data Science Techniques
- **Data Wrangling**: Complex pandas operations and transformations
- **Statistical Analysis**: Correlation analysis and distribution fitting
- **Time Series Processing**: Date parsing and temporal aggregation
- **Visualization**: Advanced matplotlib and seaborn customization

### Programming Best Practices
- **Clean Code**: Well-documented and modular functions
- **Error Handling**: Robust data validation and edge case management
- **Performance**: Efficient data processing and memory management
- **Documentation**: Comprehensive markdown explanations

## 📈 Future Enhancements

### Machine Learning Integration
- [ ] Predictive modeling for case forecasting
- [ ] Classification models for outbreak risk assessment
- [ ] Clustering analysis for country groupings
- [ ] Feature importance analysis

### Advanced Analytics
- [ ] Time series decomposition and seasonality analysis
- [ ] Geospatial analysis with mapping capabilities
- [ ] Economic impact correlation studies
- [ ] Policy response effectiveness analysis

### Visualization Improvements
- [ ] Interactive dashboards with Plotly
- [ ] Geographic heat maps
- [ ] Real-time data integration
- [ ] Mobile-responsive visualizations

## 👥 Contributing

Contributions are welcome! Please feel free to submit pull requests or open issues for:
- Data quality improvements
- Additional visualization techniques
- Statistical analysis enhancements
- Documentation updates

### How to Contribute
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 📞 Contact

**Suraj Kumar** - [GitHub](https://github.com/SurajK221b)

Project Link: [https://github.com/SurajK221b/covid19_vs_happiness_index_country_ml](https://github.com/SurajK221b/covid19_vs_happiness_index_country_ml)

## 🙏 Acknowledgments

- World Health Organization for COVID-19 data
- World Happiness Report for happiness index data
- Open source community for amazing data science libraries
- Jupyter Project for the notebook environment

---

⭐ **If you found this project helpful, please consider giving it a star!** ⭐

![Data Science](https://img.shields.io/badge/Data%20Science-Analysis-blue)
![COVID-19](https://img.shields.io/badge/COVID--19-Research-red)
![Happiness](https://img.shields.io/badge/Happiness-Index-yellow)
![Visualization](https://img.shields.io/badge/Data-Visualization-green)
