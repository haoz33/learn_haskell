# List Length

Count the number of elements in an array without using count, size or length operators (or their equivalents). 

# Solution 
```haskell 
len :: [a] -> Int
len lst = sum (map (\x -> 1) lst)
```

```haskell
len :: [a] -> Int
len [] = 0
len (x:xs) = 1 + len xs
```

```haskell 
len :: [a] -> Int
len lst = sum [1 | _ <- lst]
```