# recall

<pre class="output">
%recall:
    Repeat a command, or get command to input line for editing.
</pre>

`%recall` (along with its alias `%rep`) repeats a command, and places the resulting output into a new line input. This allows you to create elaborate command lines without relying on copying and pasting.

```python
In [1]: grocery_list = ['apples', 'bananas', 'soup', 'ice cream']

In [2]: ", ".join(grocery_list)
Out[2]: 'apples, bananas, soup, ice cream'

In [3]: %recall

In [4]: apples, bananas, soup, ice cream  # <= The cursor will be waiting here
```

You can also place lines from history (find out by using [`%history -n`](./history.md)) on the next input prompt:

```python
In [5]: a = 'foo'

In [6]: b = 'bar'

In [7]: c = a + ' ' + b

In [8]: c
Out[8]: 'foo bar'

In [9]: %recall 7

In [10]: c = a + ' ' + b  # <= The cursor will be waiting here
```
