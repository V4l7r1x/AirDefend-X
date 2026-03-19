# AirDefend-X: Hybrid ADS-B Security Gateway 🛡️✈️

**AirDefend-X** is a multi-layered security framework designed to detect and mitigate **False Data Injection (FDI)** attacks in Automated Dependent Surveillance-Broadcast (ADS-B) telemetry. This project combines cryptographic authentication with machine learning-based behavioral analysis.

## 🌟 Key Features
- **Identity Layer**: Implements **RSA-2048** digital signatures to verify aircraft origin and prevent spoofing.
- **Behavioral Layer**: Uses an **Unsupervised Isolation Forest** AI model to detect "Ghost" aircraft based on impossible physics (velocity/altitude anomalies).
- **Temporal Layer**: Sequence-based delta checking to prevent discontinuous "teleportation" attacks.
- **Interactive Dashboard**: Real-time ATC visualization built with **Streamlit** and **PyDeck**.

## 📊 Performance & Benchmarking
The system was evaluated using the **OpenSky Network** dataset. 
- **Recall**: >98% (Successfully identifies high-velocity ghost injections).
- **Precision**: 99% (Minimal false alarms on legitimate high-performance aircraft).
- **F1-Score**: ~0.99.



## 🛠️ Installation & Usage

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/V4l7r1x/AirDefend-X.git](https://github.com/V4l7r1x/AirDefend-X.git)
   cd AirDefend-X

2. **Data Acquisition:**

The project includes a sample dataset for immediate testing.
* **Dataset Location**: `data/opensky.csv`
* **Source**: [OpenSky Network](https://opensky-network.org/)
* **Note**: If you wish to use a larger dataset, replace `opensky.csv` in the `/data` folder and ensure the column headers match.
