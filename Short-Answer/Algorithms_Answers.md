Add your answers to the Algorithms exercises here.

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
b) O(n)

suppose n:=5/6/7/8/9/10

  sum = 0
    for i in range(n): # 5/6/7/8/9/10
      i += 1
      for j in range(i + 1, n): # 3/4/5/6/7/8
        j += 1
        for k in range(j + 1, n): #1/2/3/4/5/6
          k += 1
          for l in range(k + 1, 10 + k): # 10/10/10/10/10/10
            l += 1
            sum += 1

  n     loop executions
---    ---------------
 <5            0
 5            19
 6            22
 7            25
 8            28
 9            31
 10           34

 as n scales upwards, total loops scale the same amount + 3 -- linear
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
