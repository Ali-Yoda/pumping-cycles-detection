# Pumping Events Detection

Analysis of vacuum pump cycles from electron microscope data.

## Description

Detection of pumping cycles and evaluation of pump health based on pressure measurements. The analysis includes cycle threshold calculation, outlier detection, correlation analysis, and hypothesis testing.

## Data

- `Pressure.csv` - pressure measurements and pump states
- 19,862 observations from August-September 2017
- 153 pumping cycles identified

## Key Findings

- **Cycle thresholds**: Mean 9.06 Pa, range 7.35-10.36 Pa
- **Outliers**: No significant outliers detected (IQR method)
- **Correlation**: Negative correlation between cycle duration and threshold (r = -0.549)
- **Invariance**: Linear regression suggests a slight upward trend, but after autocorrelation correction (Mann-Kendall Hamed-Rao test), the trend is not statistically significant (p = 0.063, borderline).
- **Health hypothesis**: NOT supported - all cycles show pressure increases during pumping

## Requirements

```
pandas
numpy
seaborn
matplotlib
plotly
scipy
pymannkendall
statsmodels
ydata-profiling
```

## Usage

```bash
pip install -r requirements.txt
jupyter notebook Assignment_pump_navratilova.ipynb
```

## Author

Alice Navrátilová

