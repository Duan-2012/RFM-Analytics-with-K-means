# RFM-Analtics-with-K-means
Customers were grouped using the K-means method based on RFM scores.
 RFM + K-means 用户价值分析

## 技术栈
- Python 
- pandas（数据处理）
- numpy（数值计算）
- sklearn（K-means聚类）
- matplotlib（可视化）

## 数据说明
课程模拟数据：Individual Assignment Data File Electronic_sales，包含Age	Gender	Loyalty Member	Product Type	SKU	Rating	Order Status	Payment Method	Total Price	Unit Price	Quantity	Purchase Date	Shipping Type	Add-ons Purchased	Add-on Total等字段。

## 分析步骤
1. 数据预处理：处理缺失值和异常值
2. 计算 RFM 指标：R（最近消费时间）、F（消费频率）、M（消费金额）
3. 数据标准化：对 RFM 进行标准化
4. K-means 聚类：使用肘部法则确定聚类数 K=4
5. 用户画像分析：分析各群体特征并给出运营建议
6. 对比分类优势：K-means避免分值定义后分类的逻辑问题



text

## 运行方法
```bash
# 安装依赖
pip install pandas numpy scikit-learn matplotlib

# 运行代码
python RFM Analytics.ipynb


K-means客户购买行为分群结果：
Cluster	Number of Customer	Percentage %	R-Ori/Std	F-Ori/Std	M-Ori/Std
0	1475	15.58	64.13/-0.59	2.14/1.05	4115.32/-0.10
1	3067	32.40	248.17/1.16	1.05/-0.54	2842.70/-0.43
2	513	5.42	67.94/-0.76	3.30/2.75	12580.86/2.10
3	3226	34.08	83.16/-0.60	1.00/-0.61	2915.00/-0.41
4	1185	12.52	107.91/-0.33	1.80/0.56	10130.78/1.46

K-means客户取消行为分群结果：
Cluster	Number of Customer	Percentage %	R-Std	F-Std	M-Std
0	841	15.2	1.46	3.75	3.89
1	1326	24.0	3.05	1.53	3.891.68
2	1110	20.1	1.68	3.35	1.41
3	1211	21.9	4.22	2.36	1.82
4	1031	18.7	4.18	4.65	4.24


结论
1. 高频低价型客户：对价格敏感，易受促销和价格波动影响，购买频繁但单次消费金额低。  
2. 低频高价型客户：属理性消费，仅在特定需求时购买，非习惯性高频消费。  
3. “忠诚度”判断误区：仅凭购买频率或会员身份评估价值易失真，短期优惠吸引的客户未必贡献高利润。  
4. 大促期间的利润风险：频繁交易若未考虑成本与利润，可能因售后成本上升而侵蚀实际收益。
