# who

<pre class="output">
%who:
    Print all interactive variables, with some minimal formatting.
</pre>

`%who` is a nice way of looking at all of the variables you have created or assigned:

```python
In [1]: class Automobile:
   ...:     def __init__(self, name, color, doors):
   ...:         self.name = name
   ...:         self.color = color
   ...:         self.doors = doors
   ...:

In [2]: a = Automobile('Family Truckster', 'green', 4)

In [3]: s = 'this is some string'

In [4]: i = 54447877

In [5]: f = 45.99

In [6]: d = {'a': 'dict'}

In [7]: t = ('a', 'tuple')

In [8]: %who
Automobile   a   d   f   i   s   t
```

You can also filter by types, e.g. `str`, `int`, et cetera:

```python
In [9]: %who str
s
```

To get a more detailed view of assigned variables, you can use [`%whos`](./whos.md).
