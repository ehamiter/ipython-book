# InteractiveShellApp.banner1

<pre class="output">
## The part of the banner to be printed before the profile
#  Default: "Python 3.9.0 (default, Nov  2 2020, 18:14:37) \nType 'copyright', 'credits' or 'license' for more information\nIPython 7.19.0 -- An enhanced Interactive Python. Type '?' for help.\n"
</pre>

You can customize the banner that is displayed on startup-- if you're the kind of person who likes to tweak every customizable aspect of a system. You could cut it down to the important bits if you *are* into the whole brevity thing: <sup class="footnote-reference"><a href="#fn3" id="ref3">3</a></sup>

```python
c.InteractiveShell.banner1 = "Python 3.9.0 -- IPython 7.19.0\n"
```
…or eliminate it entirely:
```python
c.TerminalIPythonApp.display_banner = False
```

---

<sup class="footnote-definition" id="fn3">3. [Yeah? Well, you know, that's just like, uh… your opinion, man. ](https://www.youtube.com/watch?v=pWdd6_ZxX8c)<a href="#ref3" title="Jump back to footnote 3 in the text.">↩</a></sup>
