# history

<pre class="output">
%history:
    Print input history, with most recent last.
</pre>

By default, `%history` (or its alias `%hist`) prints the input history without line numbers for ease in copying into an editor, so if you *do* want to see them, pass in `-n` to see them.

You can specify ranges to be returned, e.g.

```python
In [5]: %history -n 1 3-4
  1: a = 5
  3: d = 8
  4: e = 9
```
