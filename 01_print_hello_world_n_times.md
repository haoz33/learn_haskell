# Print "Hello World" N Times

Print "Hello World" N Times, where N is a integer number.

In order to solve this problem, we will need know how to do two things.

- how to use function 
- how to loop 

## Function

To define a function, we use the following syntax.

> functionName parameter1, ..., parameterN  = body

### Exmaple function
```haskell
add x y = x + y
```

Use type definition to annotate the type of parameters and return type.

> parameter type -> ... -> parameter type -> return type

```haskell
add :: Integer -> Integer -> Integer
add x y = x + y
```

To call a function we simply use the function name follow by the parameters required by the function.

```haskell
add 2 3 
> 5
```

## Loop

In Haskell there is no traditional loop like for loop in other languages, but we can use recursion to achieve the same result as loop. 

Recursion is where a function call itself inside the body of that function. 

### Example of recursion 

```haskell 
hello_worlds n = do
        putStrLn "Hello World" 
        hello_worlds (n)
```

As you may notice, the function will not stop and will run forever because there is no stop condition and the function just call itself indefinitely.

We can stop the function with condition by using pattern matching.

## Pattern matching 

```haskell
hello_worlds 0 = return ()
hello_worlds n = do
        putStrLn "Hello World" 
        hello_worlds (n - 1)
```

From the above code, we can see that pattern matching is done with specific the function name following by the parameter and body, the specified parameter is passed the body will executed instead of the original function body. 

