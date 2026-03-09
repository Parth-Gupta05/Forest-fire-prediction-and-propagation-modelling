# 🔥 Forest Fire Prediction and Spread Simulation

A Machine Learning and Geospatial Analysis project that predicts forest fire probability and simulates fire spread over time using environmental features derived from satellite imagery.

The project leverages **Google Earth Engine**, **NDVI vegetation index**, and **machine learning classification** to identify potential fire-prone areas and visualize how fires can spread over time.

---

## 📍 Study Area
The analysis focuses on **Uttarakhand, India**, a region highly prone to forest fires due to:
*   Dry climate conditions
*   Dense vegetation
*   Seasonal temperature variations

---

## 🛰️ Fire Probability Mapping
The model generates a fire probability map based on environmental indicators.

### Layers Used
*   OpenStreetMap base map
*   Uttarakhand boundary
*   NDVI (Normalized Difference Vegetation Index)
*   Historical fire labels
*   Fire probability prediction

> **Note:** Red regions represent high fire probability areas predicted by the model.

---

## 📊 Dataset
The dataset was balanced to avoid bias in the classification model, ensuring high reliability.

| Fire Label | Count |
| :--- | :--- |
| No Fire (0) | 1500 |
| Fire (1) | 1500 |
| **Total Samples** | **3000** |

---

## 🤖 Machine Learning Model
A supervised machine learning classifier was trained to predict whether a location is likely to experience a forest fire.

### Evaluation Results
| Class | Precision | Recall | F1-Score | Support |
| :--- | :--- | :--- | :--- | :--- |
| **0 (No Fire)** | 0.92 | 0.83 | 0.87 | 310 |
| **1 (Fire)** | 0.83 | 0.92 | 0.88 | 290 |
| **Accuracy** | | | **0.88** | **600** |
| **Macro Avg** | 0.88 | 0.88 | 0.87 | 600 |
| **Weighted Avg** | 0.88 | 0.88 | 0.87 | 600 |

### Key Metrics
| Metric | Value |
| :--- | :--- |
| **Accuracy** | 88% |
| **Precision (No Fire)** | 0.92 |
| **Recall (Fire)** | 0.92 |
| **F1 Score** | 0.88 |

---

## 🔥 Fire Spread Simulation
After predicting fire-prone areas, a **cellular automata-based simulation** models how fires spread over time.

### Fire Spread Progression
| Time | Simulation Phase |
| :--- | :--- |
| **1 hour** | Initial ignition |
| **2 hours** | Fire starts spreading |
| **3 hours** | Expansion increases |
| **6 hours** | Fire cluster grows |
| **12 hours** | Large burn area |

### 🎞️ Fire Spread Animation
The fire spread is visualized as a time-based simulation, demonstrating how fires expand spatially over time.

---

## 🛠️ Technologies Used
| Technology | Purpose |
| :--- | :--- |
| **Python** | Core programming |
| **Google Earth Engine** | Satellite data processing |
| **Geemap** | Interactive geospatial visualization |
| **NumPy** | Numerical computation |
| **Matplotlib** | Visualization |
| **Scikit-learn** | Machine learning model |
| **Rasterio** | Raster data processing |

---

## ⚙️ Installation

### 1. Clone the repository:
```bash
git clone https://github.com/yourusername/forest-fire-prediction.git
cd forest-fire-prediction
```

### 2. Install dependencies:
```bash
pip install earthengine-api geemap rasterio xarray scikit-learn numpy matplotlib
```

### 3. Authenticate Earth Engine:
```python
import ee
ee.Authenticate()
ee.Initialize()
```

---

## 🚀 How to Run
Open the notebook `forest_fire_prediction.ipynb` and follow these steps:
1.  Install dependencies.
2.  Load satellite data using Google Earth Engine.
3.  Generate NDVI vegetation index.
4.  Train the machine learning fire prediction model.
5.  Evaluate model performance.
6.  Generate fire probability map.
7.  Run the fire spread simulation.

---

## 📈 Project Workflow
1.  **Satellite Data**
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;          ↓
2.  **NDVI Feature Extraction**
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  ↓
3.  **Dataset Creation**
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  ↓
4.  **Machine Learning Model Training**
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  ↓
5.  **Fire Probability Mapping**
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ↓
6. **Fire Spread Simulation**
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ↓
7. **Visualization**

---

## 🌍 Applications
This system serves as a valuable tool for:
*   **Forest Departments:** Monitoring fire risk.
*   **Disaster Management:** Strategic planning.
*   **Early Warning Systems:** Providing wildfire alerts.
*   **Environmental Monitoring:** Tracking ecological changes.
*   **Climate Research:** Studying the impact of climate on fire frequency.

---

## 🔮 Future Improvements
*   Incorporate weather data (temperature, wind speed, humidity).
*   Implement deep learning models (CNN / LSTM).
*   Enable real-time satellite monitoring.
*   Develop more advanced fire spread physics models.
*   Create an interactive web dashboard for public use.