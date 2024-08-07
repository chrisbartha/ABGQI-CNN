# ABGQI-CNN Acoustic Classifier

This repository is based on the [ABGQI-CNN](https://github.com/CQuinn8/ABGQI-CNN) by Colin Quinn et al.. The original project provides the foundational implementation of a Convolutional Neural Network (CNN) for soundscape classification.

## Table of Contents

- [Project Overview](#project-overview)
- [Features](#features)
- [Installation](#installation)
- [List of Scripts for Manuscript Figures, Tables, and Results](#list-of-scripts-for-manuscript-figures-tables-and-results)
- [Results Sections](#results-sections)
- [Contributors](#contributors)
- [License](#license)

## Project Overview

This project involves the implementation and deployment of a Convolutional Neural Network (CNN) for audio classification tasks. The system is designed to analyze and classify different soundscapes, providing insights into the acoustic environment. This work was funded under the Soundscapes 2 Landscapes, NASA’s Citizen Science for Earth Systems Program 16-CSESP 2016-0009 and is citable using the Zenodo DOI. Note: Please be aware that underlying software, specifically for the CNN implementation, may not continue stability as python libraries are updated.

### Features

1. **Generate Figures and Results:**
   - Reproduce all code-based figures, tables, and numerical results as presented in the published manuscript.

2. **Retrain the ABGQI-CNN:**
   - Modify and improve the CNN model to adapt to new data or research requirements.

3. **Apply to Novel Data:**
   - Process new acoustic data to generate 2-second Mel spectrograms, perform ABGQI-CNN inference, optimize f-score thresholds, and classify soundscape components.

## Installation

### Python Environment Setup

- Two Anaconda python environments are included in .yml files under the `envs` directory. These environments provide the necessary libraries for spectrogram generation, CNN training, and inference.

### R Environment Setup

- Required R libraries are listed in `envs/R_requirements.txt`. Use the `R_lib_install.R` file to install all packages automatically, or install each package manually:
  1. **RStudio:** Open `R_lib_install.R`, uncomment line 3, and specify the path to `envs/R_requirements.txt`.
  2. **Command Line:** Run `R_lib_install.R <envs/R_requirements.txt>`.

  **Note:** If errors occur, manually install packages using `install.packages("<package name>")`.

## List of Scripts for Manuscript Figures, Tables, and Results

- **Fig 1:** NA - derived using non-public GIS data in ArcGIS
- **Fig 2:** NA - conceptual figure, no code used
- **Fig 3:** NA - conceptual figure, no code used
- **Fig 4:** NA - conceptual figure, no code used
- **Fig 5:** `3_cnn_threshold_optimization_and_accuracy-R/code/0_CNN_threshold_optimization.R`
- **Fig 6:** `4_ABGQI_environ_analyses-R/code/0_ABGQIU_temporal_plotting_faceted_LCLU_figure6.R`
- **Fig 7:** `4_ABGQI_environ_analyses-R/code/1_KWDunn_tests-LULC_Roads_Annual.R`
- **Fig 8:** `4_ABGQI_environ_analyses-R/code/1_KWDunn_tests-LULC_Roads_Annual.R`
- **Table 1:** Not related to code, can be derived from Mel spectrogram training, validation, testing data set
- **Table 2:** `3_cnn_threshold_optimization_and_accuracy-R/code/1_CNN_accuracy_metrics.R`
- **Table 3:** `4_ABGQI_environ_analyses-R/code/3_multivariate_regression.R`

## Results Sections

- **3.1 Model Performance:** Most metrics in `3_cnn_threshold_optimization_and_accuracy-R/code/1_CNN_accuracy_metrics.R`; cross-validation numbers in data repository; rate of unidentified sound from `4_ABGQI_environ_analyses-R/code/0_ABGQIU_temporal_plotting_faceted_LCLU_figure6.R`
- **3.2 Statistical Analyses of Soundscape Components:** `4_ABGQI_environ_analyses-R/code/0_ABGQIU_temporal_plotting_faceted_LCLU_figure6.R`
- **3.2.1 Diurnal LULC Patterns:** `4_ABGQI_environ_analyses-R/code/2_MannWhitney_tests-day_night.R` and `0_ABGQIU_temporal_plotting_faceted_LCLU_figure6.R`
- **3.2.2 Annual and Date of Deployment Differences:** `4_ABGQI_environ_analyses-R/code/1_KWDunn_tests-LULC_Roads_Annual.R`
- **3.2.3 Daytime LULC Stratification:** `4_ABGQI_environ_analyses-R/code/1_KWDunn_tests-LULC_Roads_Annual.R`
- **3.2.4 Distance to Roads:** `4_ABGQI_environ_analyses-R/code/1_KWDunn_tests-LULC_Roads_Annual.R`
- **3.2.5 Effect of Wind Speed on Soundscapes:** Not included as contains non-public GIS data
- **3.3 Factors Affecting Amount of Soundscape Components:** `4_ABGQI_environ_analyses-R/code/3_multivariate_regression.R`

## Contributors

See the list of contributors [here](CONTRIBUTORS.md).

## License

This project is licensed under the MIT License. See the full license [here](LICENSE).

