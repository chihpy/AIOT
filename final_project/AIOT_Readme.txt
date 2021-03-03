
--------------------------------------------
以下為 sample/py子目錄內部的檔案說明:

Windows 後端開發安裝的部分
  backFlaskServer.py ===> windows上開發後端Flask伺服器，用作給使用者查詢目前pi標註口罩預測結果的狀態，透過網頁的形式來呈現。
  backMongoServer.py ===> windows上開發後端MongoDB伺服器，每隔一段時間會自動的跟前端pi的mask_flask.py的預測結果傳輸api擷取資料。

PI前端開發口罩辨識預測的部分
  webcam_mask.py ===> 包含OpenCV擷取Webcam影像，之後載入Yolo訓練模型，依據影像預測影像內有沒有戴口罩的預測結果，框選結果後，儲存至成結果影像，並且將預測的結果儲存至mask_flask.py的預測結果API中。
  mask_flask.py  ===> 透過mask_flask.py可以提供目前在pi上面預測的結果影像，預測框選物件的座標，以及清除結果的API。
  
在google Colab裡面訓練Yolov4的時候，可以透過下載 mask_50.tar.gz 的檔案，來作為 yolo 的口罩訓練集資料，除了訓練影像資料集外，也已經包含一個訓練結果在mask_50/tiny_weights/yolov3-tiny_88000.weights內
---------------------------------------------

以下為 samply/inpyb的檔案內容，檔名即為相關的註解，主要是將 sample/py的子目錄內容的檔案，以及專題內訓練的環境，整理為google colab可以直接複製程式碼的版本

1.   「Mask口罩辨識」_AIOT_期末專題_Google_Colab訓練確定版.ipybb
2.    pi上面開發透過_webcam_辨識口罩(webcam_mask_py).ipynb
3.    pi上開發的_mask_flask_API.ipynb
4.    windows上開發_backFlaskServer_py.ipynb
5.    windows機器上開發一個mognodb_client，並且會每隔五秒連線pi_flask_API，抓取辨識的結果.ipynb