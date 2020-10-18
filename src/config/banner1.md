# InteractiveShellApp.banner1

<pre class="output">
## The part of the banner to be printed before the profile
#  Default: "Python 3.8.2 (default, Jul  5 2020, 15:01:50) \nType 'copyright', 'credits' or 'license' for more information\nIPython 7.18.1 -- An enhanced Interactive Python. Type '?' for help.\n"
</pre>

You can customize the banner that is displayed on startup-- if you're the kind of person who's into that kind of thing. You could cut it down to the important bits if you *are* into the whole brevity thing: <sup class="footnote-reference"><a href="#fn3" id="ref3">3</a></sup>

```
c.InteractiveShell.banner1 = "Python 3.8.2 -- IPython 7.18.1\n"
```
…or eliminate it entirely:
```
c.TerminalIPythonApp.display_banner = False
```

---

<sup class="footnote-definition" id="fn3">3. [Yeah? Well, you know, that's just like, uh… your opinion, man. ](https://www.youtube.com/watch?v=pWdd6_ZxX8c)<a href="#ref3" title="Jump back to footnote 3 in the text.">↩</a></sup>
