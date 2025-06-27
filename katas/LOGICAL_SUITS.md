# 1️⃣2️⃣3️⃣ LOGICAL SUITS 4️⃣5️⃣6️⃣

## Goal

Given 3 integers, complete the logical suit and return the 3 following ones

## Rules
- given and returned elements are always integers
- transformation factor are always between 1 and 10 (included). 
Except for fibonacci and prime numbers

## Example

### input

```ruby
[1, 2, 3]
```

### Output

```ruby
[4, 5, 6]
```

## Handled Transformations

### Additions

```ruby
# +5 from 10 
[10, 15, 20] # => [25, 30, 35] 

# +2 from 34 
[34, 36, 38] # => [40, 42, 44] 
```

### Substractions

```ruby
# -3 from 100
[100, 97, 94] # => [91, 88, 85]

# -10 from 42
[42, 32, 22] # => [12, 2, -8]
```

### Multiplications

```ruby
# *2 from 50
[50, 100, 200] # => [400, 800, 1_600]

# *5 from 12
[12, 60, 300] # => [1500, 7_500, 37_500]
```

### Divisions

```ruby
# /10 from 100_000
[100_000, 10_000, 1_000] # => [100, 10, 1]

# /3 from 729
[729, 243, 81] # => [27, 9, 3]
```

### Powers

```ruby
# **2 from 3
[3, 9, 81] # => [6_561, 43_046_721, 1_853_020_188_851_841]

# **3 from 2
[2, 8, 27] # => [19_683, 7_625_597_484_987, 443_426_488_243_037_769_948_249_630_619_149_892_803]
```

### Fibonacci

```ruby
# from 34
[34, 55, 89] # => [144, 233, 377]

# from 4181
[4_181, 6_765, 10_946] # => [17_711, 28_657, 46_368]
```

### Prime Numbers

```ruby
# from 547
[547, 557, 563] # => [569, 571, 577]

# from 1229
[1_229, 1_231, 1_237] # => [1_249, 1_259, 1_277]
```

## Ideas to go further

- incremental multiplications *2, *3, *4, ...
- ...
