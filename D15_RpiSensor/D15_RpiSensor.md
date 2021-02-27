# D15_RpiSensor
###### tags: `AIOT`
[TOC]
## 知識點
- 溫溼度感測器
    - DHT 溫溼度感測晶片
    - 讀取 DHT 溫溼度感測器
- 繼電器控制
    - 繼電器介紹
        - 透過 RPi.GPIO 控制繼電器
        - 使用 GPIOZero 控制繼電器
- 溫度異常資料監測控制繼電器
## 筆記
### DHT感測器
- 共有三個成員: DHT11、DHT21、DHT22
- DHT感測器出廠有四隻腳，第三隻腳沒有使用
    - 1: VCC
    - 2: DATA
    - 3: NC
    - 4: GND
- DHT11:
    - 價格便宜(<100)
    - 濕度範圍廣(20%-80%+-5%)
    - 溫度適用範圍(0-50+-2)
    - 取樣頻率每秒不可超過1次
- DHT22:
    - 價格高(150~250)
    - 濕度範圍廣(0%-100%+-2~5)
    - 溫度適用範圍(-40-125+-0.5)
    - 取樣頻率每2秒不可超過1次
- 讀取DHT
    - Adafruit_DHT模組
### 繼電器介紹
- 市面上有許多整合好電源輸入、接腳訊號、繼電器模組、燈號顯示的繼電器模組
- 常見的有一路、二路、四路、八路繼電器，可用於110v/220v的電壓，工作電流10安培，勿長時間滿載
## 實作
- [ ] 實作溫溼度感測器
- [ ] 實作繼電器控制
## reference
## extension