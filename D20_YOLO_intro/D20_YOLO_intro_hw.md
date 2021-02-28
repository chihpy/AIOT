# D20_YOLO_intro
###### tags: `homework`
[TOC]
## 作業1
- 請參考 「 什麼是物件偵測？ 」頁的內容，思考 YOLO 是如何找出貓咪的位置以及類別的。
### sol:
- 將output切成grid:
- 假設yolo對某張圖的output_shape是(20x20x5*(4+1+2))，number_of_anchor是5, number_of_class是2，grid_size是20x20
- 對每個anchor，yolo都給出一個confidence，如果confidence*貓的class分數大過一個給定的threshold就會輸出預測框，同類的預測框們經過NMS最後留下的就是yolo的output