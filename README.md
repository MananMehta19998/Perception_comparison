# Duckietown Perception Pipeline

This repository contains the complete implementation of a classical perception pipeline and CNN-based approach for object recognition in the Duckietown environment.

## 📁 Project Structure

```
perception_pipeline/
├── perception/           # Classical perception (Canny, Hough, Hu Moments)                            
├── integration/          # End-to-end simulation and logging
├── final_dataset/        # Dataset utilities (splitting, generation)
├── utils/                # Helper functions for math, image, graphs
├── cnn_model.py          # CNN architecture
├── train_cnn.py          # CNN training script
├── test_cnn.py           # CNN testing script
```

## 📦 Dependencies

Install core Python dependencies:

```bash
pip install numpy pandas matplotlib scipy opencv-python torch torchvision joblib
```



## 🚀 Running the Pipeline

### Classical Pipeline

```bash
PYTHONPATH=. python3 integration/feature_stats.py dataset
```


```bash
PYTHONPATH=. python3 integration/simulate_perception.py
```

### CNN-based Perception

```bash
PYTHONPATH=. python3 integration/simulate_perception_cnn.py
```

### Training the CNN

```bash
PYTHONPATH=. python3 train_cnn.py
```

### Testing the CNN

```bash
PYTHONPATH=. python3 test_cnn.py
```

## 🧪 Evaluation Metrics

The pipeline includes:
- Accuracy and noise robustness plots
- Runtime and memory logging
- Feature analysis using Hu Moments and Hough Transform
- Class-wise degradation under Gaussian noise

## 📂 Dataset

Ensure the `final_dataset/` directory is properly populated. You can use:

```bash
python final_dataset/split_dataset.py
```
