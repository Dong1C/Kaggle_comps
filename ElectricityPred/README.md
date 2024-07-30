# 1. 数据

`test.csv - columns: ['id', 'dt']`
`train.csv - columns: ['id', 'type', 'dt']`

任务： 通过train.csv中的时间序列倒着预测之前10个dt的target

## 方法1：[简单统计预测](main.ipynb)

- 使用简单的mean进行预测，可以得到378的评分
- 说明实际上前10个dt的数据相较于邻近的10个dt的数据实际上差距不大

## 方法2：lightgbm

### [baseline](lightbgm_version.ipynb)解读

- 使用[lightgbm](https://lightgbm.cn)训练梯度提升树，得到了259的评分
- 特征工程选择了
