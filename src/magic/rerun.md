# rerun

<pre class="output">
%rerun:
    Re-run previous input
</pre>

You can repeat the last line by passing `%rerun` with no arguments, or pass in a line or line range from history.

```python
In [1]: class Person:
    ...:     def __init__(self, name, age, email):
    ...:         self.name = name
    ...:         self.age = age
    ...:         self.email = email
    ...:

In [2]: p1 = Person('Zoe', 45, 'zoe@anemailaddress.com')

In [3]: p1.age = 57

In [4]: p1.age
Out[4]: 57

In [5]: rerun 2
=== Executing: ===
p1 = Person('Zoe', 45, 'zoe@anemailaddress.com')
=== Output: ===

In [6]: p1.age
Out[6]: 45
```
