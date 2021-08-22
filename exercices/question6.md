# Question 6.

Find out whether a list is a palindrome. A palindrome can be read forward or backward; e.g. (x a m a x).

Example in Haskell:

```
λ> isPalindrome [1,2,3]
False
λ> isPalindrome "madamimadam"
True
λ> isPalindrome [1,2,4,8,16,8,4,2,1]
True
```

Below, we have a resolution of the exercise

```
isPalindrome :: (Eq a) => [a] -> Bool
isPalindrome xs = if xs == reverse xs then True else False
```

Let's go to the next [question](question8.md)
