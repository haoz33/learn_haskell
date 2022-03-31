# Filter Array
Filter a given array of integers and output only those values that are less than a specified value `X`.

# Exmaple Input and Output 
```haskell
f 3 [1,2,3,4,5,6,7,8,9,10]
> [1,2]
```

## filter 

`filter` is a built-in function in haskell used to filter a list. It returns a list that meets the given requirement.

```haskell
filter (>5) [1,2,3,4,5,6]
> [6]
```


# Solution
```haskell
f :: Int -> [Int] -> [Int]
f n arr = filter (<n) arr
```