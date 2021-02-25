# D08 MongoDB
###### tags: `homework`
[TOC]
- 作業: 安裝MongoDB、Robo 3T 工具
## 目標
- 成功安裝 Mongo資料庫及GUI工具
- 能夠使用命令提示工具(cmd、terminal)操作Mongo資料
- 能夠使用 Robo 3T 操作Mongo資料
## 重點
- 了解 DB、Collection、Document 在 Mongo 中所代表的意義。
- 能夠手動對資料做增刪改查的操作。
## 作業1
- 至以下網站下載 MongoDB 和 Robo 3T 工具，並成功運行。
- [Mongo](https://www.mongodb.com/try/download/community)
- [Robo 3T](https://robomongo.org/)
## 作業2
- 分別使用命令提示工具、Robo 3T圖形介面工具，照以下步驟操作資料。
    - 新增一個 DB 名稱自訂。
    - 在該 DB 中新增一個 Collection 名稱為 member
    - 在 Collection 中新增一筆會員資料，資料結構如下：
        ```
        name : Kevin
        email : test@abc.com
        phone: 0912345678
        ```
    - 將上述那筆資料的 name 欄位改成 Cathy
    - 加入新的欄位 age 到上述那筆資料中，並將值的部分設為 25
### sol:
- `docker pull mongo`
- `docker run -d --name mongo1 -p 8088:27017 mongo`
- `docker run -it mongo1 mongo`
- `// in mongo shell`
- `use [dbname]`
    - db不存在會自己創建
- `db.member.insert({'name' : 'Keven', 'email' :'keven@mongo.com', 'phone' : 0911111111 })`
    - collection不存在會自己創建
- `db.member.update({"name":"Keven"}, {$set:{"name":"Cathy"}})`
    - `$set的使用`，不能直接改喔，不然其他key會直接消失
- `db.member.update({"name" : "Cathy"}, {$set:{"age" : 25}})`
![](https://i.imgur.com/ec1hBms.png)
