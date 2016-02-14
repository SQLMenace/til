If we populate a vector with the numbers between 1 and 10, we can use functions head and tail to limit what we are returning. Head and tail by default return the first 6 rows or the last 6 rows

```R
> Z <- (1:10)


> Z
 [1]  1  2  3  4  5  6  7  8  9 10



```


Using the head function

```R
> head(Z)

[1] 1 2 3 4 5 6

```

Using the tail function

```R
> tail(Z)

[1]  5  6  7  8  9 10

```

We can also pass in a parameter to the head and tail function to specify how many rows we want back, in this case I am using 2 


```R
> head(Z, 2)

[1] 1 2


> tail(Z,2)

[1]  9 10

> 
```
