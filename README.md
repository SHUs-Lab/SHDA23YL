# SHDA23YL



# Data

The data zip file contains 4 subfolders corresponding different regions. California, Illinois, North Dakota, Nebraska. Each subfolder has two subfolders one for Aerial images (Aer), another for Digital Eelevation Model (DEM). 

# Usage
## Create a new conda environment:
   ```
   conda create --name culvert python=3.9
   activate culvert       # Windows
   conda activate culvert # Linux
   ```
## Clone this repo:
   ```
   git clone https://github.com/SHUs-Lab/SHDA23YL.git
   cd SHDA23YL
   ```

## Data Preparation

1. Unzip ClippedSample_5Areas.zip
2. Run [DataRead.py](https://github.com/SHUs-Lab/SHDA23YL/blob/main/DataRead.py "DataRead.py")
3. Run [VICalculation.py](https://github.com/SHUs-Lab/SHDA23YL/blob/main/VICalculation.py "VICalculation.py")

## Data Merge

[step0.merge_data.ipynb](https://github.com/SHUs-Lab/SHDA23YL/blob/main/step0.merge_data.ipynb "step0.merge_data.ipynb") is for merging the datasets and labels from 4 different regions.


## Neural Architecture Search with NNI

[step1.NNI.ipynb](https://github.com/SHUs-Lab/SHDA23YL/blob/main/step1.NNI.ipynb "step1.NNI.ipynb") is for NNI trying different model configurations with ResNet. 

## Latency Prediction
[step2.nn-Meter.ipynb](https://github.com/SHUs-Lab/SHDA23YL/blob/main/step2.nn-Meter.ipynb "step2.nn-Meter.ipynb") is for latency prediction using nn-Meter.

## Pareto Front Analysis
[step3.pareto_front.ipynb](https://github.com/SHUs-Lab/SHDA23YL/blob/main/step3.pareto_front.ipynb "step3.pareto_front.ipynb") is for Pareto front analysis with three objectives. 
1. Maximize accuracy
2. Minimize latency
3. Minimize model size