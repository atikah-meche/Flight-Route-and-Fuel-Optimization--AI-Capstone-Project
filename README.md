# Flight-Route-and-Fuel-Optimization--AI-Capstone-Project
This repository includes the capstone project for our course CS-333 AI and Machine Learning. The main aim of the project was to use Machine Learning or Deep Learning methods to an engineering problem. Our code used ADS-B dataset from different flights and the openap.dev combined to map the routes of different flights and to compute their fuel flow.
# ✈️ Aircraft Fuel & Route Optimization

## 📌 Overview

This project focuses on optimizing aircraft fuel consumption and route efficiency using real flight trajectory data combined with machine learning models and engineering constraints.

We integrate:

* Real-world ADS-B flight data
* Feature engineering (temporal + physical)
* Machine learning (baseline + advanced models)
* Physics-based constraints for realistic outputs

---

## 📂 Dataset

We use historical ADS-B Exchange data in compressed JSON format.

🔗 You can preview/download the dataset here before running the code:
https://samples.adsbexchange.com/readsb-hist/2025/12/01/000000Z.json.gz

This dataset contains:

* Altitude
* Ground speed
* Track angle
* Vertical rate
* Flight trajectories

---

## ⚙️ How to Use

### 🔹 1. Adjust Dataset Size (Block 2)

Users can control how much data is used in the model by modifying:

* Number of flights
* Flight duration (hours)

This allows:

* Faster testing with smaller datasets
* More accurate modelling with larger datasets

---

### 🔹 2. Route Visualization (Block 6)

Users can select any flight from the dataset and:

* Compare **actual route vs optimized route**

This helps:

* Visually evaluate model performance
* Understand how optimization affects trajectory
* Demonstrate real-world applicability

---

## 🤖 Machine Learning Approach

* **Baseline Model:** Linear Regression
* **Advanced Model:** Gradient Boosting

We use multiple models during development for benchmarking, but the final evaluation focuses on:

* Simplicity (baseline)
* Performance (advanced)

---

## 🌦️ External Integrations

### 🔹 Fuel Flow Calculations

Fuel-related estimations are supported using:

* **OpenAPI.dev**

---

### 🔹 NOAA Weather Integration

We also implemented a NOAA-based dataset:

* Includes environmental/weather factors
* Currently produces **lower R² scores**

📌 This indicates:

* Either insufficient feature alignment
* Or need for better weather–flight interaction modelling

👉 Identified as an area for improvement.

---

📌 Interpretation:

* R² = 1 → Perfect prediction
* R² = 0 → Model performs like a mean guess

👉 In our case:
Higher R² = better understanding of fuel behaviour

---

## ⚙️ Engineering Constraints

To ensure realistic predictions, we apply:

* Wind speed limits (based on jet stream bounds)
* Fuel consumption caps per segment

These prevent:

* Physically impossible outputs
* Unrealistic optimization paths

---

## 🚀 Future Improvements

* Improve NOAA-based model performance
* Integrate real-time weather APIs
* Extend to multi-objective optimization (fuel + time + emissions)
* Explore reinforcement learning for adaptive routing

---

## 📁 Repository Structure

* `notebooks/` → Main development notebooks
* `src/` → Modular code (cleaning, modelling, utilities)
* `outputs/` → Results, plots, trained models

---

## 📬 Notes

* Ensure all dependencies are installed (`requirements.txt`)
* Large datasets may increase runtime
* API calls may require a stable internet connection

---

## 🧠 Summary

This project demonstrates how combining:

* Data-driven models
* Engineering constraints
* Real-world aviation data

can lead to meaningful improvements in aircraft fuel efficiency and route optimization.
