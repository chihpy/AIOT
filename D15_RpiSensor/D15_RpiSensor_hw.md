# D15_RpiSensor
###### tags: `homework`
[TOC]

## 作業1：
- 練習將 DHT22 接於 GPIO 27 接腳，並且更改軟體的接腳設定值，重新執行範例程式，驗證在不同的接腳上安裝 DHT22，程式一樣可以正確地讀出數值。
### sol:
- `pip3 install Adafruit_DHT`
![](https://i.imgur.com/gwLdRl8.jpg)


## 作業2：
- 觀察 RPi.GPIO 的程式碼，與 GPIOZero 程式碼對於繼電器控制上寫法的不同，如果我們要設定 GPIO 26, 19, 13, 6 四個接腳控制一個四路繼電器，練習實作一個 GPIOZero 四路繼電器的控制程式。


## 作業3：
- 將作業 1 與作業 2 結合，設定程式在溫度 10 度以下，打開 GPIO26，溫度 10 度以上到 20 度之間，控制 GPIO19，溫度 20 度到 30 度之間，控制 GPIO13，溫度在 30 度以上，控制 GPIO6，達成在不同的溫度區間時，控制不同的繼電器的需求。

- 由於沒有溫溼度感測器、繼電器，以PIRSensor替代
- [PIRSensor]()