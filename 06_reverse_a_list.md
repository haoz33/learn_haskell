# Reverse a list 
You are given a list of  elements. Reverse the list without using the reverse function.

# Solution 

```haskell
rev l = reverse l
```

# Other Solution 
```haskell
rev [] = []
rev (x:xs) = rev xs ++ [x]
```