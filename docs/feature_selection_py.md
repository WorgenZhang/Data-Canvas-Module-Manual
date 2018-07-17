
## CorrXXFeatSpy3

计算特征变量和特征变量之间的(pearson/spearman/kendall)相关性，并通过设定的参数来消除强相关的特征变量

#### Tag:
* 特征选择

#### Param:
* corr_type (string) : 
* corr_threshold (double) : 消除强相关时的阈值

#### Input:
* d_feature (csv) 
* o_featrue_label_corr (csv) 

#### Output:
* d_feature_selected (csv) 
* o_corr_XX (html) 
* o_corr_heatmap (jpg) 

## CorrXYFeatSPy3

计算特征变量和标签变量之间的相关性（卡方/互信息/F检验），并通过设定的参数来筛选相应的特征变量

#### Tag:
* 特征选择

#### Param:
* feature_percent (int) : 
* sample_rate (double) : 

#### Input:
* d_feature (py3pkl) 
* d_label (py3pkl) 

#### Output:
* d_feature_selected (csv) 
* o_feature_label_corr (csv) 

## RFEFeatSPy3

递归特征消除的主要思想是反复的构建模型（如SVM或者回归模型）然后选出最好的（或者最差的）的特征（可以根据系数来选），把选出来的特征放到一边，然后在剩余的特征上重复这个过程，直到所有特征都遍历了。

#### Tag:
* 特征选择

#### Param:
* percent_to_keep (double) : 保留变量个数百分比

#### Input:
* d_feature (csv) 
* d_label (csv) 

#### Output:
* d_changed_data (csv) 
* d_rfe_support (html) 
* rfe_cols (py3pkl) 

## VarianceThresholdFitFeatSPy3

根据方差去掉取值变化小的特征，用于训练集数据。

#### Tag:
* 特征选择

#### Param:
* None

#### Input:
* d_feature (py3pkl) 

#### Output:
* d_changed_data (py3pkl) 
* model (py3pkl) 

## VarianceThresholdTransformFeatSPy3

去掉取值变化小的特征，用于测试集数据。

#### Tag:
* 特征选择

#### Param:
* None

#### Input:
* model (py3pkl) 
* d_feature (py3pkl) 

#### Output:
* d_changed_data (py3pkl) 
