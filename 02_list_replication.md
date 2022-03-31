# List Replication 

Given a list, repeat each element in the list  amount of times. 


# List comprehension 

Syntax

> [function variable | to_bind <- list]

1. Exmaple of turn turn elements in a list into upper case 

```haskell
[toUpper x | x <- ['h','e','l','l','o']]
> "HELLO"
```


2. Exmaple of doulbe every element in a list

```haskell 
[ x * 2 | x <- [1..10]]
> [2,4,6,8,10,12,14,16,18,20]  
```

Here we use the binded variable directly without create a function. 

3. Exmaple of doulbe every element in a list with a separated function 

```haskell
doubleMe x = x * 2 
[doubleMe x | x <- [1..10]]
> [2,4,6,8,10,12,14,16,18,20]  
```

We can also have multiple generator separated by comma, the latter generator will apply to the result list of the first generator.

4. Exmaple of multiple generator

```haskell
[ i | i <- [1,2], j <- [1..4]]

> [1,1,1,1,2,2,2,2]
```


Equivalence in For loop 
```python
result = []
for i in range(1,3):
    for j in range(4):
        result.append(i)

> [1,1,1,1,2,2,2,2]
```





# Soultion
```haskell
f :: Int -> [Int] -> [Int]
f n arr = [num | num <- arr, a <- [1 .. n]]
```

# Another way to solve

```haskell
f :: Int -> [Int] -> [Int]
f n arr = concat (map (\x -> replicate n x) arr)
```

In this solution we have used 3 functions to achieve effect of replicate a list.

`concat`

concat turns list of list into a flat list
```haskell
concat [[1,2,3],[4,5,6]]
> [1,2,3,4,5,6]
```

`map`

map transform a list into another list by appling a given function 

```haskell
map abs [-1,2,-3]
> [1,2,3]
```

with the use of lambda function we can achieve more complicated transformation

```haskell
map (\x -> x + 2) [-1,2,-3]
> [1,4,-1]
```

`replicate`

replicate creates a list of replicated items. It takes two argument, repeat times, and the item need to be repeated.

```haskell
replicate 3 5 
> [5,5,5]
```

