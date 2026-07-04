# HotSpot JH 🗺️
### Spatial Analysis of Crime Patterns in Jharkhand

A geospatial data science project that identifies crime hotspots across the districts of Jharkhand, India, using spatial statistics (Moran's I, LISA) and spatial regression models, with the goal of informing data-driven policy recommendations.

---

## 📌 Objective
To identify crime hotspots, analyze spatial patterns, and suggest policy recommendations using district-level crime data for Jharkhand.

## 🧠 Methods & Techniques
- **Data cleaning & merging** — district crime records, geographic boundaries, and population data
- **Crime rate normalization** — murders per 100,000 population
- **Choropleth mapping** — visualizing crime rate distribution across districts
- **Spatial weights matrix** — Queen contiguity to define district neighbors
- **Global Moran's I** — testing for overall spatial autocorrelation
- **Local Moran's I (LISA)** — identifying local hotspots and coldspots
- **OLS Regression** — baseline model of crime rate vs. socio-economic factors
- **Spatial Lag & Spatial Error Models** — accounting for spatial dependence in the regression
- **Residual diagnostics** — mapping and evaluating model fit

## 🔑 Key Findings
- Crime in Jharkhand is **spatially clustered, not random** (positive, significant Moran's I)
- Hotspot districts include **Gumla, Simdega, Khunti, and West Singhbhum**
- A plain OLS model explains crime rate poorly; spatial lag/error models perform meaningfully better once spatial dependence is accounted for
- Contributing factors likely include Left-Wing Extremism/insurgency presence, along with socio-economic conditions
- See the notebook's **Questions** section for the full write-up and policy recommendations

## 🛠️ Tech Stack
`Python` · `pandas` · `numpy` · `geopandas` · `matplotlib` / `seaborn` · `libpysal` · `esda` · `splot` · `spreg`

## 📂 Project Structure
```
hotspot-jh/
├── data/                 # raw input data (see data/README.md)
├── notebooks/
│   └── hotspot_jh_analysis.ipynb
├── requirements.txt
├── .gitignore
├── LICENSE
└── README.md
```

## 🚀 Getting Started

1. Clone the repo
   ```bash
   git clone https://github.com/<your-username>/hotspot-jh.git
   cd hotspot-jh
   ```
2. Install dependencies
   ```bash
   pip install -r requirements.txt
   ```
3. Add the data files listed in `data/README.md` into the `data/` folder
4. Launch Jupyter and run the notebook
   ```bash
   jupyter notebook notebooks/hotspot_jh_analysis.ipynb
   ```

## 📊 Data Sources
- District-wise IPC crime data (2014), National Crime Records Bureau (NCRB)
- Jharkhand district boundary shapefile
- District-wise population data

## 📄 License
This project is licensed under the MIT License — see [LICENSE](LICENSE) for details.
