# reset

<pre class="output">
%reset:
    Resets the namespace by removing all names defined by the user, if
    called without arguments, or by removing some types of objects, such
    as everything currently in IPython's In[] and Out[] containers.
</pre>

You can `%reset` all assigned variables in your session without confirmation by passing in the `-f` parameter:

```python
%reset -f
```

Keep in mind this will also delete your [`%history`](./history.md). To preserve your history, you can pass in `-s` for a "soft" reset:

```python
%reset -s
```

You can also reset just the input or output history or directory history:

```python
%reset in
```
```python
%reset out
```
```python
%reset dhist
```
