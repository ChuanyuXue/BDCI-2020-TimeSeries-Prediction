# BDCI-2020-TimeSeries-Prediction
Matrix Factorization for High-Dimensional and Sparse Time Series Prediction

2020-BDCI，滴滴交通堵塞预测赛道 复赛第12名解决方案

This repository contains the 12th solution on BDCI 2020 Challenges for Congestion Prediction Prediction.

赛题链接：https://www.datafountain.cn/competitions/466

解决方案blog: 

## 解决方案

## 文件结构

    │  1_data_formating.ipynb                       ## Loading the txt files into the structured csv files
    │  2_matrix_generation.ipynb                    ## Generating the time series matrix Y from the csv files 
    │  3_matrix_factorization.ipynb                 ## Learning the latent factors P & Q from the matrix Y
    │  4_feature_engineering.ipynb                  ## Extracting other features from the time series matrix Y
    │  5_Implicit_feedback.ipynb                    ## Modeling the latent factors for implicit feedback
    │  LICENSE
    │  README.md
    │  structure.txt
    │  
    └─data                                          ## Containing origin data and intermedidate files
        └─traffic
        
        
## Python库坏境依赖

## 声明


