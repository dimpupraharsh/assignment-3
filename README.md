# Clustering and Data Fitting Analysis

![Python Version](https://img.shields.io/badge/python-3.x-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)

## 📊 Project Overview

This project implements advanced clustering algorithms and polynomial curve fitting to analyze renewable energy consumption patterns and electricity access across different countries. It combines machine learning techniques with statistical analysis to provide insights into energy consumption trends and future predictions.

## 🎯 Key Features

### Data Analysis
- K-means clustering for country grouping
- Silhouette score analysis for optimal cluster determination
- Min-Max scaling for data normalization
- Missing value imputation using mean strategy

### Visualization Capabilities
- **Cluster Analysis**: Scatter plots with cluster centers
- **Trend Analysis**: Polynomial curve fitting with confidence intervals
- **Comparative Analysis**: Multi-country energy consumption patterns
- **Interactive Plots**: Customizable visualizations with seaborn

## 🛠️ Technical Requirements

### System Requirements
- Python 3.x or higher
- 4GB RAM minimum (8GB recommended)
- 500MB free disk space

### Python Dependencies
```python
numpy>=1.20.0
pandas>=1.3.0
scikit-learn>=0.24.0
seaborn>=0.11.0
matplotlib>=3.4.0
scipy>=1.7.0
```

## 🚀 Installation Guide

1. **Clone the Repository**
   ```bash
   git clone https://github.com/dimpupraharsh/clustering-analysis.git
   cd clustering-analysis
   ```

2. **Set Up Virtual Environment** (Recommended)
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install Dependencies**
   ```bash
   pip install -r requirements.txt
   ```

## 📖 Usage Guide

### Data Processing Functions

#### 1. Data Loading and Preprocessing
```python
data = load_dataset("world_bank_data_New.xlsx")
filtered_data = filter_and_transpose_data(
    data,
    selected_indicators=['Renewable energy consumption', 'Access to electricity'],
    years_of_interest=['2010', '2015', '2020']
)
```

#### 2. Data Scaling
```python
scaled_data, scaler = min_max_scale(data, selected_indicators)
```

#### 3. Clustering Analysis
```python
kmeans_cluster_and_plot(
    data=scaled_data,
    selected_indicators=['Renewable energy consumption', 'Access to electricity'],
    years_of_interest=['2010', '2015', '2020']
)
```

### Curve Fitting Functions

#### 1. Polynomial Model Fitting
```python
param_poly, covar_poly = opt.curve_fit(
    polynomial_with_error,
    country_data.index,
    country_data.values,
    maxfev=10000
)
```

#### 2. Confidence Interval Calculation
```python
low_poly, up_poly = confidence_interval(
    year_range,
    param_poly,
    covar_poly,
    polynomial_with_error
)
```

## 📊 Data Structure

The project works with Excel data containing the following columns:
- Country Name
- Indicator Name
- Year columns (2000-2020)
- Various energy consumption metrics

## 📈 Output Examples

The script generates multiple types of visualizations:
1. **Cluster Plots**: Country groupings based on energy metrics
2. **Trend Plots**: Polynomial fits with confidence intervals
3. **Comparative Analysis**: Multi-country energy consumption patterns
4. **Silhouette Analysis**: Optimal cluster number determination

## 🤝 Contributing

We welcome contributions! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

### Contribution Guidelines
- Follow PEP 8 style guide
- Add comments for complex logic
- Update documentation for new features
- Write unit tests for new functionality

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👥 Authors

- **Praharsh Vijay Medi** - *Initial work* - [GitHub Profile](https://github.com/dimpupraharsh)

## 🙏 Acknowledgments

- World Bank for providing the energy consumption data
- Python community for the excellent data science libraries
- Contributors and maintainers of scikit-learn, pandas, and matplotlib

## 📞 Support

For support, please:
1. Check the [Issues](https://github.com/dimpupraharsh/clustering-analysis/issues) section
2. Create a new issue if your problem isn't already listed
3. Contact the maintainers at praharsh789@gmail.com

## 🔄 Future Enhancements

- [ ] Add support for more clustering algorithms
- [ ] Implement interactive visualizations
- [ ] Add machine learning capabilities for energy consumption prediction
- [ ] Create a web interface for easier data visualization
- [ ] Add support for real-time data updates

---

⭐ Star this repository if you find it useful! 
