# InteractiveShellApp.exec_lines

<pre class="output">
## lines of code to run at IPython startup.
#  Default: []
</pre>

`InteractiveShellApp.exec_lines` is a list that will execute on IPython's startup. If you wanted to see *The Zen of Python* by Tim Peters everytime you fired up the shell, you could put in:

```python
c.InteractiveShellApp.exec_lines = ['import this']
```

That might not be totally practical, but it could be inspiring. An extension that we will talk more about later is the [`autoreload`](../magic/autoreload.md) extension. It's pretty nice to have this available without having to manually load it— it lets you change source code in an editor while the shell is still open, and it will reload its value without requiring you to have to restart your session. <sup class="footnote-reference"><a href="#fn6" id="ref6">6</a></sup>

You can enable it to run by default with these lines:

```python
c.InteractiveShellApp.exec_lines = []
c.InteractiveShellApp.exec_lines.append('%load_ext autoreload')
c.InteractiveShellApp.exec_lines.append('%autoreload 2')    
```

---

<sup class="footnote-definition" id="fn6">6. As with anything seemingly too good to be true, [it does have its caveats](https://ipython.org/ipython-doc/stable/config/extensions/autoreload.html#caveats) and doesn't work for every case. It works more often than not, though, and can save you a lot of time.<a href="#ref6" title="Jump back to footnote 6 in the text.">↩</a></sup>
