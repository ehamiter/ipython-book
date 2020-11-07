# debug

<pre class="output">
%debug:
    Activate the interactive debugger.
</pre>

If an exception has just occurred, you can inspect its stack interactively by entering `%debug`, which will drop you into a `pdb` session. This will only work on the last traceback that occurred, so it must be called immediately, or else the exception may be clobbered by an additional exception.

```python
In [1]: def this_will_not_work():
    ...:     first = 'abc'
    ...:     second = 'def'
    ...:     third = first / second
    ...:     return third
    ...:

In [2]: this_will_not_work()
---------------------------------------------------------------------------
TypeError                                 Traceback (most recent call last)
<ipython-input-2-b68cb3b4fc7d> in <module>
----> 1 this_will_not_work()

<ipython-input-1-2389d0ae72e8> in this_will_not_work()
      2     first = 'abc'
      3     second = 'def'
----> 4     third = first / second
      5     return third

TypeError: unsupported operand type(s) for /: 'str' and 'str'

In [3]: %debug
> <ipython-input-1-2389d0ae72e8>(4)this_will_not_work()
      1 def this_will_not_work():
      2     first = 'abc'
      3     second = 'def'
----> 4     third = first / second
      5     return third

ipdb> first
'abc'
ipdb> second
'def'
```

You can have IPython do this automatically by setting the [`%pdb` magic](../config/pdb.md) in `ipython_config.py`.
