# Lab1-3 用Python實戰一下囉

## Quiz 1: 作出兩組平行線

![image](https://user-images.githubusercontent.com/89304181/190890015-d61afc65-f928-43dc-b438-2c69461c1973.png)

## Quiz 2: 作出三角形 (含面積計算)

````python
import numpy as np
#import math

x = [1, 6, 3] # x axis location for 3 points
y = [5, 3, -1] # y axis location for 3 points

# The argument of square root mustn't be negative. 
a = sqrt((x[1]-x[0])**2) + ((y[1]-y[0])**2) # Length:AB
b = sqrt((x[2]-x[1])**2) + ((y[2]-y[1])**2) # Length:AB
c = sqrt((x[2]-x[0])**2) + ((y[2]-y[0])**2) # Length:AB

s = (a+b+c)/2

calc = abs(s*(s-a)*(s-b)*(s-c))

print('a=%g, b=%g, c=%g, s=%g, calc=%g' % (a, b, c, s, calc))

area = calc**0.5
print('The area = %g'% area)

# Draw a triangle

import matplotlib.pyplot as plt

xx = x
xx.append(x[0])
yy = y
yy.append(y[0])
plt.plot(xx, yy)
plt.show()

````
![image](https://user-images.githubusercontent.com/89304181/190890122-c75d9727-e362-4e87-8a05-af86d110ce2e.png)


## Quiz 3: 求x, y, z = ?

![image](https://user-images.githubusercontent.com/89304181/190890181-011b3bbf-d5a3-4e61-ab15-537ea32dd51f.png)

```python

import numpy as a
c = a.array([[3,-2, -1], [1,-3,2], [2,-8,5]])
d = a.array([6, -5, -15])
ans = a.linalg.solve(c,d)
print('Ans: ', ans)

## Ans: Ans:  [ 3.  2. -1.]
```

## Quiz 4: 試試看求解並比較結果是否一致?

![image](https://user-images.githubusercontent.com/89304181/190890351-679b933f-35c8-45a6-ad38-1413f458b590.png)

![image](https://user-images.githubusercontent.com/89304181/190890434-090b03f3-23e1-4969-84f7-ebbb6cbc9672.png)


## Quiz 5: 外積?

![image](https://user-images.githubusercontent.com/89304181/190890450-42527270-f1eb-4265-817c-0e94fed33924.png)

```python
m = [3, 2, 1]
n = [2, 3, -1]

import numpy as a 

m = a.array(m)
n = a.array(n)
d = a.cross(m,n)
d2 = a.cross(n,m)
print('Outer Product of m*n:', d)
print('Outer Product of n*m:', d2)

# Result
# Outer Product of m*n: [-5  5  5]
# Outer Product of n*m: [ 5 -5 -5]
```

## Quiz 6:最後的小問題 → 

> 在完成＂Lab1: Python起手式: 三週學會國高中數學＂後，對於用Python學習數學的方式，有什麼不同的心情與體會？另外，對於以程式作為國高中在數學學習的輔助上，您會有什麼樣的想法與建議。Thanks!

> Ans: 已經有越來越多的研究發現與支持, 對於數學要解的問題， 會先簡單說明求解的方法，基本上就是回顧原先熟悉的手算作法。因 為知道如何手算，接下來問題只剩下如何以程式去實現。無論使用哪一種解法，接 下來都是將手算的作法轉換成可執行的程式碼，讓電腦快速完成計算。
> 同時; 對台灣學生而言，幾乎天天都與數學打交道，每日逼迫自己運用「數學思維」作題目寫考卷，每位學生早已處在學好程式設計的有利位置而不自知，只要經過一些訓練，學習如何將數學用於程式設計，學好基礎程式設計只是早晚的事而已。
> 這個單位引導我們如何將從小所學到的數學, 從考試卷的封印中解除，學習如何運用「數學思維」於程式設計中，只要利用一點點國中數學，就會發現基礎程式設計真得很容易，遠比數學考卷簡單得多，程式設計只不過是基礎數學的直接應用而已。
> 所以, 學好程式設計可說是辛苦學數學過程中的一個附帶豐厚獎品，得來全不費功夫。



