## KBQA_medical
### 基于知识图谱的医疗问答系统
#### 1、构建知识图谱。
自定义Schama层，从JSON文件中抽取实体，并定义实体之间的关系类型，存储在Neo4j中
#### 2、利用BILSTM-CRF进行命名实体识别。
识别用户问题中的实体
#### 3、利用CasRel模型进行关系抽取。
获取用户问题中实体之间的关系，这里的关系应是Schama中定义好的关系
#### 4、利用BM25+esim进行实体规范化。
使用户问题中的实体与知识图谱中的实体相对应
#### 5、利用BERT+textCNN进行意图识别和槽位填充。
明确用户问题的意图，如用户的意图是问症状还是问药物；根据识别出用户问题中的实体、关系等信息，填充语义槽
#### 6、效果展示。
![image](https://user-images.githubusercontent.com/74800719/235571039-e6ead034-7e0a-4040-841c-5d7c36cbeafb.png)


#### 注：该项目是根据B站UP主[每天都要机器学习](https://space.bilibili.com/106467161)的视频进行学习的。
#### 参考链接：
https://github.com/wangle1218/KBQA-for-Diagnosis
<br/>
https://github.com/liuhuanyong/QASystemOnMedicalKG
