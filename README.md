# Malnutrition Analysis in Bogotá — 2017 vs 2021

Analysis of malnutrition rates across Bogotá's 20 localities, comparing 2017 and 2021 data through population projections, percentage breakdowns, and an interactive choropleth map.

---

## Project Structure

Alimentacion/
├── Analisis_Alime.ipynb       # Main analysis notebook
├── bogota_mapa.html           # Interactive map (open in browser)
├── Bogota (1).xls             # Population growth rate — DANE
├── indicadorloc (1).json      # Bogotá localities GeoJSON — DANE
└── osb_seguridad_alimentaria-alimentacionsaludable.csv  # Malnutrition survey — DANE

---

## Data Sources

| Dataset | Source | Format |
|---|---|---|
| Malnutrition survey by locality | DANE | CSV |
| Population growth rate | DANE | XLS |
| Bogotá localities boundaries | DANE | GeoJSON |
| 2018 Census population by locality | *Constructed manually* from "Pasado, Presente y Futuro de Bogotá" — Secretaría de Planeación, Alcaldía de Bogotá | DataFrame |

---

## Methodology

1. **Population projections** — 2018 census data projected to 2017 and 2021 using DANE's exponential growth rate
2. **Malnutrition estimates** — percentage answering "Sí" to food insecurity, applied to projected populations
3. **Geospatial visualization** — localities matched to GeoJSON and rendered as an interactive map

---

## Libraries Used

- `pandas` — data manipulation
- `numpy` — numerical calculations
- `matplotlib` — bar chart visualization
- `folium` — interactive map
- `geopandas` — geospatial data handling
- `unicodedata` — text normalization for locality name matching

---
## Results

![Comparación 2017 vs 2021](grafica_comparacion.png)

---
## Interactive Map

Open `bogota_mapa.html` directly in any browser — no server or internet connection required.
Hover over each locality to see population, malnutrition percentage, and total affected population for both years.
