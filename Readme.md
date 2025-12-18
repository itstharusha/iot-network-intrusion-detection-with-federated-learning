# IoT Network Intrusion Detection with Privacy-Preserving Federated Learning

## Project Overview
This Kaggle notebook implements a scalable Intrusion Detection System (IDS) for IoT networks using the CICIoT2023 dataset. The system classifies 33 types of IoT attacks (e.g., DDoS, MITM) from network flows while incorporating privacy-preserving federated learning to simulate training across distributed devices without sharing raw data.

### Objectives
- Build a hybrid CNN-LSTM model for sequence-based attack classification.
- Handle extreme class imbalance and high-dimensional features (80+ per flow).
- Simulate federated learning using the Flower library to mimic real-world IoT privacy constraints.
- Evaluate the model on unseen attacks and deploy a real-time inference simulation.
- Incorporate explainability with SHAP and LIME for ethical AI practices.

### Dataset
- **Source**: [CICIoT2023 on Kaggle](https://www.kaggle.com/datasets/madhavmalhotra/unb-cic-iot-dataset) (8.42 GB, 63 CSV files).
- **Usage**: We will sample 20% of the dataset for efficiency while maintaining the "real deal" scale, processed with Dask for big data handling.
- **Key Stats**:
  | Aspect | Details |
  |--------|---------|
  | Size | 8.42 GB |
  | Files | 63 CSVs |
  | Features | 80+ per flow (e.g., packet sizes, protocols) |
  | Classes | 34 (33 attacks + normal) |
  | Imbalance | Normal traffic ~80% |

### Why Complex & Unique?
- Extreme imbalance and high dimensionality require advanced techniques like SMOTE/ADASYN.
- Federated setup differentiates from standard classifiers by enforcing privacy.
- Showcases skills: Big data (Dask), DL optimization (CNN-LSTM), Federated Learning (Flower), Explainability (SHAP/LIME).

### Tech Stack & Skills Showcased
- **Big Data**: Dask for distributed processing.
- **Imbalance Handling**: SMOTE from imbalanced-learn.
- **Model**: Hybrid CNN-LSTM in TensorFlow/Keras.
- **Federated Learning**: Flower for simulation.
- **Explainability**: SHAP and LIME.
- **Optimization**: Early stopping, mixed precision for DL efficiency.
- **Ethical AI**: Privacy focus in federated setup.

**Note**: Run this notebook on Kaggle with GPU accelerator enabled. Monitor memory with `!free -h` and use checkpoints.

## Future Work
Here are the most exciting next steps to take this project even further (perfect for your portfolio or next iteration):

- Implement the full federated learning loop with Flower → train across 50–150 simulated IoT clients and fix zero-day performance on minority attacks.
- Add data augmentation using GANs (e.g., WGAN) to generate synthetic samples for rare attack classes and further reduce imbalance.
- Experiment with more advanced aggregation methods (FedProx, FedMADE, Scaffold) to handle non-IID data across heterogeneous IoT devices.
- Integrate lightweight models (e.g., Transformer or TabTransformer) and nature-inspired optimization (e.g., EEFO) for better accuracy and lower edge-device latency.
- Add physical-layer features (Zigbee/LoRa) and test on newer devices (healthcare sensors, industrial IIoT) to make the system more realistic.
- Explore real-time deployment on Raspberry Pi + Flower and combine with blockchain for tamper-proof model updates.
- Extend explainability with per-client SHAP in federated setting and build a dashboard showing attack predictions live.

These improvements will push detection rates toward 99%+ while keeping full privacy.
"# iot-network-intrusion-detection-with-federated-learning" 
