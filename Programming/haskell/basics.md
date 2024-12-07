---
created: 07-12-2024-16:21:31
modified: 07-12-2024-16:21:31
tags:
  - haskell
topics: Haskell
course: Haskell for Imperative Programmers
instructor: Philip Hagenlocher
---
## Introduction

### Functional Programming

```ad-note
What is functional programming?
In FP, we are interested in mathematical defintion of functions. They have some input, arguments and the outputs a result.

```
 
 - Pure (mathematical functions)
 - Immutable data
 - No/less side-effects
 - Declarative
 - Easier to verify

> [!important]
> Haskell is **lazy** evaluated

### Lazy vs Strict

Lazy:
```haskell
func arg =
	let x = func1 arg
		y = func2 arg
		z = func3 arg
	in
	if z then x else y
	
```

Strict:
```cpp
int func(int arg) {
	int x = func1(arg);
	int y = func2(arg);
	int z = func3(arg);

	if(z){
		return x;
	}
	else return y;
}
```

Here in lazy evaluation it will first calculate the value of **z** and then according to that it will decide whether to calculate x or y, so effectively it will be only 2 step process.

Whereas in strict evaluation it will first calculate all three variables x,y,z and then will proceed further,
an effective 3 step process

---
## References
- 
