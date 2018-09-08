```python
x = 25
epsilon = 0.01
numGuesses = 0
low = 0.0
high = max(1.0, x)
ans = (high + low)/2.0
i=0
while abs(ans**2 - x) >= epsilon:
    i+=1
    print('low =', low, 'high =', high, 'ans =', ans)
    
    if ans**2 < x:
        low = ans
    else:
        high = ans
    ans = (high + low)/2.0
print('numGuesses =', numGuesses)
print(ans, 'is close to square root of', x)
```

牛顿-拉普森法 数学没学过

牛顿证明了一个定理：如果存在一个值guess 是多项式p 的根的近似值，那么guess –

p(guess)/p'(guess) 就是一个更好的近似值，其中p’ 是p 的一次导数。

对于任意的常数k 和任意的系数c ，多项式cx2 + k 的一次导数是2cx 。例如，x2 – k 的一次导数

是2x 。因此，如果当前的猜测是y ，那么可以选择y – (y2 + k)/2y 作为下一个猜测。这种方法称为逐次逼近 。

```python
x = -25
flag=0
if x<0:
    x=abs(x)
    flag=1

epsilon = 0.01
numGuesses = 0
low = 0.0
high = max(1.0, x)
ans = (high + low)/2.0
while abs(ans**2 - x) >= epsilon:
    
    print('low =', low, 'high =', high, 'ans =', ans)
    numGuesses += 1
    if ans**2 < x:
        low = ans
    else:
        high = ans
    ans = (high + low)/2.0
if flag==1:
    ans=-ans
    x=-x
else:
    pass
print('numGuesses =', numGuesses)
print(ans, 'is close to square root of', x)
```
