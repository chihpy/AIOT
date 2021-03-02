# PIR_Sensor
###### tags: `RPi`
- 基礎介紹:
    - 靠近電磁波部分的遠紅外線，是一種熱能，任何物質都會輻射紅外線，例如溫水燭火等等，溫度不同波長也不一樣，人體在常溫下所釋放的紅外線波長約10微米
    - 靠近可見光部分的近紅外線，幾乎不會散發熱能，通常用於紅外線通訊、遙控和距離感測器
- 原理:
    - 凸透鏡裡面有一個焦電型感測器，焦電代表該元件會隨溫度變化產生電子訊號，感測器上的IC電路將會接收並處理感測器的訊號
    - 紅外線光難以穿透窗戶玻璃，但能穿透PE材質的塑膠
    - 被動式指出他不會發出偵測訊號，而是被動的接收紅外線源
- 外接線:
- ![](https://i.imgur.com/XGi2nUl.png)

    - 跳線方向向前，從跳線方向往回依序是
        - 接地
        - 訊號輸出
        - 5v電源
- 功能:
    - 平常輸出低電位
    - 偵測到人體移動輸出高電位(3.3v)
# 實作
- sensor的5v接pin2
- 資料線接pin26(gpio7)
- 接地接pin14
- pin11接led正
- ![](https://i.imgur.com/Oskhe0l.jpg)
- [code](https://github.com/chihpy/AIOT/blob/main/D15_RpiSensor/PIRSensor.py)
# reference
- [樹莓派Raspberry Pi之人體紅外線感測器實作](http://hophd.com/raspberry-pi-sensor-infrared/)