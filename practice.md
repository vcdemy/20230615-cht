# Turtle繪圖練習

請點擊[trinket.io](https://trinket.io/)開始練習寫程式！

## 繪製正方形

```python
import turtle

turtle.forward(100)
turtle.left(90)
turtle.forward(100)
turtle.left(90)
turtle.forward(100)
turtle.left(90)
turtle.forward(100)
turtle.left(90)
```

## for迴圈解決重複性問題
```python
import turtle

for i in range(4):
    turtle.forward(100)
    turtle.left(90)
```
注意：縮排很重要！縮排標示出程式區塊！

## 在不同位置畫出不同形狀
```python
import turtle

turtle.penup()
turtle.goto(50, 50)
turtle.pendown()
n = 3
for i in range(n):
    turtle.forward(100)
    turtle.left(360/n)

turtle.penup()
turtle.goto(-50, 50)
turtle.pendown()
n = 4
for i in range(n):
    turtle.forward(100)
    turtle.left(360/n)
```

## 使用函式(function)解決整個程式區塊重複的問題
```python
import turtle

def polygon(x, y, n):
    turtle.penup()
    turtle.goto(x, y)
    turtle.pendown()
    for i in range(n):
        turtle.forward(100)
        turtle.left(360/n)

polygon(50, 50, 3)
polygon(-50, 50, 4)
```
