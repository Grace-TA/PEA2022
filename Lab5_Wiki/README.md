# Lab5: 自動訪問維基百科 + 資料工程與分析


## Lab 5-1 起手式: 訪問 Wikipedia文章！

![image](https://user-images.githubusercontent.com/89304181/202890574-1289963d-1423-4430-804e-46c7818dfcf0.png)

```python
# 5101 摘要
wikipedia.set_lang("zh-tw")

kw = "中原大學"

M1 = wikipedia.summary(kw, auto_suggest=False)

# 5103 Wiki 文章中的部分
M2 = wikipedia.page(kw, auto_suggest=False).section('國際認證')
M3 = wikipedia.page(kw, auto_suggest=False).section('排名')

# 5111 Wiki 文章中的引用
M4 = wikipedia.page(kw, auto_suggest=False).references

wikipedia.set_lang("en") # 選擇語言: English

ekw = "Chung Yuan Christian University"
M5 = wikipedia.summary(ekw, auto_suggest=False)

```

## Lab 5-2 下載中文維基百科, 一起學習文章語料分詞和詞頻分析!

![image](https://user-images.githubusercontent.com/89304181/202891337-693942dd-3fec-45a1-b8b3-8307e4ae57be.png)

## Lab 5-3 Your Show Time: 找一篇簡體文章或新聞 實作H1~H6

![image](https://user-images.githubusercontent.com/89304181/202891353-933f20f3-fb60-4047-92b6-42cb41590710.png)

