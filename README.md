# EdgeAI-Cattle: Edge AI-Powered Multi-Modal Sensor Fusion for Early Cattle Disease Detection


**EdgeAI-Cattle** is an edge AI-powered wearable sensor system with multi-modal sensor fusion for early disease detection in cattle operating in remote pasture environments. The system achieves **92.3% accuracy**, detects diseases **22.5 hours before clinical symptoms**, and operates **offline** without cloud dependency.

## 🎯 Key Features

- **Multi-Modal Sensor Fusion**: Integrates 6 heterogeneous sensors (accelerometer, gyroscope, temperature, GPS, acoustic, thermal)
- **Edge AI Deployment**: Runs on ESP32 (240 MHz, 520 KB SRAM) with 87 ms latency
- **Early Disease Detection**: Detects mastitis, lameness, ketosis, and respiratory infections 6–48 hours early
- **Offline Operation**: No internet required, ideal for remote pastures
- **Low Power**: 95 mW consumption, 14-day battery life
- **INT8 Quantization**: 450 KB model size (75% reduction from FP32)

## 📊 Performance Metrics

| Metric | Value |
|--------|-------|
| Accuracy | **92.3%** |
| Sensitivity | **90.1%** |
| Specificity | **93.8%** |
| F1-Score | **89.7%** |
| Early Detection Time | **22.5 hours** (mean) |
| Inference Latency | **87 ms** |
| Power Consumption | **95 mW** |
| Model Size | **450 KB** (INT8) |

## 🚀 Quick Start

### Installation

```bash
# Clone repository
git clone https://github.com/yourusername/EdgeAI-Cattle.git
cd EdgeAI-Cattle

# Create virtual environment
python -m venv venv
source venv/bin/activate  # Linux/Mac
# or
venv\Scripts\activate  # Windows

# Install dependencies
pip install -r requirements.txt
```

### Train Model

```bash
# Using Python script
python src/train.py --config config/training_config.yaml

# Or using bash script
./scripts/run_training.sh
```

### Run Inference

```bash
python src/inference.py --model models/edgeai_cattle.pth --data data/processed/test_data.npy
```

### Convert to TensorFlow Lite (for ESP32)

```bash
./scripts/convert_to_tflite.sh
```

## 🏗️ System Architecture
