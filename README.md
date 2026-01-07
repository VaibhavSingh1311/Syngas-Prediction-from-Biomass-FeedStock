# Syngas-Prediction-from-Biomass-FeedStock
A comprehensive machine learning framework for predicting syngas composition from various biomass feedstocks using hybrid ensemble models. This project combines chemical engineering principles with advanced machine learning to create an accurate, fast, and interpretable prediction tool for biomass gasification.

### Features

1. Multi-Model Ensemble: Combines Random Forest, XGBoost, LightGBM, ANN, and SVR with custom stacking.

2. Multi-Biomass Support: Handles 1-4 biomass mixtures with property-weighted blending.

3. Real-Time Optimization: Differential evolution algorithm for maximizing H₂/CO yields.

4. Interactive Web Interface: Gradio-based UI with 5 functional tabs.

5. Physics-Informed Augmentation: Synthetic data generation maintaining thermochemical relationships

## Technical Details:

#### Dataset

1. Original: 87 experimental samples from literature

2. Augmented: 1,000 samples via physics-informed synthesis

3. Features: 20 total (14 numerical, 2 categorical, 4 targets)

4. Biomass Types: 23 distinct types (Type-A through Type-W)
   
#### Dataset Statistics

| Parameter | Range | Samples |
|-----------|-------|---------|
| Total Samples | - | 1,000 |
| Training Set | - | 800 (80%) |
| Test Set | - | 200 (20%) |
| Biomass Types | 23 types | - |
| Temperature | 500-950°C | - |
| S/B Ratio | 0.1-3.0 | - |
| ER Ratio | 0.1-2.8 | - |
| H₂ Content | 7.81-71.5% | - |
| CO Content | 5.61-52.88% | - |
| CO₂ Content | 0-41.13% | - |
| CH₄ Content | 0.61-26.5% | - |

---


#### Performance Comparison

| Model | Overall R² | H₂ R² | CO R² | CO₂ R² | CH₄ R² | MAE (%)  |
|-------|------------|-------|-------|--------|--------|---------|
| **Hybrid Ensemble** | **0.9718** | **0.9872** | **0.9763** | **0.9688** | **0.9550** | **0.882** |
| XGBoost | 0.9641 | 0.9776 | 0.9649 | 0.9611 | 0.9526 | 1.243 |
| Random Forest | 0.9577 | 0.9718 | 0.9606 | 0.9484 | 0.9501 | 1.382 |
| ANN | 0.9573 | 0.9760 | 0.9532 | 0.9553 | 0.9448 | 1.539 |
| SVR | 0.9146 | 0.9352 | 0.8742 | 0.9147 | 0.9342 | 2.082 |
| LightGBM | 0.8986 | 0.9281 | 0.8715 | 0.8975 | 0.8973 | 2.627 |

---

#### Feature Importance for H₂ Prediction

| Feature | Importance (%) | Chemical Significance |
|---------|---------------|----------------------|
| Temperature (°C) | 8.72 | Controls reaction kinetics and equilibrium |
| Ash Content | 4.92 | Inert material affecting heat transfer |
| Nitrogen (N) | 3.31 | Affects NH₃ and NOx formation |
| Sulfur (S) | 1.79 | Influences H₂S and COS production |
| Moisture | 2.37 | Energy required for evaporation |
| Carbon (C) | 2.33 | Primary feedstock element |
| Fixed Carbon | 2.23 | Char available for gasification reactions |
| Hydrogen (H) | 0.94 | Direct hydrogen source |
| Volatile Matter | 0.56 | Easily devolatilized components |
| Oxygen (O) | 0.51 | Affects oxidation state |

---







