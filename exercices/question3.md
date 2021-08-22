# Question 3.
Find the K'th element of a list. The first element in the list is number 1.

Example:

```
* (element-at '(a b c d e) 3)
c
```
Example in Haskell:
```
λ> elementAt [1,2,3] 2
2
λ> elementAt "haskell" 5
'e'
```

Below, we have a resolution of the exercise

```
elementAt :: [a] -> Int -> a
elementAt xs idx
    | idx > len || idx < 1 = error "index exceeds list's length"
    | otherwise = xs !! (idx - 1)
    where len = length xs
```



Let's go to the next [question](question4.md)
