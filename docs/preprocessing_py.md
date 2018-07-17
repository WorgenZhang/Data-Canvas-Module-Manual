
## ChiMergeDataSPy3

卡方分箱法：自低向上的(即基于合并的)数据离散化方法。它依赖于卡方检验：具有最小卡方值的相邻区间合并在一起，直到满足确定的停止准则。
基本思想：对于精确的离散化，相对类频率在一个区间内应当完全一致。因此，如果两个相邻的区间具有非常类似的类分布，则这两个区间可以合并；否则，它们应当保持分开。而低卡方值表明它们具有相似的类分布。

#### Tag:
* 数据预处理

#### Param:
* label (string) : 定义标签变量

#### Input:
* d_data1 (py3pkl) 

#### Output:
* d_data2 (py3pkl) 
* all_var (py3pkl) 

## DummyFitDataSPy3

对数据做哑编码转化(训练数据时使用)

#### Tag:
* 数据预处理

#### Param:
* None

#### Input:
* d_data (py3pkl) 

#### Output:
* d_dummy_data (py3pkl) 
* cols (py3pkl) 

## DummyTransformDataSPy3

对数据做哑编码转化(将数据转化为同训练数据相同的变量)

#### Tag:
* 数据预处理

#### Param:
* None

#### Input:
* d_data (py3pkl) 
* cols (py3pkl) 

#### Output:
* d_dummy_data (py3pkl) 

## ImbalanceDataSPy3

对数据进行过采样处理

#### Tag:
* 数据预处理

#### Param:
* None

#### Input:
* X (csv) 
* Y (csv) 

#### Output:
* x_resampled (csv) 
* y_resampled (csv) 

## LabelEncoderDataSPy3

对类别型文本变量进行编码

#### Tag:
* 数据预处理

#### Param:
* col (string) : 数据中需要更改成虚拟变量的原列
* signal (int) : 选择是否按照数据类型自动转换

#### Input:
* d_data (py3pkl) 

#### Output:
* d_changed_data (py3pkl) 

## MinMaxScalerFitDataSPy3

对连续型变量进行归一化处理, 使用这种缩放的目的包括实现特征极小方差的鲁棒性以及在稀疏矩阵中保留零元素。适用于训练数据。

#### Tag:
* 数据预处理

#### Param:
* None

#### Input:
* d_data (py3pkl) 

#### Output:
* d_changed_data (py3pkl) 
* m_minmax_model (py3pkl) 

## MinMaxScalerTransformDataSPy3

对连续型变量进行归一化处理, 使用这种缩放的目的包括实现特征极小方差的鲁棒性以及在稀疏矩阵中保留零元素。适用于测试数据。

#### Tag:
* 数据预处理

#### Param:
* None

#### Input:
* d_data (py3pkl) 
* model (py3pkl) 

#### Output:
* d_changed_data (py3pkl) 

## MissingDropDataSPy3

删除拥有唯一值的字段；删除缺失百分比大于一定比率的字段(类别变量大于30%，连续变量大于60%)。

#### Tag:
* 数据预处理

#### Param:
* percent_obj (int) : 
* percent_non_obj (int) : 
* percent_unique (double) : 

#### Input:
* d_data (py3pkl) 

#### Output:
* d_changed_data (py3pkl) 

## MissingFillDataSPy3

小比例缺失值用众数或中位数填充。


#### Tag:
* 数据预处理

#### Param:
* percent_obj (int) : 
* percent_non_obj (int) : 

#### Input:
* d_data (py3pkl) 

#### Output:
* d_changed_data (py3pkl) 

## MissingImputeDataSPy3

用传播算法对缺失值进行填充

#### Tag:
* 数据预处理

#### Param:
* lower_null_percent_object (int) : 
* upper_null_percent_object (int) : 
* lower_null_percent_nonobject (int) : 
* upper_null_percent_nonobject (int) : 

#### Input:
* d_data (py3pkl) 

#### Output:
* d_changed_data (py3pkl) 

## OneHotEncoderDataSPy3

将数据转化为虚拟数据，即将数据拆分为多个以0或1表示的列

#### Tag:
* 数据预处理

#### Param:
* None

#### Input:
* d_data (py3pkl) 

#### Output:
* d_changed_data (py3pkl) 

## QuantileTrasformerDataSPy3

分位数转换的目的是把特征数据转换到一定的范围内, 或者让他们符合一定的分布。分位数转换利用的是数据的分位数信息进行变换。
它能够平滑那些异常分布，对于存在异常点的数据也很适合。但是它会破话原来数据的相关性和距离信息

#### Tag:
* 数据预处理

#### Param:
* n_quantiles (int) : 计算所用的分位数，默认值为1000
* output_distribution (string) : 换数据遵循的分布函数，默认值为uniform
* ignore_implicit_zeros (string) : 只针对稀疏矩阵，默认值为False，当为True时，则在计算分位数时稀疏矩阵中的稀疏条目将被忽略
* subsample (int) : 用于计算有效分为数的最大样本数，默认值为100000
* copy (string) : 

#### Input:
* d_data (py3pkl) 

#### Output:
* d_changed_data (py3pkl) 
* transformer (py3pkl) 

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
