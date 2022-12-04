# AI工程程式與實作 - Lab3: 資料預測 &深度學習模型

<a name="000"/>

## 目錄(Table of Contents)

[Lab 3-1 數據分析](#111)

[Lab 3-2 實戰時刻! Let’s fight!](#222)

[Lab 3-3 如何零基礎入門深度學習?](#333)

[Lab 3-4 AI深度學習三步曲: 訓練、驗證、測試](#444)

[Lab 3-5 應用實作:  “微笑檢測應用於使用者滿意分析”](#555)
<a name="111"/>

## Lab 3-1 數據分析

### Pandas

![image](https://user-images.githubusercontent.com/89304181/193442492-3a3b3f83-174e-4275-9133-60b97d09994e.png)

### 一行程式，快速取得台銀牌告匯率

![image](https://user-images.githubusercontent.com/89304181/193442509-48a6e114-40f9-4ce1-b304-66073bb1e928.png)

### 掛接雲端硬碟，保存課程練習產生的檔案

![image](https://user-images.githubusercontent.com/89304181/193442541-58564c5b-990d-40a0-9a69-dbee9cff8dd6.png)

![image](https://user-images.githubusercontent.com/89304181/193442556-c1094c9c-85ab-4d52-95cd-3b387a2da808.png)

[return to content](#000) 

<a name="222"/>

## Lab 3-2 實戰時刻! Let’s fight!

### 1. 對特定產品item (e.g., #1 ~ #10)求銷售總額??

![image](https://user-images.githubusercontent.com/89304181/193442702-bba37a31-ff86-49be-af54-83df75aac601.png)

### 2. 平均分店的銷售總額??

![image](https://user-images.githubusercontent.com/89304181/193442739-54a792db-3a7c-44cb-8c5f-e1e78bcd2a00.png)

### 3. 品項太多，只查單一產品item #12的銷售總額

![image](https://user-images.githubusercontent.com/89304181/193443388-5cedf60d-ae11-4674-83e5-68902bb22542.png)

### 4. 狀況來了! BOSS現在就要看圖 : 那一個產品賣的好 os:有沒有搞錯91萬筆資料耶~ (debug). Ans: The best sale: #15! (最熱賣!)

![image](https://user-images.githubusercontent.com/89304181/193442608-7009a1ee-b124-4ad8-9480-97698984a289.png)

### 5. 哪一家分店長準備走路? Ans: Store #7 (銷售總額最差!)

![image](https://user-images.githubusercontent.com/89304181/193442619-04f0f2a6-8647-4e61-8f8e-2ae95b566ee3.png)

[return to content](#000) 

<a name="333"/>

## Lab 3-3 如何零基礎入門深度學習?

### 0. 把工作資料夾(所在目錄)設為課程資料夾，很重要!

![image](https://user-images.githubusercontent.com/89304181/193442889-d8cea1ca-68a9-4592-b3bd-a4ac6c4c4755.png)

### 1. 顯示圖形檔案.png & 下載手寫數字圖片到本機電腦: /0/10.png

![image](https://user-images.githubusercontent.com/89304181/193442918-d7c334a7-8c25-4664-ba34-9e2768ea3402.png)

### 2. 請選一個自己喜愛的數字; 並且在相同的數字下，看一下３張手寫數字圖片圖形檔案.png 的差異(e.g.,  在mist_png/testing/9/, 1000.png, 104.png, 12.png)

![image](https://user-images.githubusercontent.com/89304181/193442933-ab0bff73-af61-4334-908a-c7ae4c49aa2d.png)

[return to content](#000) 

<a name="444"/>

##  Lab 3-4 AI深度學習三步曲: 訓練、驗證、測試

![image](https://user-images.githubusercontent.com/89304181/196022842-a5ede13d-b3b6-4923-ad15-a4179ee0a7b2.png)

### 步驟 1. 資料集準備

![image](https://user-images.githubusercontent.com/89304181/196023019-4c0b432e-1173-46c4-98bb-eb28fb41604e.png)

### 步驟 2. 建模訓練 / 訓練

![image](https://user-images.githubusercontent.com/89304181/196023040-6e7cff31-1204-48c8-9445-94a11fef0d0a.png)


### 步驟 3. 預測未知 / 預測

![image](https://user-images.githubusercontent.com/89304181/196023057-f0f11cf4-1ef1-43a3-aa1e-dfdac0425388.png)

![image](https://user-images.githubusercontent.com/89304181/196023075-10ad531d-a6cf-43a0-a733-c2c7d611bbaa.png)

[return to content](#000) 

<a name="555"/>

## Lab 3-5 應用實作:  “微笑檢測應用於使用者滿意分析”

### 1. 顯示資料夾 樹狀結構, 確定完成資料的下載;並更新到你的GitHub實作中

<img width="400" alt="image" src="https://user-images.githubusercontent.com/89304181/197371940-a4b8c9e3-6c42-433d-9d43-94b408391ced.png">

## 2. 實測數據!! 最後可試著到網路找3張微笑或不微笑的臉來試試

### Smile Test 1

<img width="343" alt="image" src="https://user-images.githubusercontent.com/89304181/197371744-261e9889-6476-4c23-915c-88988ade5f3f.png">

### Smile Test 2

<img width="341" alt="image" src="https://user-images.githubusercontent.com/89304181/197371762-c32a981d-1977-45ad-b4db-b18bb250b136.png">

### Smile Test 3

<img width="349" alt="image" src="https://user-images.githubusercontent.com/89304181/197371768-289310f1-d399-48ce-9f30-4b4ac7dcb127.png">

### 人臉圖片預測微笑的程式

```python
## 人臉圖片預測微笑
def DetectSmile(fn): # Rewrite by Horace, 2022.10.23
  test_images = []
  t_image = cv2.imread(fn) #2000 1000 
  t_image = cv2.cvtColor(t_image, cv2.COLOR_BGR2GRAY)
  t_image = cv2.resize(t_image,(60,64))
  test_images.append(t_image)

  plt.imshow(t_image)
  test_images = np.asarray(test_images)
  test_images = test_images.astype(np.float32) / 255.

  test_images = np.expand_dims(test_images, axis=-1)
  p = model.predict(np.array([test_images[0]]))[0]

  print(p)
  class_names = ["Neutral:中性","Smiling:微笑"]
  bar_width = 50 #刻度寬度
  left_count = int(p[1] * bar_width) #使用Smiling決定 左邊刻度
  right_count = bar_width - left_count 
  left_side = '-' * left_count #顯示左邊長度
  right_side = '-' * right_count #顯示右邊長度
  print (class_names[0], left_side + '<|>' + right_side, class_names[1])
```

[return to content](#000) 
