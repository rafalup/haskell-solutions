# Question 9.

Pack consecutive duplicates of list elements into sublists. If a list contains repeated elements they should be placed in separate sublists.

Example:
```
* (pack '(a a a a b c c a a d e e e e))
((A A A A) (B) (C C) (A A) (D) (E E E E))
```
Example in Haskell:
```
λ> pack ['a', 'a', 'a', 'a', 'b', 'c', 'c', 'a', 
             'a', 'd', 'e', 'e', 'e', 'e']
["aaaa","b","cc","aa","d","eeee"]
```


Below, we have a resolution of the exercise
```
pack :: (Eq a) => [a] -> [[a]]
pack = foldr foldLogic []
  where foldLogic e [] = [[e]]
        foldLogic e acc@(x:xs) = if head x == e then (e:x):xs else [e]:acc
```

Let's go to the next [question](question10.md)