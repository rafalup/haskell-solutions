# Question 4.
Find the number of elements of a list.

Example in Haskell:

```
λ> myLength [123, 456, 789]
3
λ> myLength "Hello, world!"
13
```

Below, we have a resolution of the exercise

```
myLength :: [a] -> Int
myLength [] = 0
myLength (x:xs) = 1 + myLength xs
```


Let's go to the next [question](question5.md)
