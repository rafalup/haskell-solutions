# Question 1.
Find the last element of a list.

(Note that the Lisp transcription of this problem is incorrect.)

Example in Haskell:

```
λ> myLast [1,2,3,4]
4
λ> myLast ['x','y','z']
'z'
```

Below, we have a resolution of the exercise

```
myLast :: [a] -> a
myLast [] = error "empty list"
myLast [x] = x
myLast (x:xs) = myLast xs
```


Let's go to the next [question](question2.md)
