# D18 Flask-PyMongo
###### tags: `homework`
[TOC]
- 作業：使用 Flask 操作 Mongo
## 目標
- 能夠使用 python 操作 mongodb 的增刪改查。
- API 設計上能符合 Restful 風格。
## 重點
- 能使用正確的 Http Method 去接收 Request。
- 實作之前，Mongo Server 要記得開啟。
- 若 DB 和 Collection 原本不存在，請先用 Robo3T 手動建立。
- 本作業你可能需要使用的 packages
    ```
    from pymongo import MongoClient
    from flask import Flask, request
    from bson.objectid import ObjectId
    ```
## 作業 1
- 使用 Post，傳入參數 name, age, email 參數，並把資料存入 Member Collection。
## 作業 2
- 使用 Get，取得所有的資料。
- 使用 Get，帶入要取得的資料 id 參數，並成功從 Mongo 中取得某一筆特定資料。
## 作業 3
- 使用 PUT，帶入要更新的資料id，並傳入 name, age, email 參數，並修改 Mongo 中某一筆資料的值。
## 作業 4
- 使用 DELETE，帶入要刪除的資料 id，並刪除 Mongo 中某一筆資料。