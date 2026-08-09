# Real-Time Air Quality Index Analysis

This project analyzes real-time air quality data collected from monitoring stations across India through the Government of India's Open Government Data (OGD) Platform.

## Project Overview

The project uses Python for data collection, cleaning, exploratory data analysis, statistical analysis, and visualization. The analysis examines different pollutants and focuses particularly on PM2.5, comparing its concentrations across states, cities, and monitoring stations.

Since the source dataset is continuously updated, the results represent the data available at the time of analysis and may change when the data is retrieved again.

## Features

- Real-time data collection from the Government of India's OGD API
- Data inspection and preprocessing to prepare the dataset for analysis
- Missing-value and duplicate analysis
- Pollutant-wise analysis of air quality measurements
- PM2.5-focused analysis across states, cities, and monitoring stations
- PM2.5 categorization using CPCB reference concentration ranges
- Statistical analysis of pollutant distributions and variability
- Outlier detection to identify unusually high pollutant observations
- Correlation analysis to examine relationships between pollutants
- Data visualization using statistical charts and plots
- Geographic comparison of air quality across monitoring locations

## Getting Started

### Prerequisites

- Python 3.7+
- Jupyter Notebook or Google Colab
- API key from data.gov.in (see API Access section below)

### Installation

1. Clone the repository
2. Install required dependencies: `pip install -r requirements.txt`

## Required Libraries

| Library | Purpose |
|---------|---------|
| **pandas** | Data manipulation, cleaning, filtering, grouping, aggregation, and analysis |
| **matplotlib** | Creating charts and visualizations |
| **seaborn** | Statistical data visualization (boxplots, countplots, heatmaps) |
| **requests** | Retrieving real-time data from the Government of India API |

## How to Use

### Running in Google Colab

1. Open the notebook in Google Colab
2. Obtain an API key from data.gov.in
3. Store your API key using Google Colab Secrets
4. Run the cells sequentially

### Using Your API Key in Colab

1. Click the **Secrets** icon (🔑) in the left sidebar
2. Click **+ Add new secret**
3. Enter: Name: `AIR_QUALITY_API_KEY`, Value: Your API key
4. In your notebook, retrieve it:

```python
from google.colab import userdata
api_key = userdata.get('AIR_QUALITY_API_KEY')
```

## Data Source
**Government of India – Open Government Data (OGD) Platform**

- **Dataset:** Real-Time Air Quality Index from Various Locations
- **URL:** [https://www.data.gov.in/resource/real-time-air-quality-index-various-locations](https://www.data.gov.in/resource/real-time-air-quality-index-various-locations)
- **Measurements Include:** PM2.5, PM10, NO2, SO2, CO, OZONE, NH3

## Analysis Methodology

The analysis follows these key steps:

1. **Data Collection** – Retrieve real-time data through the government API
2. **Data Inspection** – Examine structure, data types, missing values, duplicates, and pollutant coverage
3. **Data Cleaning & Preprocessing** – Prepare the data for analysis
4. **Exploratory Data Analysis** – Examine distributions, summary statistics, and variability
5. **PM2.5 Analysis** – Analyze concentrations across states, cities, and monitoring stations
6. **Category Analysis** – Classify PM2.5 using CPCB reference ranges
7. **Outlier Analysis** – Identify unusually high or low observations
8. **Correlation Analysis** – Examine relationships between pollutants
9. **Visualization** – Present findings using statistical charts and plots
