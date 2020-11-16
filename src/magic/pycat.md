# pycat

<pre class="output">
%pycat:
    Show a syntax-highlighted file through a pager.
</pre>

`%pycat` is very similar to the `cat` utility, which will read a file and write them to standard output, but additionally assumes the file is written in Ptthon, and will show it with syntax highlighting. The command can take a local filename, a URL, a [`%history`](./history.md) range, or a [`%macro`](./macro.md).

```python
%pycat my_file.py
```

```python
%pycat https://raw.githubusercontent.com/ehamiter/pindead/master/pindead.py
```

```python
%pycat 16-23
```

```python
%pycat my_macro
```
