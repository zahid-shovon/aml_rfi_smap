
# Detection of Radio Frequency Interference Affecting Soil Moisture Retrieval Quality in NASA's SMAP Passive Microwave Observations

## Overview
This project investigates the detection of **Radio Frequency Interference (RFI)** affecting **soil moisture retrieval** quality in **NASA's SMAP Passive Microwave Observations**. Using a variety of **advanced machine learning algorithms**, including **Logistic Regression**, **Random Forest**, **MLP**, **1D CNN**, and **XGBoost**, the goal is to detect RFI in passive microwave data and improve the quality of soil moisture and **Sea Surface Temperature (SST)** products. Additionally, **SHAP** is used to pr...

## Key Objectives
- **Detect RFI** in the passive microwave radiometer data collected by **NASA's SMAP satellite**.
- **Improve soil moisture retrieval** quality by mitigating the impact of RFI.
- **Compare and contrast machine learning models** to evaluate their performance in detecting RFI.
- **Explain model decisions** using **SHAP** to improve the transparency of model results.

## Dataset
The dataset used in this project comes from the **NASA SMAP L1B Radiometer Brightness Temperature** product, available from NASA's **NSIDC DAAC**. This dataset includes calibrated, geolocated brightness temperatures measured by the SMAP radiometer, along with additional features like quality flags, geolocation data, and RFI-related attributes.

- **Data Source**: [SMAP L1B Radiometer Brightness Temperature](https://nsidc.org/data/SPL1BTB)

## Prerequisites
To run the code and reproduce the analysis, you will need the following libraries:

- Python 3.x
- TensorFlow
- scikit-learn
- XGBoost
- SHAP
- Plotly
- UMAP
- pandas
- numpy
- matplotlib
- h5py

You can install the necessary libraries using pip:

```bash
pip install tensorflow scikit-learn xgboost shap plotly umap-learn pandas numpy matplotlib h5py
```

## Project Structure
The repository includes the following files:

- **AML_SMAP_Detection.ipynb**: Jupyter notebook containing the full code for the project.
- **AML_SMAP_Models.py**: Python script with the implementation of machine learning models and evaluation methods.
- **SMAP_L1B_TB_59906_A_20260419T160238_R19240_001.h5**: Example dataset used for RFI detection.
- **outputs/**: Folder containing the model evaluation results and visualizations.
- **README.md**: The readme file you are currently reading.

## File Paths
The main file paths in the code are set as:

- **Dataset**: `/content/drive/MyDrive/AML/Data/SMAP_L1B_TB_59906_A_20260419T160238_R19240_001.h5`
- **Outputs**: `/content/drive/MyDrive/AML/Outputs`

Ensure that the correct paths are set in your environment before running the code.

## Steps to Run the Code
1. Clone the repository:

```bash
git clone https://github.com/your-username/aml_rfi_smap.git
```

2. Open the Jupyter notebook `AML_SMAP_Detection.ipynb` in **Google Colab** or **Jupyter Lab**.
3. Mount your Google Drive to access the dataset and save outputs (in case you're using Colab):

```python
from google.colab import drive
drive.mount('/content/drive')
```

4. Execute the code cells step by step. Each cell performs a distinct task, including:
   - **Data Preprocessing**
   - **Model Training** (Logistic Regression, RF, CNN, etc.)
   - **Evaluation** (including ROC-AUC, F1 Score, and Precision-Recall curves)
   - **SHAP Analysis** for model explainability.

5. Check the `outputs/` directory for the generated figures, evaluation results, and models.

## Results
- **Model Comparison**: The models are evaluated on their ability to detect RFI and improve the quality of soil moisture retrieval.
- **SHAP Plots**: SHAP plots are used to explain the feature importance and provide transparency in the model's decisions.
- **Subset Experiment**: A subset of the data was used to check model stability and data efficiency.

## Limitations
- **Data Availability**: The dataset used in this project is limited to specific SMAP L1B radiometer products, which may not represent the full range of global conditions.
- **Computational Resources**: The models, especially deep learning models, require significant computational power for training.

## Future Work
- **RFI Mitigation Techniques**: Explore more sophisticated RFI mitigation methods such as signal processing-based techniques or hybrid models combining machine learning and traditional DSP methods.
- **Global Application**: Apply the trained models to different geographic regions and satellite data to generalize the findings.
- **Model Optimization**: Improve model performance by tuning hyperparameters, incorporating additional features, or using more advanced architectures.

## Ethical and Legal Considerations
- **Data Privacy**: The dataset used is publicly available and does not contain any personal data.
- **RFI in Protected L-Band**: The issue of RFI in the L-Band is particularly important due to international regulations (ITU) that protect this frequency for scientific and communication purposes.
- **UN Implications**: Accurate soil moisture data is crucial for **UNDP**, **WFP**, and other global organizations for applications in disaster relief, agriculture, and climate change monitoring.
- **Commercial Impacts**: RFI in passive microwave data could severely impact commercial sectors, especially in remote sensing, agriculture, and environmental monitoring.

## Acknowledgments
I would like to acknowledge **Prof. Ciprian Daniel Neagu** for his unwavering support and guidance throughout this project. His acceptance of the selected topic has been crucial in aligning the project with both my academic and career goals.

## Links
- [GitHub Repository](https://github.com/your-username/aml_rfi_smap)
- [Google Drive (Dataset)](https://drive.google.com/drive/folders/1sBCZBsKjUX6fOllrCUV4MtndDCf7VxXM?usp=sharing)
- [SMAP Data Source](https://nsidc.org/data/SPL1BTB)


