# pprint

<pre class="output">
%pprint:
    Toggle pretty printing on/off.
</pre>

Pretty printing is on by default, but you can toggle it off and on with `%pprint`:

```python
In [1]: s = {
     ...:     'a': [1,2,3,4,5,6,7,8,9,10],
     ...:     'b': {1:2, 2:3, 3:4, 4:5, 5:6, 6:7, 7:8, 8:9, 9:10},
     ...:     'c': (1,2,3,4,5,6,7,8,9,10)
     ...: }
     ...:

In [2]: %pprint
Pretty printing has been turned OFF

In [3]: s
Out[3]: {'a': [1, 2, 3, 4, 5, 6, 7, 8, 9, 10], 'b': {1: 2, 2: 3, 3: 4, 4: 5, 5: 6, 6: 7, 7: 8, 8: 9, 9: 10}, 'c': (1, 2, 3, 4, 5, 6, 7, 8, 9, 10)}

In [4]: %pprint
Pretty printing has been turned ON

In [5]: s
Out[5]:
{'a': [1, 2, 3, 4, 5, 6, 7, 8, 9, 10],
 'b': {1: 2, 2: 3, 3: 4, 4: 5, 5: 6, 6: 7, 7: 8, 8: 9, 9: 10},
 'c': (1, 2, 3, 4, 5, 6, 7, 8, 9, 10)}
```

