# Human Activity Recognition (HAR) on Edge Devices

An end-to-end TinyML pipeline built using Edge Impulse and the UCI HAR Smartphone Dataset. The project processes triaxial accelerometer and gyroscope data to classify human activities with high accuracy and ultra-low embedded resource consumption.

## 📊 Performance Benchmarks

| Metric | Result |
| :--- | :--- |
| **Validation Accuracy** | **95.0%** |
| **Inference Engine** | Edge Impulse EON™ Compiler |
| **Inference Latency** | **1 ms** |
| **Peak RAM Usage** | **1.8 KB** |
| **Flash Usage** | **16.5 KB** |

## ⚙️ Architecture & Pipeline

1. **Signal Preprocessing:** Python (Google Colab) windowing raw 50 Hz inertial sensor signals into 2.56-second segments.
2. **DSP Feature Extraction:** Spectral Analysis (FFT) extracting frequency/time-domain features across 6 axes.
3. **Classification Model:** Quantized (Int8) Keras Neural Network classifier.
4. **Target Deployment:** Standalone C++ library compiled via the EON™ Compiler.

## 🖼️ Visual Evaluation Metrics

### DSP Spectral Analysis
![DSP Features](dsp_spectral_features.png)

### Model Accuracy & Confusion Matrix
![Confusion Matrix](confusion_matrix_accuracy.png)

### On-Device Hardware Benchmarks
![On-Device Performance](on_device_performance_benchmarks.png)

## 📁 Repository Files

* `cpp_edge_library.zip`: Standalone C++ deployment package for microcontrollers.
* `edge_impulse_csvs.zip`: Preprocessed and windowed dataset formatted for Edge Impulse.
* `HAR-EdgeML - Classifier - Edge Impulse.html`: Offline HTML report backup of project dashboard.

## 🔗 Dataset Reference
* UCI Machine Learning Repository / Kaggle HAR Dataset: [Human Activity Recognition with Smartphones](https://www.kaggle.com/datasets/uciml/human-activity-recognition-with-smartphones)
