<div align="center">

# 🌦️ Real-Time Air Quality Monitoring System

### IoT-Based Environmental Monitoring & Machine Learning

<p>
  <strong>ESP32</strong> •
  <strong>Blynk Cloud</strong> •
  <strong>Arduino C/C++</strong> •
  <strong>Python</strong> •
  <strong>Scikit-learn</strong>
</p>

<p>
  An integrated IoT and Machine Learning project for real-time environmental monitoring,
  cloud-based data visualization, and weather prediction.
</p>

<br>

![ESP32](https://img.shields.io/badge/ESP32-IoT-blue?style=for-the-badge&logo=espressif)
![Arduino](https://img.shields.io/badge/Arduino-C%2FC%2B%2B-00979D?style=for-the-badge&logo=arduino&logoColor=white)
![Python](https://img.shields.io/badge/Python-Data%20Science-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Blynk](https://img.shields.io/badge/Blynk-Cloud-23C48E?style=for-the-badge)
![Scikit Learn](https://img.shields.io/badge/Scikit--learn-ML-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)

</div>

---

## 📌 About The Project

**Real-Time Air Quality Monitoring System** is an academic IoT project that combines
embedded systems, environmental sensing, cloud connectivity, and Machine Learning.

The ESP32 collects real-time environmental measurements from multiple sensors and
displays the readings locally through a **20×4 I2C LCD**. Selected measurements are
also transmitted through Wi-Fi to **Blynk Cloud** for remote monitoring.

Alongside the IoT monitoring system, a Python-based Machine Learning workflow analyzes
historical Australian weather data and performs **RainTomorrow classification** using
multiple classification algorithms.

> **Project Focus:** Embedded Systems • IoT • Environmental Monitoring • Data Analysis • Machine Learning

---

# ✨ Core Features

<table>
<tr>
<td width="50%">

### 🌫️ Environmental Monitoring

- Dust density measurement
- Temperature monitoring
- Humidity monitoring
- Wind-speed measurement
- Rain detection
- Real-time sensor processing

</td>
<td width="50%">

### ☁️ IoT Connectivity

- ESP32 Wi-Fi connectivity
- Blynk Cloud integration
- Remote sensor monitoring
- Virtual channel data transmission
- Local LCD visualization

</td>
</tr>

<tr>
<td width="50%">

### 🤖 Machine Learning

- Weather dataset analysis
- Data preprocessing
- Feature preparation
- PCA
- Classification
- Cross-validation
- RainTomorrow prediction

</td>
<td width="50%">

### 📊 Data Analysis

- Python-based analysis
- Pandas & NumPy
- Matplotlib visualization
- Seaborn visualization
- Scikit-learn models
- Model performance comparison

</td>
</tr>
</table>

---

# 🏗️ System Architecture

```text
                         ┌──────────────────────┐
                         │        ESP32         │
                         │   Main Controller    │
                         └──────────┬───────────┘
                                    │
              ┌─────────────────────┼─────────────────────┐
              │                     │                     │
              ▼                     ▼                     ▼
       ┌─────────────┐       ┌─────────────┐       ┌─────────────┐
       │ Dust Sensor │       │    DHT11    │       │ Rain Sensor │
       │             │       │ Temp/Humidity│      │             │
       └─────────────┘       └─────────────┘       └─────────────┘
              │                     │                     │
              └─────────────────────┼─────────────────────┘
                                    │
                                    ▼
                           ┌─────────────────┐
                           │ Wind Sensor /   │
                           │   Anemometer    │
                           └────────┬────────┘
                                    │
                                    ▼
                           ┌─────────────────┐
                           │   20×4 I2C LCD  │
                           │ Local Monitoring│
                           └─────────────────┘
                                    │
                                    ▼
                              ┌───────────┐
                              │   Wi-Fi   │
                              └─────┬─────┘
                                    │
                                    ▼
                           ┌─────────────────┐
                           │   Blynk Cloud   │
                           │ Remote Monitoring│
                           └─────────────────┘


                    ┌─────────────────────────────┐
                    │ Historical Weather Dataset │
                    └──────────────┬──────────────┘
                                   │
                                   ▼
                         ┌───────────────────┐
                         │ Data Preprocessing│
                         └─────────┬─────────┘
                                   │
                                   ▼
                              ┌─────────┐
                              │   PCA   │
                              └────┬────┘
                                   │
                                   ▼
                         ┌───────────────────┐
                         │ ML Classification │
                         └─────────┬─────────┘
                                   │
                                   ▼
                         ┌───────────────────┐
                         │ RainTomorrow      │
                         │    Prediction      │
                         └───────────────────┘
