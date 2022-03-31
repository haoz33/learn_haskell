# Filter Positions in a List 

For a given list with `X` integers, return a new list removing the elements at odd positions.

# Example input and output 
```haskell 
f [1,2,3,4,5]
> [2,4]
```


## zip 
`zip` returns a list of tuple where each tuple contains element of both list occuring at the same position 

```haskell
zip [0,1,2] [1,2,3]
> [(0,1),(1,2),(2,3)]
```


## fst & snd 
`fst` and `snd` is a way to retrive a value from tuple, `fst` returns first item in the tuple, `snd` returns the second item in a tuple.


```haskell
f lst = filter ( (\x -> odd x) zip [0..] lst)

```