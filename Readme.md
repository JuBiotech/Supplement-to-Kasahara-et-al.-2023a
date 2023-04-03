# Code Supplement to: Enabling oxygen-controlled microfluidic cultures for spatiotemporal microbial single-cell analysis (Kasahara et. al) (submitted)

This repository provides reproducible microscopy image analysis to reproduce the reported data in our paper.

## Microscopy Data

Our microscopy data is available [here](https://fz-juelich.sciebo.de/s/KTBjtTZBZawpClS) but it is described in the next section how to download it automatically for reproduction.

## Segmentation and Fluorescence Analysis

In order to reproduce the result extraction from the microscopy images we provide the analysis scripts. Please follow the steps below to reproduce our results:

1. Clone our repo
    ```bash
    git clone https://github.com/JuBiotech/Supplement-to-Kasahara-et-al.-2023a.git Supplement-to-Kasahara-et-al
    cd Supplement-to-Kasahara-et-al
    ```

1. Download the microscopy data
    ```bash
    wget -O data.zip https://fz-juelich.sciebo.de/s/KTBjtTZBZawpClS/download
    unzip data.zip
    ```

1. Create the analysis environment using [anaconda](https://www.anaconda.com/):

    ```bash
    conda env create -f conda.yml
    conda activate oxygen-analysis
    ```

1. Start the `jupyter` notebook server
    ```
    jupyter notebook
    ```

    and navigate to the `MetaScript.ipynb` file. Executing the cells in the file will reproduce and plot the fluorescence intensity developments reported in our paper.