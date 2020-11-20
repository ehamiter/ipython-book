# xmode

<pre class="output">
%xmode:
    Switch modes for the exception handlers.
</pre>

`%xmode` toggles between different modes of exception handling (plain, context, verbose, minimal). A mode can also be passed in directly as a parameter.

```python
In [1]: bologna
NameError: name 'bologna' is not defined


In [2]: %xmode
Exception reporting mode: Plain

In [3]: bologna
Traceback (most recent call last):
  File "<ipython-input-38-5de53f9f76d4>", line 1, in <module>
    bologna
NameError: name 'bologna' is not defined


In [4]: %xmode verbose
Exception reporting mode: Verbose

In [5]: bologna
---------------------------------------------------------------------------
NameError                                 Traceback (most recent call last)
<ipython-input-40-5de53f9f76d4> in <module>
----> 1 bologna
        global bologna = undefined

NameError: name 'bologna' is not defined
```
