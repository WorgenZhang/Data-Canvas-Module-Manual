
## ClasEvalNewSPy3

对二分类及多分类模型进行评估（包括AUC，Kappa，评估报告及混淆矩阵等）

#### Tag:
* 模型评估
* 可视化

#### Param:
* None

#### Input:
* d_true (csv) 
* d_pred (csv) 
* d_prob (csv) 

#### Output:
* o_metric (csv) 
* o_classification_report (txt) 
* o_confusion_matrix (jpg) 

## ClasRocEvalSPy3a

输出分类模型的ROC曲线

#### Tag:
* 模型评估
* 可视化

#### Param:
* None

#### Input:
* d_feature (csv) 
* d_label (csv) 
* m_fitted_model (py3pkl) 

#### Output:
* o_roc_curve (jpg) 

## PlotLearningCurveSPy3_BestModel

画出学习曲线，根据训练集和测试集分数判断是否过拟合或欠拟合。

#### Tag:
* 模型评估
* 可视化

#### Param:
* n_jobs (int) : Number of jobs to run in parallel
* n_splits (int) : 交叉验证时使用折数
* test_size (double) : 验证集百分比

#### Input:
* d_feature (csv) 
* d_label (csv) 
* best_model (py3pkl) 

#### Output:
* learning_curve (jpg) 

## PlotLearningCurveSPy3

画出学习曲线，根据训练集和测试集分数判断是否过拟合或欠拟合。

#### Tag:
* 模型评估
* 可视化

#### Param:
* n_jobs (int) : Number of jobs to run in parallel
* n_splits (int) : 交叉验证时使用折数
* test_size (double) : 验证集百分比
* model (string) : 输入模型estimator, 例如GaussianNB()

#### Input:
* d_feature (csv) 
* d_label (csv) 

#### Output:
* learning_curve (jpg) 

## RegrEvalSPy3_Anaconda

对回归模型进行评估（包括mae,mse,r2等）

#### Tag:
* 模型评估

#### Param:
* multioutput (string) : 计分算法

#### Input:
* d_true (csv) 
* d_pred (csv) 

#### Output:
* o_metric (csv) 

## ReportPDFClasEvalSPy3

输出分类评估报告

#### Tag:
* 模型评估
* 可视化

#### Param:
* None

#### Input:
* o_metric (csv) 
* o_classification_report (txt) 
* o_confusion_matrix (jpg) 
* o_roc_curve (jpg) 
* o_metric_2 (csv) 
* o_classification_report_2 (txt) 
* o_confusion_matrix_2 (jpg) 
* o_roc_curve_2 (jpg) 

#### Output:
* evaluation_report (pdf) 

## ScoresSendSPy3

发送评估数据

#### Tag:
* 模型评估

#### Param:
* None

#### Input:
* Scores (csv) 
* model (any) 

#### Output:
* modelScores (py3pkl) 
