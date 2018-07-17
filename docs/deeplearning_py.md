
## DataLoadMnistKeras

从指定路径加载划分为训练集和测试集的mnist数据，返回该路径。

#### Tag:
* 深度学习

#### Param:
* path (string) : 

#### Input:
* None

#### Output:
* mnist_path (txt) 

## DataPretreatmentMnistKeras

对数据集进行预处理，返回划分好的数据集和shape。

#### Tag:
* 深度学习

#### Param:
* img_rows (int) : 图像像素高度
* img_cols (int) : 	图像像素宽度
* num_classes (int) : 分类数目
* train_num (int) : 训练集数目
* test_num (int) : 

#### Input:
* path (txt) 

#### Output:
* x_train (csv) 
* y_train (csv) 
* x_train_shape (csv) 
* y_train_shape (csv) 
* x_test (csv) 
* y_test (csv) 
* x_test_shape (csv) 
* y_test_shape (csv) 

## imageclassifier_mxnet

基于mxnet框架的图像分类demo。

#### Tag:
* 深度学习

#### Param:
* model_name (string) : 

#### Input:
* image (jpg) 

#### Output:
* predict (txt) 

## keras_test

keras测试

#### Tag:
* 深度学习

#### Param:
* None

#### Input:
* data (csv) 

#### Output:
* image (pdf) 

## ModelEvaluateKeras

用测试集数据进行模型评估。

#### Tag:
* 深度学习

#### Param:
* mlServerAddr (string) : 
* modelName (string) : 
* EVALUATE_batch_size (string) : 
* EVALUATE_verbose (int) : 
* EVALUATE_sample_weight (string) : 

#### Input:
* model_trained (h5) 
* x_test (csv) 
* y_test (csv) 
* x_test_shape (csv) 
* y_test_shape (csv) 
* blockId (pkl) 

#### Output:
* model (model.h5) 

## ModelMnistKeras

利用keras搭建一个两层的卷积神经网络模型。

#### Tag:
* 深度学习

#### Param:
* img_rows (int) : 
* img_cols (int) : 
* num_classes (int) : 

#### Input:
* None

#### Output:
* model (h5) 
* model_json (json) 

## ModelStructShowKeras

利用model.summary打印模型概况。

#### Tag:
* 深度学习

#### Param:
* None

#### Input:
* model (h5) 

#### Output:
* model_struct (png) 

## ModelTrainKeras

进行模型训练，返回训练好的模型。

#### Tag:
* 深度学习

#### Param:
* COMPILE_optimizer (string) : 编译优化器
* COMPILE_loss (string) : 编译损失函数（目标函数）
* COMPILE_metrics (string) : 模型训练/测试的度量指标
* COMPILE_sample_weight_mode (string) : 样本权重类型(一维或多维)
* COMPILE_weighted_metrics (string) : metrics权重列表
* COMPILE_target_tensors (string) : 自定义目标张量
* FIT_epochs (int) : 训练轮数目
* FIT_verbose (int) : 训练过程日志显示
* FIT_batch_size (int) : 训练样本数量/批次
* FIT_callbacks (string) : 训练过程中回调函数集
* FIT_validation_split (double) : 从训练集抽取验证集比例
* FIT_validation_data (string) : 指定的验证集
* FIT_shuffle (int) : 是否在每训练轮次打乱样本顺序
* FIT_class_weight (string) : 训练样本类权重
* FIT_sample_weight (string) : 样本权重(依赖样本权重类型为temporal)
* FIT_initial_epoch (int) : 训练起始轮次（用于继续中断的训练）
* FIT_steps_per_epoch (string) : 每轮次训练包含的步数/批次
* FIT_validation_steps (string) : 处理验证集用的步数/批次（依赖训练步数/训练轮次）
* COMPILE_loss_weights (string) : 损失函数权重列表
* categorical_classes (int) : 

#### Input:
* model (h5) 
* x_train (csv) 
* y_train (csv) 
* x_train_shape (csv) 
* y_train_shape (csv) 

#### Output:
* model_trained (h5) 
* model_json (json) 
* blockId (pkl) 

## mxnet_test

基于mxnet框架，构建2层神经网络，实现前向传播和反向传播算法。

#### Tag:
* 深度学习

#### Param:
* lr (double) : 学习率
* num_epochs (int) : 迭代次数
* batch_size (int) : 梯度下降值

#### Input:
* data (csv) 

#### Output:
* out_1 (file) 

## pytorch_test

基于pytorch框架，构建2层神经网络，实现前向传播和反向传播算法。

#### Tag:
* 深度学习

#### Param:
* None

#### Input:
* data (csv) 

#### Output:
* result (txt) 

## tensorflow-test

基于tensorflow框架，构建、训练神经网络模型，并对模型进行预测。

#### Tag:
* 深度学习

#### Param:
* data_path (string) : 

#### Input:
* None

#### Output:
* None
