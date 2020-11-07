# doctest_mode

<pre class="output">
%doctest_mode:
    Toggle doctest mode on and off.
</pre>

You can change the way that IPython's prompts, exceptions, and output looks by running `%doctest_mode`. This makes it easy to copy and paste code that has characters such as `>>>` and `...` and have it recognize it. This is also handy if you use [`doctests`](https://docs.python.org/3/library/doctest.html) in your docstrings, as you can directly copy and paste them from the shell without having to leave the session and they are ready to use in your functions.

An example:

```python
In [1]: def my_amazing_function(a, b):
    ...:     return a * b
    ...:

In [2]: %doctest_mode
Exception reporting mode: Plain
Doctest mode is: ON
>>> my_amazing_function(2, 4)
8
>>> my_amazing_function('woo', 3)
'woowoowoo'
>>> %doctest_mode
Exception reporting mode: Context
Doctest mode is: OFF
```

Now you can copy and paste the examples directly into your code's docstring. Below is a complete working example, let's say saved as `example.py`:

```python
def my_amazing_function(a, b):
    """
    >>> my_amazing_function(2, 4)
    8
    >>> my_amazing_function('woo', 3)
    'woowoowoo'
    """
    return a * b

if __name__ == "__main__":
    import doctest
    doctest.testmod()
```

So running `python example.py` will run the doctest and verify your statements are true. You won't see any message (since it passes) but you can pass in the `-v` parameter for it to print a verbose log.

```
python example.py -v
```

<pre class="output">
Trying:
    my_amazing_function(2, 4)
Expecting:
    8
ok
Trying:
    my_amazing_function('woo', 3)
Expecting:
    'woowoowoo'
ok
1 items had no tests:
    __main__
1 items passed all tests:
   2 tests in __main__.my_amazing_function
2 tests in 2 items.
2 passed and 0 failed.
Test passed.
</pre>
