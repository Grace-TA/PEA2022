# Lab6: 化繁為簡的文字雲 ( WordCloud)


## Lab 6-1 溫故知新: 請自行找一篇你喜歡的繁體中文新聞或文章, 參考Lab5-3, 來實作H1 ~ H6

<img width="707" alt="image" src="https://user-images.githubusercontent.com/89304181/204117252-1fb15f0c-7633-4af0-b7a1-a9d2ee05bd6a.png">


## Lab 6-2 , 如何親自動手製作我們第一個文字雲呢? (三寶)

### 本課程的第一個文字雲

![image](https://user-images.githubusercontent.com/89304181/204117289-88c91508-59c3-473c-8a2c-72861fad9e5f.png)

### 文字雲 + 出現的圖形 (遮罩1)

![image](https://user-images.githubusercontent.com/89304181/204117291-2a0450d4-2bf9-4d4b-a09c-7ce8355b4232.png)

### 文字雲 + 出現的圖形 (遮罩2)

![image](https://user-images.githubusercontent.com/89304181/204117296-317da0ca-5d72-41ee-9bb6-2b6378836c3d.png)


## Lab 6-3 Your Show Time: 找一篇你喜歡的長文章或新聞, 選一個你喜歡的Mask來試試, 實作Lab 6-2.

### 1. 文章來源: https://news.cnyes.com/news/id/5019701

### 2. 結果, but "台", "積電"被分開
![image](https://user-images.githubusercontent.com/89304181/204124655-a42ebdfe-4e64-4c3e-9e34-804269b8dc24.png)

## 3. 使用"自訂詞庫"

![image](https://user-images.githubusercontent.com/89304181/204124791-62bf61d0-cdb7-4ac8-9cea-589c1110fdf0.png)


````python
text = open('news2.txt', "r",encoding="utf-8").read()  # ****** 讀文字資料 ******
 
jieba.set_dictionary('dictionary/dict.txt.big.txt')

jieba.load_userdict('dictionary/user_dict_test.txt')  #設定自訂詞庫

````
![image](https://user-images.githubusercontent.com/89304181/204124757-e7a2091e-0e61-4dcc-81eb-7e0bbdbd42ca.png)

