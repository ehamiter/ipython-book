# xdel

<pre class="output">
%xdel:
    Delete a variable, trying to clear it from anywhere that
    IPython's machinery has references to it. By default, this uses
    the identity of the named object in the user namespace to remove
    references held under other names. The object is also removed
    from the output history.
</pre>

```python
In [1]: animal = 'porcupine'

In [2]: animal
Out[2]: 'porcupine'

In [3]: %xdel animal

In [4]: animal
NameError: name 'animal' is not defined
```
