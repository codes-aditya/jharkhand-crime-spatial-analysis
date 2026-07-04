# Data

This folder is where the input data files should live. They are **not included in the repo** (raw data is usually excluded from GitHub, especially shapefiles which have multiple parts and can be large).

Place the following files here before running the notebook:

| File | Description |
|---|---|
| `01_District_wise_crimes_committed_IPC_2014.csv` | District-wise IPC crime data |
| `DISTRICT_BOUNDARY.shp` (+ `.shx`, `.dbf`, `.prj`) | Jharkhand district boundary shapefile |
| `pop_jh.csv` | District-wise population data |

> Note: a `.shp` file needs its companion files (`.shx`, `.dbf`, `.prj`) in the same folder to load correctly with `geopandas`.
