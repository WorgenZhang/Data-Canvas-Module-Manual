
## ChangeTypeDataSPy3

转换数据类型

#### Tag:
* 数据操作

#### Param:
* cols (string) : 选择需要转换类型的变量
* type (string) : 转换后的变量类型
* cols1 (string) : 选择要剔除的变量，其余变量全部做类型转换

#### Input:
* d_data (py3pkl) 

#### Output:
* d_changed_data (py3pkl) 

## ColsDropDataSPy3

删除指定列

#### Tag:
* 数据操作

#### Param:
* cols (string) : 

#### Input:
* d_data (py3pkl) 

#### Output:
* d_changed_data (py3pkl) 

## ColsSelect2DataSPy3



#### Tag:
* 数据操作

#### Param:
* None

#### Input:
* d_data (py3pkl) 
* selected_cols (py3pkl) 

#### Output:
* d_selected_data (csv) 

## ColsSelectCSVDataSPy3

选择需要的变量，并以CSV形式输出

#### Tag:
* 数据操作

#### Param:
* cols (string) : 

#### Input:
* d_data (csv) 

#### Output:
* d_selected_data (csv) 

## ColsSelectDataSPy3

选择需要的变量

#### Tag:
* 数据操作

#### Param:
* cols (string) : 

#### Input:
* d_data (py3pkl) 

#### Output:
* d_selected_data (py3pkl) 

## ConcatDataSPy3

合并两个数据集

#### Tag:
* 数据操作

#### Param:
* None

#### Input:
* d_data1 (csv) 
* d_data2 (csv) 

#### Output:
* d_data (csv) 

## Date2DaysDataSPy3

将日期转换为天数(可以是两个日期间距离的天数也可以是一个日期距今的天数)

#### Tag:
* 数据操作

#### Param:
* var1 (string) : var1 - var2
* var2 (string) : var1 - var2
* whether_use_2_variables (int) : 是否使用两个日期变量，如果否，则只使用var1，计算var1距当前时间天数
* new_var (string) : 新生成变量的变量名

#### Input:
* d_data1 (py3pkl) 

#### Output:
* d_data2 (py3pkl) 

## DateParsingDataSPy3

解析日期型变量，生成四个新变量：月、日、一周的第几天、是否为周末

#### Tag:
* 数据操作

#### Param:
* cols (string) : 选择要构建衍生变量的日期
* format (string) : 指定日期变量的格式

#### Input:
* d_data1 (py3pkl) 

#### Output:
* d_changed_data (py3pkl) 

## DropDuplicatesDataSPy3

根据指定变量去掉重复行

#### Tag:
* 数据操作

#### Param:
* col (string) : 指定变量
* method (string) : 选择去重方法

#### Input:
* d_data1 (csv) 

#### Output:
* d_changed_data (csv) 

## FillNADataSPy3

将指定变量的缺失值填补为0

#### Tag:
* 数据操作

#### Param:
* cols (string) : 

#### Input:
* d_data (py3pkl) 

#### Output:
* d_changed_data (py3pkl) 

## MapLambdaDataSPy3

对数据使用map函数从而进行特征的清洗

#### Tag:
* 数据操作

#### Param:
* script (string) : map函数中的语句
* var (string) : 选择清洗的变量

#### Input:
* d_data1 (py3pkl) 

#### Output:
* d_data2 (py3pkl) 

## MappingDataSPy3

类别字段映射

#### Tag:
* 数据操作

#### Param:
* cols (string) : 选择要映射的字段

#### Input:
* d_data1 (py3pkl) 

#### Output:
* d_changed_data (py3pkl) 

## MergeDataSPy3

根据主键对数据进行合并操作

#### Tag:
* 数据操作

#### Param:
* key (string) : 定义主键变量
* method (string) : 选择合并方式

#### Input:
* d_data1 (csv) 
* d_data2 (csv) 

#### Output:
* d_changed_data (csv) 

## ReplaceDataSPy3

将数据中的某个值全部替换为另一个值

#### Tag:
* 数据操作

#### Param:
* value_after (string) : 替换后的值
* value_before1 (string) : 
* value_before2 (string) : 替换前的值

#### Input:
* d_data1 (py3pkl) 

#### Output:
* d_data2 (py3pkl) 

## SplitFeatSPy3

将特征数据集和标签数据集拆分为训练集（特征、标签），测试集（特征、标签）。

#### Tag:
* 数据操作

#### Param:
* test_size (double) : 测试集比例

#### Input:
* d_feature (csv) 
* d_label (csv) 

#### Output:
* d_feature_train (csv) 
* d_feature_test (csv) 
* d_label_train (csv) 
* d_label_test (csv) 
