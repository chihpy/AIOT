# D21_YOLO_train
###### tags: `homework`
[TOC]
## 重點
- 使用指令修改 yolo 的 cfg 檔

## 作業1：
- 請問 YOLO 訓練前，分別要對哪幾個檔案做設定？
### sol:
- 根據darknet的training範例:
- cfg檔:
    - batch_size要改
    - subdivisions要改(如果沒辦法一次forward就跑到num_batch)
    - max_batches要改(alexAB建議class*2000 but not less than number of training images)最大更新weight次數
    - steps通常設成80% and 90% max_batches(調learning rate用)
    - num_class要改
    - filters要改(因為class改了)
    - train.txt, valid.txt
- data檔(train.txt, valid.txt)
- name檔(classes name)
## 作業2：
- 請問 UNIX 的文字取代工具 sed 在使用時，指定參數 -i 有什麼意義？
### sol:
- edit files in place (makes backup if SUFFIX supplied)
- 沒-i不會直接寫入取代喔
## 作業3：
- 請問 UNIX 的文字編輯工具 echo 在使用時，指定參數 -e 有什麼意義？
### sol:
- enable interpretation of backslash escapes
- 比如出現`\n`就會換行，沒用`-e`會出現`\n`
## 作業4：
- 請在 colab 的儲存空間新建 "123.sh" 文件，透過echo指令往裡面寫入
### sol:
- [train.sh]()