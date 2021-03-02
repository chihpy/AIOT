# D28_WebCam_yolo
###### tags: `homework`
[TOC]
## 作業1：
- 請思考並論述門禁系統的控制流程。
### sol:
- edge端:
    - 使用相機拍照
    - 使用yolo推論
    - 藉由flask將結果推送到WebAPI上
- PC端:
    - 使用request下載flaskWeb上的結果
    - 使用request下載flaskWeb上的圖片
    - 將圖片和結果存在mongoDB中
## 作業2：
- 請思考資料 (影像) 在門禁系統流程的各個階段如何被處理與呈現？
### sol:
- 在edge端拍照
- 在edge端inference
- edge端推送到WebAPI
- PC端藉由WebAPI下載
- PC端將圖片存到MongoDB
