# Event-Based Contagion Forecasting

Analysis of COVID-19 spread correlation with 2020 campaign rally locations and timing.

![Python](https://img.shields.io/badge/Python-3.x-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Plotly](https://img.shields.io/badge/Plotly-3F4F75?style=for-the-badge&logo=plotly&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)

---

## About

This project examines whether large-scale political rallies held during the COVID-19 pandemic had a measurable effect on local case counts. Specifically, it compares county-level COVID-19 case and death trajectories before and after each of the 2020 Trump campaign rallies, using publicly available data from the New York Times COVID-19 dataset and rally schedules from Ballotpedia.

The analysis addresses a gap in epidemiological modeling: few contagion forecasting models account for the social and political dimensions of disease spread, including information asymmetries, variation in risk tolerance, and the politicization of public health guidance.

## Methodology

1. **Data acquisition** -- County-level COVID-19 case and death counts sourced from the [NYT COVID-19 dataset](https://github.com/nytimes/covid-19-data). Rally dates and locations sourced from [Ballotpedia](https://ballotpedia.org/Donald_Trump_presidential_campaign,_2020).
2. **Geographic join** -- Rally cities are mapped to their respective counties using the [US Cities Database](https://github.com/kelvins/US-Cities-Database) and FIPS-coded geographic boundaries from Plotly's GeoJSON dataset.
3. **Window comparison** -- For each rally, new daily cases are compared across a symmetric 20-day window (20 days before vs. 20 days after the event). The mean percentage change in daily new cases is computed.
4. **Visualization** -- Time series plots show case and death trajectories around each rally date. Choropleth maps display the intra-state distribution of case growth by county during the rally window.

## Key Findings

- Of the rallies analyzed, the majority of rally counties showed an increase in the mean daily case rate in the 20 days following the event compared to the 20 days prior.
- Counties hosting rallies in Minnesota, Wisconsin, and Ohio exhibited some of the largest percentage increases.
- Intra-state choropleth maps show that rally counties often experienced higher relative case growth than neighboring counties in the same state during the same period.

These are observational results. The analysis does not establish causation, and confounding factors (regional trends, testing capacity changes, seasonality) are not controlled for.

## Getting Started

### Prerequisites

- Python 3.7+
- Jupyter Notebook or JupyterLab

### Installation

```bash
git clone https://github.com/sieverett/Event-Based-Contagion-Forecasting.git
cd Event-Based-Contagion-Forecasting
pip install pandas numpy matplotlib seaborn plotly requests openpyxl python-dateutil
jupyter notebook Event-Based-Contagion-Forecasting.ipynb
```

### Data Sources

| Source | Description |
|--------|-------------|
| [NYT COVID-19 Data](https://github.com/nytimes/covid-19-data) | County-level daily case and death counts |
| [Ballotpedia](https://ballotpedia.org/Donald_Trump_presidential_campaign,_2020) | 2020 campaign rally schedule |
| [US Cities Database](https://github.com/kelvins/US-Cities-Database) | City-to-county mapping |
| [Plotly GeoJSON](https://github.com/plotly/datasets) | County FIPS boundaries for choropleth maps |

## License

This project is provided for educational and research purposes.
