# Question 5.

Reverse a list.

Example in Haskell:

```
λ> myReverse "A man, a plan, a canal, panama!"
"!amanap ,lanac a ,nalp a ,nam A"
λ> myReverse [1,2,3,4]
[4,3,2,1]
```

Below, we have a resolution of the exercise

```
myReverse :: [a] -> [a]
myReverse = foldl (\acc x -> x : acc) []
```



Let's go to the next [question](question6.md)
