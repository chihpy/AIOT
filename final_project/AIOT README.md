# AIOT README
###### tags: `project`
# 流程
1. training data
2. data preprocessing
3. train model
4. inference model test
5. flask web on pi
6. yolo opencvDNN inference to flask
7. flask web to mongodb
8. assert mongodb
9. flask web server show result
## 1_training_data
- 說明: 想辦法取得任務data
    - 這邊使用[fddb](http://vis-www.cs.umass.edu/fddb/)訓練基本的人臉檢測model
    - [demo video: yolo_face_detection](https://youtu.be/a82ucVpd3Bo)
## 2_data_preprocessing
- 說明: 清理data成需要的格式
    - 清理任務寫成sh讓復現變得容易
    - 打包成一個zip傳到drive，由colab mount近來
- data cleaning
    - [build_fddb.sh](https://github.com/chihpy/AIOT/blob/main/final_project/colab/clean/build_fddb.sh)
        - fddb2darknet.py
        - build_fddb會執行fddb2darknet.py把資料轉成darknet需要的格式
## 3_train_model
- [colab_train](https://github.com/chihpy/AIOT/blob/main/final_project/colab/train/tiny_v3_fddb_long.ipynb)
    - 由於12小時斷連一次，所以在訓練一定步數就把參數存到drive裡
## 4_model_evaluation_test
- [demo code: yolo_inference_imshow.py](https://github.com/chihpy/AIOT/blob/main/final_project/Pi/yolo_inference_imshow.py)
    - [demo video: yolo person detection](https://youtu.be/Sf4ilZJCtQ4)
- [ ] 把mAP講清楚
## 5_flaskWeb_on_Pi
- 說明: 將Pi上的資料丟到Web上
    - [pi_flask.py](https://github.com/chihpy/AIOT/blob/main/final_project/Pi/pi_flask.py)
- 主要功能:
    - postLabel: 給pi的辨識程式上傳資料
    - list: 回傳目前postLabel上傳在pi上的辨識結果資料
    - clear: 將pi上儲存的辨識結果清空
    - clearImg: 將pi上儲存的影像資料清空
    - img: 依據傳入的file參數，回傳某個影像資料
## 6_yolo_inference_to_flask
- 說明: 開啟Pi上的相機，如果有偵測到物件，就儲存辨識結果((dictionary)、原始圖片)並更新到Web
    - [webcam_yolo.py](https://github.com/chihpy/AIOT/blob/main/final_project/Pi/webcam_yolo.py)
    - RPi上的畫面:
    - ![](https://i.imgur.com/p0IgaTU.jpg)

## 7_flaskweb_to_mongodb
- 說明: 在PC端自動去pi_flask_web_server抓取最新的辨識結果，之後將結果存到mongodb
- [backMongoServer,py](https://github.com/chihpy/AIOT/blob/main/final_project/PC/backMongoServer.py)
- note: 要先把mongoDB的docker跑起來
- 每隔t秒就會自動去Web把樹梅派上的資料抓下來、清空樹梅派上的資料、把資料存到PC端的資料庫
## 8_assert_mongoDB
- 在mongo shell檢查資料
    - `docker exec -it mongo1 mongo`
    - `use yolo_pred_db`
    - `show collections`
    - `db.test_coll.count()`
    - `db.test_coll.find({label:'face'}).count()`
    - windows執行的畫面:
    - ![](https://i.imgur.com/z6NFIpY.png)

## 9_show_mongoDB
- 在PC端把本地mongoDB上的資料顯示出來
    - [showdb.py](https://github.com/chihpy/AIOT/blob/main/final_project/PC/FlaskServer.py)
- ![](https://i.imgur.com/rZFtZg3.png)
