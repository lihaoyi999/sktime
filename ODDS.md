# MATCH ODDS

## 数据字段信息
```
match_id, company_id, win, draw, lost,
draw-win, lost-draw, draw-win/lost-draw,
label1, label2, label3, label4,label5,label6
```
### 多分类
label1: 3, 1, 0  主队胜、平、负   

### 二分类
label2: 3and1, 0  主队不败、主队败  
label3: 3, 1and0  主队胜、主队不胜  
label4: 3and0, 1  分出胜负、打平    
label5: big, small  大球、小球  
label6: 0, 1  是否爆冷  

## 时间序列分类算法
### 单变量时间序列分类算法   

#### 整个时间序列的相似性
1. DTW：Dynamic time warping
1. WDTW：Weighted DTW
1. TWE：Time warp edit
1. MSM：Move–split–merge
1. CID：Complexity invariant distance 
1. $DD_{DTW}$：Derivative DTW
1. $DTD_{C}$：Derivative transform distance
1. EE：Elastic ensemble 

#### 相位相关间隔
1. TSF：Time series forest
1. TSBF：Time series bag of features
1. LPS：Learned pattern similarity

#### 相位无关形状
1. FS：Fast shapelets
1. ST：Shapelet transform
1. LS：Learned shapelets

#### 基于字典的分类器
1. BOP：Bag of patterns  
1. SAXVSM：Symbolic aggregate approximation-vector space model
1. BOSS：bag of SFA symbols

#### 变换组合
1. $DTW_F$：DTW features
1. COTE：Collection of transformation ensembles

#### 各个算法的时间和空间复杂性



### 多变量时间序列分类算法  
应用多变量时间序列的定制分类算法。

1. 将多变量时间序列按列合并成长的单变量时间序列，训练单变量时间序列分类模型  
1. 对多变量时间序列的每一列训练一个单变量时间序列模型，聚合每个模型的分类结果作为最终的分类结果。