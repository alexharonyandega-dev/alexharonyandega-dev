# Hi, I'm Alex 👋

**16-year-old Kenyan student building enterprise-grade climate software.**

I am the founder of **Kenya Climate Data Lab** — an open-source, county-level drought and vegetation stress monitor for all 47 Kenyan counties. 

Instead of building a static dashboard, I built a full-stack intelligence service that uses satellite data, machine learning, and automated CI/CD pipelines to predict agricultural risk.

### 🚀 Live Services
*   **[Interactive Dashboard (Streamlit)](https://kenya-climate-data-lab.streamlit.app)** — User-friendly interface with ML-powered next-month drought predictions.
*   **[Developer API (FastAPI)](https://kenya-climate-api.onrender.com/docs)** — REST API for programmatic access to the dataset.

### 🛠️ Tech Stack & Architecture
I designed and deployed the entire stack from scratch:
*   **Data Engineering:** Python, Pandas, CHIRPS (rainfall), Sentinel-2 (NDVI), ERA5-Land (soil moisture). Automated data ingestion pipelines using GitHub Actions.
*   **Machine Learning:** XGBoost classifier trained on lagged soil moisture and rainfall anomalies to predict severe drought probability (ROC-AUC: 0.82).
*   **Backend:** FastAPI, Uvicorn, Pytest. Deployed on Render.
*   **Frontend:** Streamlit, Plotly. Deployed on Streamlit Community Cloud.
*   **Infrastructure:** Docker, Docker Compose, GitHub Actions (CI/CD), Run Manifests.

### 📊 Key Findings
My research (currently being prepared for preprint) uncovered three critical insights:
1.  **Drought ≠ Crop Damage:** In 2022, 31 counties experienced severe drought, but only **8** experienced it *while maize was actively growing*.
2.  **Soil Moisture Leads Vegetation:** Topsoil moisture anomalies predict vegetation collapse by 1 month (r = 0.461).
3.  **Complementary to NDMA:** The monitor tracks crop-region vegetation stress in all 47 counties, complementing NDMA's pastoral drought tracking.

### 📫 Connect with me
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Alex%20Haro%20Nyandega-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/alexharonyandega)
[![Email](https://img.shields.io/badge/Email-alex@kenyaclimatelab.me-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:alex@kenyaclimatelab.me)
