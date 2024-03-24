# ECG Anomaly Detection using convolutional neural network 
### Classification

The repository contains code for Master's degree dissertation -
**ECG Anomaly Detection using convolutional neural network**.

The repository follows _config_ principle and can be run in the following modes:

- Training - use `train.py --config configs/training/ECGNet.json` to train the model
- Validation - use `inference.py --config configs/inference/config.json` to validate the model

All available models and all necessary information are described below

**Python 3.7** and **PyTorch** are used in the project

## Getting started

Training quick start:

1. [Download](https://physionet.org/static/published-projects/mitdb/mit-bih-arrhythmia-database-1.0.0.zip)
   and unzip files into `mit-bih` directory
2. Install requirements via `pip install -r requirements.txt`
3. Generate 2D data files running `cd scripts && python dataset-generation-pool.py`
4. Create `json` annotation files
   - For 2D model - `cd scripts && python annotation-generation-2d.py`
5. Run training - `python train.py --config configs/training/ECGNet.json`