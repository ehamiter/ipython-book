# highlighting_style

<pre class="output">
## The name or class of a Pygments style to use for syntax highlighting. To see
#  available styles, run `pygmentize -L styles`.
#  Default: traitlets.Undefined
</pre>


[Pygments](https://pygments.org/) is a generic syntax highlighter used to prettify source code. You can set your style of choice by entering:

```
c.TerminalInteractiveShell.highlighting_style = 'monokai'
```

It is dependent on the `Pygments` library, which can be installed via:

```
pip install Pygments
```

You can view all of the available styles (below is a sample of the complete output):
```
pygmentize -L styles
```

<pre class="output">
* emacs:
    The default style (inspired by Emacs 22).
* monokai:
    This style mimics the Monokai color scheme.
* vim:
    Styles somewhat like vim 7.0
* xcode:
    Style similar to the Xcode default colouring theme.
* solarized-dark:
    The solarized style, dark.
* solarized-light:
    The solarized style, light.
</pre>
