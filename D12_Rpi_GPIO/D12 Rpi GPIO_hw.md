# D12 Rpi GPIO
###### tags: `homework`
[TOC]

## 作業1：
- 實際練習 /sys/class/gpio 啟動 gpio，設定 gpio 接腳的狀態，並且卸載所啟動的 gpio。同時觀察卸載之後的 gpio 接腳，繼續送設定狀態的資料，將會發生什麼樣的狀態。
### sol:
- `cd /sys/class/gpio`
- `ls -al`
- `echo 4 > /sys/class/gpio/export`
    - 會發現`/sys/class/gpio`目錄下多了`gpio4`檔案
    - 代表gipo4啟動了
- 將GPIO4設為輸出接腳，並設定為高電位
    - `echo out > /sys/class/gpio/gpio4/direction`
    - `echo 1 > /sys/class/gpio/gpio4/value`
- 使用debugfs觀察GPIO設定
    - `cat /sys/kernel/debug/gpio`
    - note: 沒有設定高電位時顯示lo，設定後顯示hi
- 釋放gpio4
    - `echo 4 > /sys/class/gpio/unexport`
    - 所以再對gpio4下指令會顯示no such file or directory
## 作業2：
- 使用 raspi-config 啟動 i2c，觀察 gpio2 以及 gpio3 的變化
- 透過 /sys/kernel/debug/gpio 觀察改變的情形，嘗試重新做一次作業1，
- 針對 gpio2 以及 gpio3 操作，觀察在 i2c 啟動的狀態下，gpio2 以及 gpio3 相對 gpio4 有何不同。
### sol:
- i2c(gpio的2、3)啟動不會讓gpio設定失敗，


## 作業3：
- 使用 raspi-config 啟動 spi，觀察 gpio 各接腳的變化狀態，嘗試將 spi 關閉
- 透過 /sys/kernel/debug/gpio，觀察可以使用 gpio 數量的變化情形 。