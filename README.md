# 0 overview
###### tags: `AIOT`
[TOC]
# AIOT物聯網與感測裝置介紹
## D01 AIOT人工智慧物聯網介紹
## D02 感測器介紹
## D03 感測器傳輸介面
## D04 感測器應用層傳輸模式
## D05 感測器資料自動蒐集
# 雲端軟體管理與大數據資料庫程式開發
## D06 SQL&NOSQL資料庫介紹
## D07 Docker軟體容器平台介紹與安裝使用
- 基本的docker使用
- [x] [study](https://github.com/chihpy/AIOT/blob/main/D07_docker/D07%20Docker.md)
- [x] [homework](https://github.com/chihpy/AIOT/blob/main/D07_docker/D07_Docker_hw.md)
## D08 MonogoDB大數據資料庫介紹與安裝實作
- 基本的MonogoDB使用
- [x] [study](https://github.com/chihpy/AIOT/blob/main/D08_MongoDB/D08_MongoDB.md)
- [x] [homework](https://github.com/chihpy/AIOT/blob/main/D08_MongoDB/D08_MongoDB_hw.md) 
## D09 Python存取MongoDB常用指令與程式教學
- pymongo增刪改查
- [x] [study](https://github.com/chihpy/AIOT/blob/main/D09_pymongo/D09%20pymongo.md)
- [x] [homework](https://github.com/chihpy/AIOT/blob/main/D09_pymongo/D09%20pymongo_hw.md)
## D10 RaspberryPi OS系統管理與操作
- 開箱樹梅派
- ssh、vnc設定
- [x] [study](https://github.com/chihpy/AIOT/blob/main/D10_RaspbarryPi/D10%20Raspberry%20Pi.md)
- [x] [homework](https://github.com/chihpy/AIOT/blob/main/D10_RaspbarryPi/D10%20Raspberry%20Pi_hw.md)
## D11 Linux常用指令教學
- linux的基礎指令
- [x] [study](https://github.com/chihpy/AIOT/blob/main/D11_Linux_command/D11%20Linux%20command.md)
- [x] [homework](https://github.com/chihpy/AIOT/blob/main/D11_Linux_command/D11%20Linux%20command_hw.md)
## D12 RaspberryPi之接腳介紹與GPIO教學
- 啟動、關閉GPIO接腳
- 啟動、關閉I2C、SPI
- `/sys/kernel/debug/gpio`
- 使用sysfs點亮LED燈
- [x] [study](https://github.com/chihpy/AIOT/blob/main/D12_Rpi_GPIO/D12%20Rpi%20GPIO.md)
- [x] [homework](https://github.com/chihpy/AIOT/blob/main/D12_Rpi_GPIO/D12%20Rpi%20GPIO_hw.md)
## D13 使用python控制GPIO接腳
- remote vscode
- python點亮LED燈
- python控制LED明暗
- python按鈕控制LED
- [x] [sutdy](https://github.com/chihpy/AIOT/blob/main/D13_python_gpio/D13%20python%20GPIO.md)
- [x] [homework](https://github.com/chihpy/AIOT/blob/main/D13_python_gpio/D13%20python%20GPIO_hw.md)
## D14 使用Python進行WebCam視訊擷取與輸出
- command拍照
- fswebcam
- [x] [study](https://github.com/chihpy/AIOT/blob/main/D14_RpiWebCam/D14%20RpiWebCam.md)
- [x] [homework](https://github.com/chihpy/AIOT/blob/main/D14_RpiWebCam/D14%20RpiWebCam_hw.md)
## D15 使用Python控制DHT22感測器與繼電器
- [ ] 使用人體紅外線感測器
- [x] [study](https://github.com/chihpy/AIOT/blob/main/D15_RpiSensor/D15_RpiSensor.md)
- [x] [homework](https://github.com/chihpy/AIOT/blob/main/D15_RpiSensor/D15_RpiSensor_hw.md)
# 物聯網網頁後端程式開發
## D16 使用Docker架設Flask Web Server
- 用flask寫一個hello world
- 寫一個dockerfile有flask和python環境
- [x] [study](https://github.com/chihpy/AIOT/blob/main/D16_Flask_docker/D16_Flask_and_Docker.md)
- [x] [homework](https://github.com/chihpy/AIOT/tree/main/D16_Flask_docker/file)
## D17 使用Python開發Flask網頁程式
- [ ] http的八種方法
- [ ] 回傳HTML的畫面
- [ ] 一個上傳的按鈕和顯示HTML
- [x] [study](https://github.com/chihpy/AIOT/blob/main/D17_Flask/D17_Flask.md)
- [x] [homework](https://github.com/chihpy/AIOT/blob/main/D17_Flask/D17_Flask_hw.md)
## D18 撰寫Flask Web程式存取MongoDB
- 由flask存取mongo進行增刪改查
- [x] [study](https://github.com/chihpy/AIOT/blob/main/D18_flask-pymongo/D18%20Flask-PyMongo.md)
- [x] [homework](https://github.com/chihpy/AIOT/blob/main/D18_flask-pymongo/D18%20Flask-PyMongo_hw.md)
## D19 在Raspberry Pi上安裝Flask Web Server
- 由flask Web Server控制LED燈
- [x] [study](https://github.com/chihpy/AIOT/blob/main/D19_Flask_Rpi/D19_Flask_Rpi.md)
- [x] [homework](https://github.com/chihpy/AIOT/blob/main/D19_Flask_Rpi/D19_Flask_Rpi_hw.md)
# Pre-trained模型訓練資料方法-使用LabelImg與yolo影像辨識技術
## D20 YOLO目標檢測框架介紹
## D21 使用yolov3訓練人臉識別
## D22 在Raspberry Pi上使用YOLO已訓練好的模型
## D23 在樹梅派上佈署與使用YOLOv3-tiny
## D24 使用YOLO訓練如何辨識橘子
# 樹梅派連結MongoDB整合前後端
## D25 透過Flask將訊息從樹梅派傳送給PC
## D26 將RaspberryPi的YOLO資料集預測結果傳送至PC
## D27 設計一個影像與辨識結果的資料庫
## D28 使用Webcam 拍照並以YOLO辨識資料庫儲存的結果
# 期末專題
## D29 支援口罩辨識的智慧門禁系統
## D30 Line Chat API即時通知系統