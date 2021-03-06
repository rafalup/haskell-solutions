# Question 7.

Flatten a nested list structure.

Transform a list, possibly holding lists as elements into a `flat' list by replacing each list with its elements (recursively).

Example:

```
* (my-flatten '(a (b (c d) e)))
(A B C D E)
```

Example in Haskell:

We have to define a new data type, because lists in Haskell are homogeneous.

```
data NestedList a = Elem a | List [NestedList a]
λ> flatten (Elem 5)
[5]
λ> flatten (List [Elem 1, List [Elem 2, List [Elem 3, Elem 4], Elem 5]])
[1,2,3,4,5]
λ> flatten (List [])
[]
```

Below, we have a resolution of the exercise

```
data NestedList a = Elem a | List [NestedList a]

flatten :: NestedList a -> [a]
flatten (Elem x) = [x]
flatten (List []) = []
flatten (List (x:xs)) = (flatten x) ++ (flatten (List xs))
```

Let's go to the next [question](question8.md)
