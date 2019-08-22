Add your answers to the Algorithms exercises here.

Exercise I:

```
a) O(n) (linear)

  a = 0
    while (a < n * n * n):    #occurs n times
      a = a + n * n    #occurs 1 time

 n     loop executions
---    ---------------
 1            1
 2            2
 3            3
 4            4

```

```
b) O(n^3)

  sum = 0
    for i in range(n): # occurs n times
      i += 1
      for j in range(i + 1, n): # occurs n-1 times
        j += 1
        for k in range(j + 1, n): # occurs n-2 time
          k += 1
          for l in range(k + 1, 10 + k): # occurs 10 times
            l += 1
            sum += 1

  n     total loop executions (as evidenced by new sum value)
---    ------------------------------------------------------
 <5            0
 5            99
 6            423
 7            1125

as input scales upwards, loop executions scale (n*n-1*n-2*10), where n^3 is the dominant term
```

```
c)  O(n)

def bunnyEars(bunnies):
      if bunnies == 0:
        return 0

      return 2 + bunnyEars(bunnies-1)

  n     loop executions
---    ---------------
 1            1
 2            2
 3            3

 essentially just counts down recursively from n, so scales with n

```

Exercise II:

```


n := [1,2,3,4,5]
f :=2

def find_floor(n,f):

work like recursive binary search:
#find middle as current floor
current=(n[0] + n[-1])//2

if egg breaks on current but DOESN'T break on current-1:
    #base case, success, we found it
    return middle
elif egg breaks on current AND on current-1
    # floor is lower
    return find_floor(n[:middle], f)
else: egg doesn't break
    # floor is further up
    return find_floor(n[middle:], f)


Binary search improves with speed with every loop, so runtime complexity --> O(log n)


```
