## 文件结构：
```
  ├── model.py: ResNet模型搭建
  ├── train.py: 训练脚本
  ├── predict.py: 单张图像预测脚本
  └── batch_predict.py: 批量图像预测脚本
```
## 使用自定义数据集需要修改以下代码：
```
train.py:
-    29. dataset路径  
-    43. batch_size  
-    61. 引用的model (selected from resnet 18/34/50/101)  
-    64. 载入预训练模型  
-    73. dataset中类别个数  
-    83. epoch训练轮数  
-    85. 存放结果模型  
-    💡预训练模型可以从import torchvision.models.resnet，ctrl+B键进入获取下载链接。  

class_indices.json:
-    填入识别类别以及下标，格式为：{"0":"no pod","1":"pod"}  

predict.py:
-    22.img_path="./与predic.py同路径的测试图片名"  
-    42.weights_path="./与predic.py同路径的模型训练结果"  
```
