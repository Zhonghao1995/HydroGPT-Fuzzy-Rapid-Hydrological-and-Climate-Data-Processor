# Fuzzy-HydroGPT-RTC v2.0  

**Released by Zhonghao Zhang & Caterina Valeo**  
Based on the research paper:  
**“FUZZY-BASED INPUT METHOD FOR UNCERTAINTY QUANTIFICATION IN A DETERMINISTIC MODEL: COMPARISON WITH CHATGPT FOR PEAK FLOW PREDICTION.”**

---

## 📖 Overview  

**Fuzzy-HydroGPT-RTC** integrates a complete hydrological and uncertainty-quantification workflow into a single, user-friendly **PyQt6 interface**.  
Unlike earlier versions, **v2.0 introduces real-time control (RTC)**, enabling a seamless **data-to-prediction pipeline** that transforms raw inputs into GPT-based flow predictions with near-instant feedback (<10 seconds).  

The tool supports **broad generalization beyond hydrology**—any application that requires real-time data ingestion, GPT processing, and uncertainty quantification can be adapted with minimal configuration.

---

## ⚙️ Core Features  

### 🔐 Secure Card-Based Login  
<div align="center">
<img width="380" alt="image" src="https://github.com/user-attachments/assets/0077a642-5dd5-49e6-b546-e7fb5f43eb51" />
</div>

- Authentication via card number and password (`Card.txt` included for testing).  
- Prevents unauthorized use.  

---

### 🌦 Weather & Flow Data Scraping  
<div align="center">
<img width="500"  alt="image" src="https://github.com/user-attachments/assets/d969fcea-1140-4424-b897-135b5964837f" />
<img width="425"  alt="image" src="https://github.com/user-attachments/assets/bd72c5c9-a915-42ab-a740-7547c6b552bc" />
</div>

- **Weather Data Scraper:** Fetch daily/hourly climate data (rainfall, temperature, snow, etc.) from public sources.  
- **Flow Gauge Scraper:** Retrieve river discharge values directly from hydrometric networks.  
- Auto-clean and export to **CSV/Excel**.  

---

### 🧹 Data Cleaning & File Processing  
- Load CSV/Excel datasets, filter invalid entries, and save cleaned data.  
- Extract & merge multiple datasets by timestamp (pairwise or bulk).  

---

### 🤖 GPT Flow Prediction (NEW: Real-Time Control)  
<div align="center">
<img width="550" alt="image" src="https://github.com/user-attachments/assets/2a4f0562-c59b-4d94-8295-fde6d0794713" />
<img width="550" alt="image" src="https://github.com/user-attachments/assets/4df79d82-a776-4ff7-a6ae-c69f132de04e" />
<img width="550" alt="image" src="https://github.com/user-attachments/assets/a9f87a02-493e-4c29-a736-a876197f203a" />
</div>

- Configure **OpenAI API key & model** in-app.  
- Convert tabular input ➝ JSONL ➝ GPT call ➝ parsed numeric output automatically.  
- **Full real-time data loop:**  
  numeric inputs (Excel) ➝ JSONL ➝ GPT API ➝ JSONL parser ➝ numeric predictions.  
- Update predictions every ~10 seconds with minimal setup.  
- Works for hydrology and other fields requiring **real-time inference**.  

---

### 🌫 Fuzzy Uncertainty Analysis  
<div align="center">
<img width="550" alt="image" src="https://github.com/user-attachments/assets/36a44872-a3fb-44a7-b71d-a1f118da5b86" >
</div>

- Triangular and trapezoidal membership functions.  
- Compute **α-cuts**, membership values, and visualize uncertainty intervals.  
- Export fuzzy interval data to CSV/Excel.  

---

### 📊 Model Evaluation  
<div align="center">
<img width="550" alt="image" src="https://github.com/user-attachments/assets/84bbe9a5-d57d-47f0-a08f-fc4be6fc6f2f" />
</div>

- Compare **observed vs. simulated** datasets.  
- Compute performance metrics:  
  - **R²**  
  - **Nash–Sutcliffe Efficiency (NSE)**  
  - **RMSE**  
  - **MAE**  
- Plot observed–simulated comparisons for validation.  

---

## 🚀 What’s New in v2.0  

- **Real-Time Control (RTC):** Seamlessly connect data sources, GPT calls, and output parsing for predictions within 10 seconds.  
- **General Applicability:** Not restricted to hydrology—usable in any field with real-time data + GPT integration.  
- **PyQt6 Interface:** Modern, responsive UI with stability fixes and enhanced usability.  
- **Expanded Help System:** Built-in instructions on each tab.  
- **Bug Fixes:** Improved data scraping, JSONL parsing, and evaluation modules for reliability.  

---

## 🛠 Getting Started  

### 1. Download Release  
- Get the latest installer from the [Releases](../../releases) section:  
  **Fuzzy-HydroGPT-RTC v2.0**.  

### 2. Login  
- Use the `Card.txt` file in the repository for credentials.  
- Enter your card number and password.  

### 3. Configure GPT  
- Enter your **OpenAI API key** and preferred **model name**.  
- Save configuration.  

### 4. Run Real-Time Monitoring  
- Load your **Excel/CSV input file**.  
- Start monitoring.  
- Predictions update automatically every cycle.  

### 5. Export & Analyze  
- Export results at any stage (**CSV/Excel/JSONL**).  
- Perform fuzzy uncertainty analysis or model evaluation.  

---

## 🎓 Academic Access  

For academic or long-term usage licenses, please contact:  
📧 **valeo@uvic.ca**

---
