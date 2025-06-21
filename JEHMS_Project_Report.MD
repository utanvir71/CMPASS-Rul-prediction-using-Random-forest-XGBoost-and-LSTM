
# Jet Engine Health Monitoring System (JEHMS) - Project Report

---

## 🔹 1. Introduction
Jet engines naturally degrade over time due to high mechanical and thermal stress. Unplanned engine failures are expensive and dangerous. This project aims to build a Jet Engine Health Monitoring System (JEHMS) that predicts Remaining Useful Life (RUL) using the NASA C-MAPSS dataset and triggers alerts to support predictive maintenance.

---

## 🔹 2. Objectives
- Predict RUL with RMSE < 15 cycles.
- Trigger alerts when RUL < 30, <20, and <10 cycles.
- Ensure system is modular, accurate, and explainable.

---

## 🔹 3. Dataset Overview
- **Source**: NASA C-MAPSS
- **Content**: Engine sensor readings over multiple operating cycles until failure
- **Processing**:
  - Normalized per engine
  - Sequence windows created for LSTM input

---

## 🔹 4. Methodology

### 📦 Functional Decomposition:
1. **Data Ingestion**
2. **Preprocessing & Cleaning**
3. **Feature Engineering**
4. **LSTM Model Training**
5. **RUL Prediction**
6. **Alert Generation**
7. **Visualization**

### 🧠 Model:
- Long Short-Term Memory (LSTM) neural network
- Sequence-based input (time-series of sensor readings)
- Trained to predict RUL for each engine unit

---

## 🔹 5. Alert System
- Thresholds:
  - RUL < 30 → Notice
  - RUL < 20 → Warning
  - RUL < 10 → Critical
- Alerts displayed as color-coded labels
- Rule-based fallback ensures robustness

---

## 🔹 6. Testing & Evaluation
- Unit tested preprocessing, feature pipeline
- End-to-end integration tested with full system
- Final RMSE on test set: ~12.4
- Confirmed alerts triggered correctly across edge cases

---

## 🔹 7. Reliability Analysis
- Components in series (sensor → model → alert): risk of single point failure
- Added rule-based parallel backup → overall reliability improved to ~99.5%

---

## 🔹 8. Project Management
- Used Gantt chart to plan tasks over 12 weeks
- Google Colab used to avoid hardware limitations
- Milestones:
  - W2: Preprocessing
  - W5: Model complete
  - W8: Alerts integrated
  - W12: Final report/presentation

---

## 🔹 9. Ethical and Legal Considerations
- Public dataset used ethically
- ChatGPT assisted in code, but all final logic validated and understood
- Limitations of the model clearly communicated

---

## 🔹 10. Results & Future Work
- ✅ Achieved RMSE ~12.4
- ✅ Reliable alert logic
- 🚀 Future: Real-time streaming, UI dashboard

---

## 🔹 11. Team Reflection
While each team member played a role, task coordination, testing, and code integration were key. Regular check-ins and clear communication helped ensure delivery under tight timelines.

---
