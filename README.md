# SSP-project

Language Identification (LID) using prosodic features at the syllable level.

![Language Distribution](https://img.shields.io/badge/Jupyter-80.5%25-orange) ![MATLAB](https://img.shields.io/badge/MATLAB-19.5%25-blue)

## Overview

This project implements **Language Identification (LID)** using solely prosodic features on the syllable level. The system identifies languages based on prosodic characteristics extracted from audio signals.

## Features

- 🎵 **Prosodic Feature Extraction** - Syllable-level prosody features
- 🗣️ **Language Identification** - Multi-language LID system
- 📊 **GMM Implementation** - Gaussian Mixture Model for classification
- 🔬 **MATLAB Processing** - Audio feature extraction in MATLAB
- 📓 **Jupyter Notebook** - Main implementation and analysis

## Requirements

- **MATLAB** - For audio processing and feature extraction
- **Python** - For GMM implementation
- **Jupyter Notebook** - For running the main code
- **NumPy, SciPy, scikit-learn** - Python dependencies

## Project Structure

```
SSP-project/
├── feat/              # Extracted features (auto-generated)
│   ├── test/         # Test features
│   └── train/        # Training features
├── testdata/         # Test audio data (.mat files)
├── traindata/        # Training audio data (.mat files)
├── trained_model/    # Trained GMM models (.pkl files)
├── temp/             # Temporary files
├── GMM.ipynb         # Main implementation
├── prosody.m          # Prosody feature extraction
├── VOP.m              # Syllable boundary detection
├── voiced.m           # Voiced/unvoiced detection
├── freq.m             # Fundamental frequency extraction
├── mat_test.ipynb     # MATLAB testing
├── Output.json        # Results output
└── ssp.pdf            # Project documentation
```

## Usage

### Step 1: Convert Audio to Features

1. Convert `.wav` files to `.mat` format using `prosody.m`
   - Note: You may need to change the mat file name manually

### Step 2: Organize Data

Place your data in the following structure:

**Test Data:**
```
testdata/
├── Language1/
│   ├── language1_1.mat
│   ├── language1_2.mat
│   └── ...
├── Language2/
│   └── ...
```

**Train Data:**
```
traindata/
├── Language1/
│   ├── language1_1.mat
│   ├── language1_2.mat
│   └── ...
├── Language2/
│   └── ...
```

### Step 3: Run the Code

1. Open `GMM.ipynb` in Jupyter Notebook
2. Run all cells to:
   - Extract features from test/train data
   - Train GMM models for each language
   - Generate predictions and output

### Step 4: View Results

- Trained models are saved in `trained_model/` as `.pkl` files
- Features are stored in `feat/test/` and `feat/train/`
- Results are output to `Output.json`

## Code Files

- **`GMM.ipynb`** - Main GMM implementation for language identification
- **`prosody.m`** - Extracts prosody syllable-level features from `.wav` files
- **`VOP.m`** - Extracts syllable boundary information
- **`voiced.m`** - Extracts voiced/unvoiced information
- **`freq.m`** - Extracts fundamental frequency information
- **`mat_test.ipynb`** - MATLAB testing notebook

## Language Distribution

- **Jupyter Notebook**: 80.5% - Main implementation and analysis
- **MATLAB**: 19.5% - Audio processing and feature extraction

## Documentation

See `ssp.pdf` for detailed project documentation and methodology.

## License

This project is licensed under the **MIT License**.

See the [LICENSE](https://github.com/AakashR13/SSP-project/blob/main/LICENSE) file in the repository for full license details.

