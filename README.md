# Taupō–Reporoa Geothermal & Māori Land Interactive GIS Explorer
### 地熱発電所・マオリ土地・ロヘ GISマップ

An interactive, browser-based GIS map application for exploring geothermal resources, Māori land ownership blocks, and Iwi Areas of Interest (Rohe) across the Taupō–Reporoa geothermal zone in the Central North Island, New Zealand.

---

## 🌐 Live Web Application (GitHub Pages)

Once deployed to GitHub Pages, the application is accessible instantly in any browser:
- **English Version**: `https://<YOUR-GITHUB-USERNAME>.github.io/<REPO-NAME>/`
- **Japanese Version (日本語版)**: `https://<YOUR-GITHUB-USERNAME>.github.io/<REPO-NAME>/index_ja.html`

Use the **`[ EN | JA ]`** toggle switch in the top-right header to switch seamlessly between languages.

---

## 🌟 Key Features

1. **6 Geothermal Power Stations**:
   - Ohaaki (Contact Energy, 45 MW)
   - Ngatamariki (Mercury Energy, 82 MW)
   - Tauhara (Contact Energy, 174 MW)
   - Nga Awa Purua (Mercury Energy, 140 MW)
   - Wairakei (Contact Energy, 132 MW)
   - Mokai (Tuaropaki Power Company, 112 MW)
   - Includes custom red plant markers with pulsing ripple indicators and clickable popup inspection cards.

2. **4,757 Matched Māori Land Parcels**:
   - Combined LINZ Property Titles with Māori Land Court (2025) ownership data.
   - Distinct visualization for **Standard Māori Land** vs. **Aggregated Ownership Blocks** (shared owner registry).
   - Dynamic owner count filter spanning **0 to 17,737 owners**.
   - Prominent **Owner Numbers on Map Toggle** (switches `is_rep = 1` owner count badges).

3. **Iwi Areas of Interest (TPK Rohe)**:
   - Ngāti Tahu / Ngāti Whaoa (default ON)
   - Ngāti Tūwharetoa (default ON)
   - Overlapping Area highlighting shared cultural interests.

4. **Curated Base Maps**:
   - **Esri World Topo Map** (Default high-resolution topographic map)
   - **Google Maps Roadmap**
   - **Google Maps Hybrid** (Satellite + road labels)
   - **Google Maps Terrain**

---

## 📁 Repository Structure

```
├── docs/                             # GitHub Pages deployment source
│   ├── index.html                    # English interactive map application
│   └── index_ja.html                 # Japanese interactive map application
├── map_app/                          # Application source and data processing
│   ├── data_processing_and_map.ipynb # Reproducible data pipeline Jupyter notebook
│   ├── index.html                    # Standalone English app
│   ├── index_ja.html                 # Standalone Japanese app
│   └── processed_data/               # Exported GeoJSON & GeoPackage files
├── plants_data/                      # Geothermal power stations GIS layer
├── property_data/                    # LINZ titles & Māori Land Court CSVs
└── rohe_data/                        # Te Puni Kōkiri Iwi Areas of Interest shapefiles
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
