# env

<pre class="output">
%env:
    Get, set, or list environment variables.
</pre>

If you need access to an environment variable and can't remember what it was, you can recall it easily using `%env`. You can list all of them by passing the command by itself, or recall specific ones like `%env variable`, or set them like `%env variable new_value`.

```python
In [1]: %env foo
UsageError: Environment does not have key: foo

In [2]: %env foo bar
env: foo=bar

In [3]: %env foo
Out[3]: 'bar'
```
