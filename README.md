# BDCI-2020-TimeSeries-Prediction
Matrix Factorization for High-Dimensional and Sparse Time Series Prediction

2020-BDCI，滴滴交通堵塞预测赛道 复赛第12名解决方案

This repository contains the 12th solution on BDCI 2020 Challenges for Congestion Prediction Prediction.

赛题链接：https://www.datafountain.cn/competitions/466

解决方案blog: 

## 解决方案

1. 如下面文件结构所示，我们首先在 1_data_formating.ipynb 中把比赛方提供的txt数据转化为更容易处理的csv格式。
2. 2_matrix_generation.ipynb 文件把数据中出现过的所有时间点的状态放到一个(32 x 15584 x 720)的矩阵中。
3. 3_matrix_factorization.ipynb 采用交替最小二乘法把矩阵分解为一个道路隐含因子矩阵与一个时间隐含因子矩阵，并采用周期因子法预测未来的时间隐含因子。
4. 4_feature_engineering.ipynb 在原始数据中进行统计性特征描述，弥补矩阵分解中造成的信息损失。
5. 5_Implicit_feedback.ipynb 将第3步提取的隐含因子以及第4步提取的统计性描述一起使用catboost建模，还原待预测时间段的路况堵塞状态。


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

