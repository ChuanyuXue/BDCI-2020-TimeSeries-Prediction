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

    catboost==0.24
    networkx==2.1
    numpy==1.18.5
    pandas==1.1.0
    scikit-learn==0.23.2
    tqdm==4.48.2
    python-louvain==0.14
    seaborn==0.10.1

## 声明

感谢 @supermanwasd 提供的代码运行环境，感谢UCONN - CSE5095 Machine Learning for Time Series Analysis 的Dongjin Song老师提供的论文阅读环节给予我启发。

本项目库专门存放KDD2020挑战赛的相关代码文件，所有代码仅供各位同学学习参考使用。如有任何对代码的问题请邮箱联系：cs_xcy@126.com

If you have any issue please feel free to contact me at cs_xcy@126.com

