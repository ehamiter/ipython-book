# system

<pre class="output">
%system:
    Shell execute - run shell command and capture output (!! is short-hand).
</pre>

`%system` has two aliases: `%sx` and `!!`.

To run a system command in IPython, like `ls`, you can put a single leading `!` in front of it, e.g.

```python
In [1]: !ls
LICENSE     README.md   book        book.toml   deploy.sh   src
```

Two leading `!!` is the short-hand for `%system` or `%sx`. The difference between using single or double exclamation points is that `!!` returns the results in a list that is split on `\n`, and since it is returned, it will be stored in the output history.

```python
In [2]: !!ls
Out[2]: ['LICENSE', 'README.md', 'book', 'book.toml', 'deploy.sh', 'src']
```
