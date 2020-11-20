# tb

<pre class="output">
%tb:
    Print the last traceback.
</pre>

`%tb` prints the last traceback. You can also pass in exception reporting modes (plain, context, verbose, minimal) to get more or less information (normally set with [`%xmode`](./xmode.md)):

```python
In [1]: 5 // 0
---------------------------------------------------------------------------
ZeroDivisionError                         Traceback (most recent call last)
<ipython-input-7-e6530c2158eb> in <module>
----> 1 5 // 0

ZeroDivisionError: integer division or modulo by zero

In [2]: %tb
---------------------------------------------------------------------------
ZeroDivisionError                         Traceback (most recent call last)
<ipython-input-7-e6530c2158eb> in <module>
----> 1 5 // 0

ZeroDivisionError: integer division or modulo by zero

In [3]: %tb plain
Traceback (most recent call last):
  File "<ipython-input-23-e6530c2158eb>", line 1, in <module>
    5 // 0
ZeroDivisionError: integer division or modulo by zero

In [4]: %tb minimal
ZeroDivisionError: integer division or modulo by zero
```
