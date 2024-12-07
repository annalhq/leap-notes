---
created: 07-12-2024-20:57:36
modified: 07-12-2024-20:57:36
tags:
  - haskell
topics: Haskell
course: Haskell for Imperative Programmers
instructor: Philip Hagenlocher
---
## Functions

> [!info]
> name arg1 arg2 ... argn = < expr >

> [!example]
> 
> ```haskell
> in_range min max x =
> 	x >= min && x <= max
> in_range 0 5 3
>  => True
>  in_rang 4 5 3
>  => False 
> ```
```
```

---
#### Types

**name :: <'type'>**

>Examples

```haskell
x :: Integer
x = 1

y :: Bool
y = True

z :: Float
z = 3.14159265358
```

---
#### Types for Functions

>Example

```haskell
in_range :: Integer -> Integer -> Integer -> Bool
in_range min max x = x >= min && x <= max

in_range 0.5 1.5 1 -- Type error
in_range 0 5 3 -- Correct
```

---
#### Let bindings in functions

```haskell
in_range min max x = 
	let in_lower_bound = min <= x
		in_upper_bound = max >= x
	in
	in_lower_bound && in_upper_bound
```

---

## References
- 
