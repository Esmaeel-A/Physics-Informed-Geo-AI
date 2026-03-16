# Physics-Informed-Geo-AI
This repository contains the submission for the I-GUIDE Spatial AI Challenge. We present a novel framework that hybridizes Satellite Foundation Model Embeddings with Mechanistic Hydrological Equations to estimate daily irrigation intensity at 1km resolution across the California Central Valley.

##  Core Innovation
Unlike standard "black-box" machine learning models that map pixels directly to irrigation volumes, this framework uses a **Physics-Informed Neural Network (PINN)** architecture based on **TabNet**. 

**Key Contribution:** We hypothesize that high-dimensional embeddings (AlphaEarth) capture latent soil properties. Our model uses these embeddings to **parameterize** the physical environment (estimating $Z, K, b$ parameters for the SM2RAIN equation) rather than simply curve-fitting, ensuring all predictions remain strictly constrained by the laws of hydrology.

## Repository Structure
* `PINN_GEO-AI_Irrigation.ipynb`: The primary notebook containing data processing, the PINN architecture, and regional validation.
* `physics_tabnet_best_Final.pt`: Pre-trained model weights (Restored in Section 4 of the notebook).
* `requirements.txt`: List of required Python libraries for environment reproducibility.

## Installation & Reproducibility
To ensure a clean run on the I-GUIDE platform or a local machine:

1. Clone the repository:
   ```bash
   git clone [https://github.com/Esmaeel-A/PINN_IrrigationVolumeQuantification.git](https://github.com/Esmaeel-A/PINN_IrrigationVolumeQuantification.git)
