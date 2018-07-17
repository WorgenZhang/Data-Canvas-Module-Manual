
## ClasPredictSPy3

通过已训练好的模型进行预测

#### Tag:
* 模型预测

#### Param:
* None

#### Input:
* d_feature (csv) 
* m_fitted_model (py3pkl) 

#### Output:
* d_predict (csv) 
* d_pred (csv) 
* d_prob (csv) 

## LogisticPredSPy3

使用训练好的逻辑回归模型进行预测 (在原有预测数据上要先添加截距)

#### Tag:
* 模型预测

#### Param:
* None

#### Input:
* d_data1 (csv) 
* cols (py3pkl) 
* m_fitted_model (py3pkl) 

#### Output:
* d_pred (csv) 
* d_prob (csv) 
* d_feature (csv) 

## StackingPredictSPy3

根据训练好的Stacking模型对数据进行预测

#### Tag:
* 模型预测

#### Param:
* None

#### Input:
* d_feature (csv) 
* m_fitted_model (py3pkl) 

#### Output:
* d_predict (csv) 
* d_pred (csv) 
* d_prob (csv) 
