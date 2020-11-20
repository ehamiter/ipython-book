# whos

<pre class="output">
%whos:
    Like %who, but gives some extra information about each variable.
</pre>

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

In [8]: %whos
Variable   Type       Data/Info
-------------------------------
Automobile type       <class '__main__.Automobile'>
s          str        this is some string
i          int        54447877
f          float      45.99
d          dict       n=1
t          tuple      n=2
a          Automobile <__main__.Automobile object at 0x104a0bd30>
```

Like [`%who`](./who.md), you can filter by type:

```python
In [9]: %whos dict
Variable   Type    Data/Info
----------------------------
d          dict    n=1
```
