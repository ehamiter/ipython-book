# InteractiveShell.pdb

<pre class="output">
## Automatically call the pdb debugger after every exception.
#  Default: False
</pre>

The [Python debugger](https://docs.python.org/3/library/pdb.html) can be a super useful tool for stepping through code and examining what's going on. Normally to use it, you import it and then set the trace:

```python
import pdb; pdb.set_trace()
```

Things got a little more simple with the advent of [PEP 553](https://www.python.org/dev/peps/pep-0553/) which introduced `breakpoint()` to Python 3.7. You can accomplish the above with simply:

```python
breakpoint()
```

To invoke this automatically in your shell if you hit an exception, you can set it like so:

```python
c.InteractiveShell.pdb = True
```

Now, whenever your code hits an exception, you will automatically be dropped into the debugger.

