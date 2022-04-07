# Area Under Curves and Volume of Revolving a Curve

## Exmaple input and output 

```haskell 
solve 1 4 [1,2,3,4,5] [6,7,8,9,10] 
> [2435300.3, 26172951168940.8]
```

## Formula 

> f(x) = (a[0] * x ^ b[0]) + (a[1] * x ^ b[1]) + ...


```python
area = 0
subinterval = 0.001
 
for i in my_range(1, 4, subinterval):
    area += f(i) * subinterval
```

Volume
```python
volume = 0
subinterval = 0.001
for i in my_range(1, 4, subinterval):
    volume += f(i) ^ 2 * subinterval * pi

```

# One possible solution

```haskell 

f z a b = sum (map (\x -> fst x * z ^ snd x ) (zip a b) )

area l r a b = sum ( map (\x -> 0.01 * (f x a b)) [l,1.001..r])

volume l r a b = sum ( map ((\x -> pi * 0.01 * (f x a b) ^ 2)) [1,1.001..r])

solve l r a b = [area l r a b, volume l r a b]

```