# timeit

<pre class="output">
%timeit:
    Time execution of a Python statement or expression
</pre>

`%timeit` is a commonly used magic command used for gauging the efficiency and speed of a function. Suppose we have two methods that return the same result, but we're not exactly sure which one is more efficient (which is especially helpful if you're not super familiar with [Big O notation](https://en.wikipedia.org/wiki/Big_O_notation)).

<pre class="output">
In [1]: def square(x):
   ...:     return pow(x, 2)

In [2]: square(2)
Out[2]: 4

In [3]: def square_alternative(x):
   ...:     return x * x

In [4]: square_alternative(2)
Out[4]: 4

In [5]: %timeit square(2)
479 ns ± 15.3 ns per loop (mean ± std. dev. of 7 runs, 1000000 loops each)

In [6]: %timeit square_alternative(2)
130 ns ± 0.217 ns per loop (mean ± std. dev. of 7 runs, 10000000 loops each)
</pre>

In this example we can see that the `square_alternative()` is much faster than  the `square()` function that uses Python's builtin `pow()` function.

We can also use cell magic to only time certain aspects of a function if it requires some initial setup. Suppose we want to run the `square_alternative` function on a number that will be caluculated, but we don't want to include the initial calculation of `x`. We can do this using two `%` symbols, so it only times the last line:

<pre class="output">
In [7]: import math

In [8]: %%timeit x = math.pi * math.tau
   ...: square_alternative(x)
   ...:
   ...:
132 ns ± 1.54 ns per loop (mean ± std. dev. of 7 runs, 10000000 loops each)
</pre>
