# bookmark

<pre class="output">
%bookmark:
    Manage IPython's bookmark system.
</pre>

Setting bookmarks is very handy if you find yourself changing directories within a project, or even outside a project and would like to be have faster access to often-used directories.

<pre class="output">
%bookmark &lt;name&gt;       - set bookmark to current dir
%bookmark &lt;name&gt; &lt;dir&gt; - set bookmark to &lt;dir&gt;
%bookmark -l           - list all bookmarks
%bookmark -d &lt;name&gt;    - remove bookmark
%bookmark -r           - remove all bookmarks
</pre>

Here's an example that shows setting a bookmark to the current directory, navigating to the user's home directory, then coming back to the project:

```python
In [1]: %pwd
Out[1]: '/Users/eric/projects/ipython-book'

In [2]: %bookmark book

In [3]: %bookmark -l
Current bookmarks:
book -> /Users/eric/projects/ipython-book

In [4]: %cd ~
/Users/eric

In [5]: %pwd
Out[5]: '/Users/eric'

In [6]: %cd -b book
(bookmark:book) -> /Users/eric/projects/ipython-book
/Users/eric/projects/ipython-book

In [7]: %pwd
Out[7]: '/Users/eric/projects/ipython-book'
```

You can also omit the `-b` after the `%cd` command if there's no directory with the name of your bookmark. The bookmarks are associated with each profile and persist through IPython sessions.
