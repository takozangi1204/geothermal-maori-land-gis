# Taupō–Reporoa Geothermal & Māori Land Interactive GIS Explorer
### 地熱発電所・マオリ土地・ロヘ GISマップ

An interactive, browser-based GIS map application for exploring geothermal resources, Māori land ownership blocks, and Iwi Areas of Interest (Rohe) across the Taupō–Reporoa geothermal zone in the Central North Island, New Zealand.

---

## 🌐 Live Web Application (GitHub Pages)

Once deployed to GitHub Pages, the application is accessible instantly in any browser:
- **Māori Land & Rohe Map (EN)**: `https://takozangi1204.github.io/geothermal-maori-land-gis/`
- **Māori Land & Rohe Map (JA)**: `https://takozangi1204.github.io/geothermal-maori-land-gis/index_ja.html`
- **2023 Census Regional Report App (EN)**: `https://takozangi1204.github.io/geothermal-maori-land-gis/census.html`
- **2023 Census Regional Report App (JA)**: `https://takozangi1204.github.io/geothermal-maori-land-gis/census_ja.html`

Use the top navigation bar to toggle between the **Land Map** and the **2023 Census Report**, and use the **`[ EN | JA ]`** switch in the top-right header to switch languages seamlessly.

---

## 🌟 Key Features

1. **6 Geothermal Power Stations & Case-Study Popups**:
   - Ohaaki, Ngatamariki, Tauhara, Nga Awa Purua, Wairakei, and Mokai.
   - Click any station marker on the map to open a detailed **Plant Description Screen (Modal)** featuring ownership specs, historical/Māori relationship summaries, current status, key takeaways, confidence tags (`[Fact]`, `[Inference]`), and hyperlinked primary sources.

2. **2023 Census Regional Socioeconomic & Industry Analysis App**:
   - Dedicated split-view dashboard (Report Sheet + Map) covering 19 SA2 areas across the Central North Island geothermal belt and commuter catchment zones.
   - 5-line demographic summary (population, age structure, Māori ethnicity/descent %, commuter base & inflow rate).
   - Side-by-side residence and workplace industry structure pie charts (single-stage rounded percentages with muted colors) and breakdown tables.
   - Inflow commuter origin pills and map visualization.

3. **4,757 Matched Māori Land Parcels**:
   - Combined LINZ Property Titles with Māori Land Court (2025) ownership data.
   - Distinct visualization for **Standard Māori Land** vs. **Aggregated Ownership Blocks** (shared owner registry).
   - Dynamic owner count filter spanning **0 to 17,737 owners**.
   - Prominent **Owner Numbers on Map Toggle** (switches `is_rep = 1` owner count badges).

4. **Iwi Areas of Interest (TPK Rohe)**:
   - Ngāti Tahu / Ngāti Whaoa (default ON)
   - Ngāti Tūwharetoa (default ON)
   - Overlapping Area highlighting shared cultural interests.

5. **Curated Base Maps**:
   - **Esri World Topo Map** (Default high-resolution topographic map)
   - **Google Maps Roadmap**
   - **Google Maps Hybrid** (Satellite + road labels)
   - **Google Maps Terrain**

---

## 📁 Repository Structure

```
├── docs/                               # GitHub Pages deployment source
│   ├── index.html                      # Māori Land Map (English)
│   ├── index_ja.html                   # Māori Land Map (Japanese)
│   ├── census.html                     # 2023 Census Report Map (English)
│   └── census_ja.html                  # 2023 Census Report Map (Japanese)
├── map_app/                            # Application source and data processing
│   ├── data_processing_and_map.ipynb   # Māori land & plant processing notebook
│   ├── census_processing_and_map.ipynb # 2023 Census data processing notebook
│   ├── index.html                      # Standalone English land app
│   ├── index_ja.html                   # Standalone Japanese land app
│   ├── census.html                     # Standalone English census app
│   ├── census_ja.html                  # Standalone Japanese census app
│   └── processed_data/                 # GeoJSON, GeoPackage, and JSON data
├── plants_data/                        # Geothermal power stations GIS layer
├── property_data/                      # LINZ titles & Māori Land Court CSVs
└── rohe_data/                          # Te Puni Kōkiri Iwi Areas of Interest shapefiles
```

---

## 🚀 How to Run Locally

### Option 1: Direct Browser Open (No installation needed)
Simply double-click `docs/index.html` or `docs/index_ja.html` in your file explorer. It opens directly in your web browser.

### Option 2: Run / Modify Data Pipeline
If you wish to re-process data or add new layers, run the Jupyter Notebook:
```bash
pip install geopandas pandas shapely pyproj folium
jupyter notebook map_app/data_processing_and_map.ipynb
```

