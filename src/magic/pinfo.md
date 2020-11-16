# pinfo

<pre class="output">
%pinfo:
    Provide detailed information about an object.
</pre>

`%pinfo` is a synonym for `object?` or `?object`, which prints out detailed information about an object. This is an incredibly useful feature that lets you examine objects, including magic commands. We can get information about `%pinfo` itself, inception-style:

```python
In [1]: %pinfo?
Docstring:
Provide detailed information about an object.

'%pinfo object' is just a synonym for object? or ?object.
File:      ~/.virtualenvs/ipython-book/lib/python3.9/site-packages/IPython/core/magics/namespace.py
```

Off the top of your head, do you know all of the parameters for `timedelta`? If not, this is a great way to show them along with some other helpful information:

```python
In [2]: from datetime import timedelta

In [3]: timedelta?
Init signature: timedelta(self, /, *args, **kwargs)
Docstring:
Difference between two datetime values.

timedelta(days=0, seconds=0, microseconds=0, milliseconds=0, minutes=0, hours=0, weeks=0)

All arguments are optional and default to 0.
Arguments may be integers or floats, and may be positive or negative.
File:           ~/.pyenv/versions/3.9.0/lib/python3.9/datetime.py
Type:           type
Subclasses:
```