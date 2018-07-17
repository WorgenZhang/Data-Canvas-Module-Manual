
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

## FormShowCSVUnivSPy3



#### Tag:
* 可视化

#### Param:
* None

#### Input:
* d_data (csv) 

#### Output:
* d_form (html) 

## FormShowUnivSPy3

数据显示

#### Tag:
* 可视化

#### Param:
* None

#### Input:
* d_data (py3pkl) 

#### Output:
* d_form (html) 

## KMeansVisuSPy3

聚类中心雷达图和肘部图

#### Tag:
* 聚类模型
* 可视化

#### Param:
* None

#### Input:
* o_centers (py3pkl) 
* o_distortions (py3pkl) 

#### Output:
* distortion_plot (html) 
* centers_plot (html) 

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

## WOE_IV_DataSPy3

IV的全称是Information Value，中文意思是信息价值，或者信息量。我们需要一些具体的量化指标来衡量每个自变量的预测能力，并根据这些量化指标的大小，来确定哪些变量进入模型。IV就是这样一种指标，他可以用来衡量自变量的预测能力。类似的指标还有信息增益、基尼系数等等。高IV表示该特征和目标变量的关联度高；目标变量只能是二分类；特征分箱越细，IV越高。

WOE的全称是“Weight of Evidence”，即证据权重。WOE是对原始自变量的一种编码形式。WOE表示的实际上是“当前分组中响应客户占所有响应客户的比例”和“当前分组中没有响应的客户占所有没有响应的客户的比例”的差异。

#### Tag:
* 可视化
* 数据预处理

#### Param:
* label (string) : 标签变量

#### Input:
* d_data1 (py3pkl) 
* o_all_var (py3pkl) 

#### Output:
* o_IV_bar_plot (jpg) 
* o_WOE_corr_plot (jpg) 
* o_vars_after_corr (txt) 
* o_vars_after_VIF (txt) 
* d_data2 (py3pkl) 
* o_vars_after_VIF_pkl (py3pkl) 
