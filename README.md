# 🚔 ST-Hotspot Analyzer

## 📍 Spatio-Temporal Crime Hotspot Detection and Evolution Analysis Using Unsupervised Learning

ST-Hotspot Analyzer is a data science project that analyzes urban crime patterns using spatial clustering and temporal hotspot evolution techniques. The project uses the Chicago Crime Dataset to identify crime hotspots and examine how these hotspots persist, emerge, or disappear over time.

The system combines DBSCAN clustering with quarterly temporal segmentation and centroid-based hotspot matching to uncover meaningful spatio-temporal crime patterns.

---

# 🎯 Project Objectives

- Detect spatial crime hotspots using unsupervised learning
- Analyze how hotspots evolve across time
- Measure hotspot persistence and spatial volatility
- Visualize hotspot evolution through interactive dashboards
- Support data-driven insights for urban safety and planning

---

# 📊 Dataset

**Source:** Chicago Crime Dataset  
**Time Range:** 2001 – 2026  
**Dataset Size:** ~8.3 million cleaned records  

## 📌 Features Used
- Latitude
- Longitude
- Date
- Year
- Quarter
- Primary Type (optional)

🔗 Dataset Source:  
https://data.cityofchicago.org

---

# ⚙️ Methodology

## 1️⃣ Data Preprocessing
- Removed records with missing geographic or temporal values
- Converted date fields into datetime format
- Extracted Year and Quarter features
- Filtered data for multi-year analysis (2018–2025)

---

## 2️⃣ Spatial Hotspot Detection

DBSCAN clustering was applied independently for each quarter.

### 📌 Parameters
- `eps = 300 meters`
- `min_samples = 50`
- Distance Metric: Haversine Distance

---

## 3️⃣ Temporal Segmentation

Crime data was divided into:
- Q1
- Q2
- Q3
- Q4

for each year.

---

## 4️⃣ Hotspot Evolution Analysis

Cluster centroids from consecutive quarters were compared.

### 🔁 Evolution Rules
- Distance ≤ 1.5 km → Persisted
- No Match → Disappeared
- New Cluster → Emerged

---

# 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Jupyter Notebook
- Power BI

---

# 📈 Dashboard Visualization

An interactive Power BI dashboard was developed to visualize:
- Hotspot trends
- Persistence rates
- Noise percentage
- Quarterly hotspot analysis
- Spatial hotspot evolution maps

---

# 📌 Results

## 📍 2023 Clustering Results
- ~72–85 hotspots detected per quarter
- ~20–26% spatial noise
- Significant hotspot stability across quarters

---

## 📊 Multi-Year Analysis (2018–2025)
- Average hotspots: ~78
- Average persistence rate: ~56%
- Crime hotspots showed both stable and dynamic behavior over time

---

# 📂 Repository Structure

```text
ST-Hotspot-Analyzer/
│
├── data/
├── notebooks/
├── outputs/
├── dashboard/
├── report/
├── images/
├── requirements.txt
└── README.md
```

---

# 🚀 How to Run

## 1️⃣ Clone Repository

```bash
git clone https://github.com/your-username/ST-Hotspot-Analyzer.git
```

---

## 2️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

---

## 3️⃣ Open Jupyter Notebook

```bash
jupyter notebook
```

---

# 🔮 Future Work

- Advanced hotspot tracking using cluster overlap methods
- Crime-type-specific hotspot analysis
- Predictive hotspot forecasting
- Real-time crime stream analysis
- Scalable distributed processing for larger datasets

---

# 💻 Hardware Used

- Alienware 16X Aurora
- NVIDIA® GeForce RTX™ 5060
- 32 GB DDR5 RAM
- Intel Core Ultra 7 Processor

---

# 👨‍💻 Author

**Hemin Shah**  
Master of Science in Computer Science (Data Science)  
University of Regina

---

# 📜 License

This project is licensed under the MIT License.