# InteractiveShellApp.exec_lines

<pre class="output">
## lines of code to run at IPython startup.
#  Default: []
</pre>

`InteractiveShellApp.exec_lines` is a list that will execute on IPython's startup. You could put in
```
c.InteractiveShellApp.exec_lines.append('import this')
```
if you wanted to see The Zen of Python everytime you fired up the shell. That might not be totally practical, but it could be inspiring. An extension that we will talk more about later is the `autoreload` extension. It's pretty nice to have this available without having to manually load it— it lets you change source code in an editor while the shell is still open, and it will reload its value without requiring you to have to restart your session. <sup><a href="#fn1" id="ref1">1</a></sup>

You can enable it to run by default with these lines:
```
c.InteractiveShellApp.exec_lines = []
c.InteractiveShellApp.exec_lines.append('%load_ext autoreload')
c.InteractiveShellApp.exec_lines.append('%autoreload 2')    
```

---

<sup id="fn1">1. As with anything seemingly too good to be true, [it does have its caveats](https://ipython.org/ipython-doc/stable/config/extensions/autoreload.html#caveats) and doesn't work for every case. It works most of the time, though, and can save you a lot of time.<a href="#ref1" title="Jump back to footnote 1 in the text.">↩</a></sup>