# Question 2.
Find the last but one element of a list.

(Note that the Lisp transcription of this problem is incorrect.)

Example in Haskell:

```
λ> myButLast [1,2,3,4]
3
λ> myButLast ['a'..'z']
'y'
```

Below, we have a resolution of the exercise

```
myButLast :: [a] -> a
myButLast xs
    | len <= 2 = error "contains one or less elements"
    | otherwise = xs !! (len - 2)
    where len = length xs
```




Let's go to the next [question](question3.md)
