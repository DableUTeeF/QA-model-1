
#### 任务下的结构基本一致
* config：放置每个具体任务的配置文件，包括训练参数，数据路径，模型存储路径
* data_helper.py：数据预处理文件
* metrics.py：性能指标文件
* model.py：模型文件，可以很容易的实现bert和下游网络层的结合
* trainer.py：训练模型
* predict.py：预测代码，只需要实例化Predictor类，调用predict方法就可以预测

#### 训练数据格式

* context：抽取式阅读理解的上下文
* question：问题
* answer：答案，从context中抽取一个片段
* start_position: answer的起始位置
* end_position: answer的终止位置

#### 训练模型
* 执行每个任务下的sh脚本即可，sh run.sh。只需要更改配置文件就可以训练不同的模型

#### 预测
* 执行bert_task中每个任务下的test.py文件就可以预测。
