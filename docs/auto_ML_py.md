
## ML_BinaryClassModelEval_churn

自动建模 - 二分类评估模块

#### Tag:
* 自动建模

#### Param:
* None

#### Input:
* blockId (py3pkl) 
* model (model.pkl) 
* X_test (csv) 
* y_test (csv) 

#### Output:
* modelScores (txt) 

## ML_BinaryClassModelEval

自动建模 - 二分类评估模块

#### Tag:
* 自动建模

#### Param:
* None

#### Input:
* model (model.pkl) 
* X_test (csv) 
* y_test (csv) 

#### Output:
* modelScores (py3pkl) 

## ML_CategoryFeatureHandle

自动建模-类别特征处理

#### Tag:
* 自动建模

#### Param:
* cols (string) : 类别列名，多列用逗号分割
* handling (string) : 特征处理策略
* targetCol (string) : 目标列，仅支持一列

#### Input:
* sampleData (csv) 

#### Output:
* categoryFeatureHandleData (csv) 

## ML_HyperparamsCV

自动建模
超参数调优模块

#### Tag:
* 自动建模

#### Param:
* hyperparams (string) : 超参数配置
* param_dist (string) : 算法参数信息
* evalStr (string) : 算法名称

#### Input:
* X_train (csv) 
* y_train (csv) 

#### Output:
* model (model.pkl) 
* blockId (py3pkl) 

## ML_MultiClassModelEval

自动建模 - 多分类评估模块

#### Tag:
* 自动建模

#### Param:
* None

#### Input:
* model (model.pkl) 
* X_test (csv) 
* y_test (csv) 

#### Output:
* modelScores (py3pkl) 

## ML_NumFeatureHandle

自动建模-数值特征处理

#### Tag:
* 自动建模

#### Param:
* targetCol (string) : 目标列
* cols (string) : 数值列，多列使用逗号分割
* handling (string) : 数值特征处理策略
* rescaling (string) : handling为ASREGULARFEATURE必填
* binarizeThreshold (string) : handling为BINARIZETHRESHOLD必填
* constantValue (double) : 固定值，binarizeThreshold为CONSTANT必填
* quantizeNum (int) : handling为QUANTIZE必填

#### Input:
* sampleData (csv) 

#### Output:
* numFeatureHandleData (csv) 

## ML_PreHandle

自动建模-特征工程-数据预处理

#### Tag:
* 自动建模

#### Param:
* cols (string) : 列名，多列用逗号分割
* variableType (string) : 列的类型
* handling (string) : 缺失值处理策略
ASREGULAR - 作为常规值
IMPUTE - 填充
DROPROWS - 删除该行
* impute (string) : 缺失值填充策略
MOSTFREQUENT-众数,
MEAN-平均数
MEDIAN-中位数
CONSTANT-固定值
* constantValue (string) : 缺失值填充固定值
* targetCol (string) : 目标列

#### Input:
* originalData (csv) 

#### Output:
* handleData (csv) 

## ML_RegModelEval

自动建模 - 回归模型评估

#### Tag:
* 自动建模

#### Param:
* None

#### Input:
* model (model.pkl) 
* X_test (csv) 
* y_test (csv) 

#### Output:
* modelScores (py3pkl) 

## ML_SampleData

自动建模 - 数据采样

#### Tag:
* 自动建模

#### Param:
* method (string) : 采样方法
* recordsNum (int) : 采样行数
* recordsRatio (double) : 采样比例
* column (string) : 保持类平衡采样的特征列
* cols (string) : 要采样的列，多列使用逗号分割

#### Input:
* handleData (csv) 

#### Output:
* sampleData (csv) 

## Ml_SplitSet

自动建模-数据拆分

#### Tag:
* 自动建模

#### Param:
* targetCol (string) : 目标列
* split (string) : 拆分策略
* kFoldCrossTest (string) : 是否启用K-折交叉
* foldNum (int) : K-折，kFoldCrossTest=True
* trainRatio (double) : 训练集的样本比例，kFoldCrossTest=FALSE

#### Input:
* featureHandleData (csv) 

#### Output:
* X_train (csv) 
* y_train (csv) 
* X_test (csv) 
* y_test (csv) 

## TPOTSPy3

基于Python的自动式机器学习工具，使用基因算法优化机器学习管道。

#### Tag:
* 自动建模

#### Param:
* split_radio (double) : 训练数据分割比
* generations (int) : 对运行管道优化过程的迭代次数
* population_size (int) : 每次迭代个体保留数目
* tpop_mode (string) : 确实模型是监督分类或回归问题
* cv (int) : 在评估管道时使用的交叉验证策略
* verbosity (int) : TPOT显示信息等级
* scoring (string) : 模型评估选择指标
* n_jobs (int) : 在TPOT优化过程中，并行用于评估管道的过程的数量

#### Input:
* in_1 (csv) 

#### Output:
* out_1 (file) 
