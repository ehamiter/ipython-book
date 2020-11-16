# pdef

<pre class="output">
%pdef:
    Print the call signature for any callable object.
</pre>

`%pdef` prints a call signature for an object, or if the object is a class, it will print the constructor information. This is an easy way to see what parameters may or may not be required when creating or updating an object.

```python
In [1]: import calendar

In [2]: %pdef calendar.TextCalendar
Class constructor information:
 calendar.TextCalendar(firstweekday=0)

In [3]: import hashlib

In [4]: %pdef hashlib.md5
 hashlib.md5(string=b'', *, usedforsecurity=True)
```
