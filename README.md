# Multimodal Property Valuation using Tabular Data and Satellite Imagery

## Project Overview
This project builds a **multimodal regression framework** to predict real estate property prices by combining traditional **tabular housing data** with **satellite imagery**. The objective is to demonstrate that visual neighborhood context (such as greenery, density, and surrounding infrastructure) can improve property valuation beyond tabular features alone.

---

## Dataset
**Source:** Kaggle – House Sales Prediction Dataset  

**Target Variable:**
- `price`

**Key Tabular Features:**
- `bedrooms`, `bathrooms`
- `sqft_living`, `sqft_lot`
- `sqft_living15`, `sqft_lot15`
- `condition`, `grade`
- `view`, `waterfront`
- `lat`, `long`

Latitude and longitude are used to fetch satellite images for each property.

---

## Satellite Imagery
- Satellite images are programmatically fetched using **latitude and longitude**
- **Mapbox Static Images API** is used
- Images are resized to `224×224`
- A representative subset of images is used due to API and computational constraints

---

## Methodology (High Level)
- Data preprocessing and feature scaling
- Tabular-only baseline regression model
- CNN-based image feature extraction using a pretrained ResNet
- Multimodal fusion by concatenating tabular features and image embeddings
- Performance comparison between tabular and multimodal models

---

## Repository Structure

---

## How to Run
1. Run `preprocessing.ipynb`  
   - Generates cleaned data, scaled features, and coordinate files

2. Run `data_fetcher.py`  
   - Downloads satellite images using Mapbox API

3. Run `model_training.ipynb`  
   - Trains models and generates `enrollno_final.csv`

---

## Technologies Used
- Python
- Pandas, NumPy
- Scikit-learn
- PyTorch
- Mapbox Static Images API

---

## Author
**Name:** Arun Kaarthikeyan R  
**Enrollment Number:** 23321006
