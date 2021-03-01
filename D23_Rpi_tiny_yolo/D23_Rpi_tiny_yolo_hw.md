# D23_Rpi_tiny_yolo
###### tags: `homework`
[TOC]
## 作業1 :
- 請思考使用 YOLO 和 tinyYOLO 進行訓練時，他們之間需要調整的差異在哪裡？
### sol:
- tiny_yolo_v3的output feature map只有2個(相較於yolo_v3的3個)
- 每層的anchor一樣是3個不過整體anchor數從9降到6
- pretrain要改
## 作業2 :
- 請思考當我們要訓練一個 7 個 class 的 tiny_yolo 時，要如何設定 cfg 檔？
### sol:
- num_class要改
- output層的number_of_filter應該是:num_anchor*(4+1+num_class)，以預設的darknet架構來說是3*(12)=36