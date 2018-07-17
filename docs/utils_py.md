
## CSV2PKLUnivSPy3

将csv转换为pkl格式

#### Tag:
* 通用模块

#### Param:
* None

#### Input:
* d_data1 (csv) 

#### Output:
* d_data2 (py3pkl) 

## DataDownloaderUnivSPy3

解析数据模块表示的资源引用，然后导入工作流。

#### Tag:
* 通用模块

#### Param:
* None

#### Input:
* data_source (datasource.file) 

#### Output:
* data (any) 

## DataInfoUnivSPy3

数据统计：数据类型，最大值，最小值，中位数

#### Tag:
* 通用模块

#### Param:
* None

#### Input:
* d_data (py3pkl) 

#### Output:
* o_data_type_null (html) 
* o_data_describe (html) 

## HDFSdownloaderUnivSPy3

从HDFS路径获取数据

#### Tag:
* 通用模块

#### Param:
* None

#### Input:
* o_path (any) 

#### Output:
* d_data (any) 

## HiveDownloaderUnivSPy3

从Hive对应数据库获取数据

#### Tag:
* 通用模块

#### Param:
* script (string) : 

#### Input:
* o_path (any) 

#### Output:
* d_data (csv) 

## JDBCdownloaderUnivSPy3

通过JDBC方式，访问数据库。

#### Tag:
* 通用模块

#### Param:
* jdbc_url (string) : 数据库JDBC连接串
* driver_jar (string) : 数据库驱动路径
* query (string) : SQL语句
* driver_name (string) : 驱动类名
* delimiter (string) : 数据的分隔符

#### Input:
* None

#### Output:
* output_file (any) 

## PKL2CSVUnivSPy3

将pkl转换为csv格式

#### Tag:
* 通用模块

#### Param:
* None

#### Input:
* d_data1 (py3pkl) 

#### Output:
* d_data2 (csv) 

## PKLfromStorage

从个人存储空间中读入PKL文件

#### Tag:
* 通用模块

#### Param:
* input_name (string) : 从个人存储空间读入文件名

#### Input:
* None

#### Output:
* o_pkl_file (py3pkl) 

## PKLtoStrorage

将PKL文件导入个人存储空间中

#### Tag:
* 通用模块

#### Param:
* output_name (string) : 填写输出文件的名字
* foldername (string) : 

#### Input:
* o_pkl_file (any) 

#### Output:
* None
