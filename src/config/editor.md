# editor

<pre class="output">
## Set the editor used by IPython (default to $EDITOR/vi/notepad).
#  Default: 'subl'
</pre>

The default listed above is `subl` for me because I use Sublime Text as my default editor. For you, it may be `vim`, `vscode`, `emacs`, `nano`, or any number of text editors. For my particular case, as we will explore later, there is an `edit` command in IPython, which lets you …well, edit things. For whatever reason, Sublime Text does not work well with the `edit` command. <sup><a href="#fn3" id="ref3">3</a></sup> Because of this, I want to set IPython's editor of choice to something else– `vim`, in my case:

```
c.TerminalInteractiveShell.editor = 'vim'
```

---

<sup id="fn3">3. Once `edit` is invoked, a temporary file is created. In Sublime's case, it immediately executes the code instead of waiting for the save signal to execute it, so there is never a chance of actually editing the file. <a href="#ref3" title="Jump back to footnote 3 in the text.">↩</a></sup>
