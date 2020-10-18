# timeit

`%timeit` is a commonly used magic command used for gauging the efficiency and speed of a function. Suppose we have two methods that return the same result, but we're not exactly sure which one is more efficient (which is especially helpful if you're not super familiar with [Big O notation](https://en.wikipedia.org/wiki/Big_O_notation)).

<pre class="output">
In [1]: def power(x):
   ...:     return pow(x, 2)

In [2]: power(2)
Out[2]: 4

In [3]: def power_alternative(x):
   ...:     return x * x

In [4]: power_alternative(2)
Out[4]: 4

In [5]: %timeit power(2)
479 ns ± 15.3 ns per loop (mean ± std. dev. of 7 runs, 1000000 loops each)

In [6]: %timeit power_alternative(2)
130 ns ± 0.217 ns per loop (mean ± std. dev. of 7 runs, 10000000 loops each)
</pre>

In this example we can see that the `power_alternative()` is much faster than  the `power()` function that uses Python's builtin `pow()` function.