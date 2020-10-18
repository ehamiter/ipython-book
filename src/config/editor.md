# editor

<pre class="output">
## Set the editor used by IPython (default to $EDITOR/vi/notepad).
#  Default: 'subl'
</pre>

The default listed above is `subl` for me because I use Sublime Text as my default editor. For you, it may be `vim`, `vscode`, `emacs`, `nano`, or any number of text editors. For my particular case, as we will explore later, there is an `%edit` magic command in IPython, which lets you …well, edit things. For whatever reason, Sublime Text does not work well with the `%edit` command. <sup class="footnote-reference"><a href="#fn4" id="ref4">4</a></sup>Because of this, I want to set IPython's editor of choice to something else– `vim`, in my case: <sup class="footnote-reference"><a class="superscript" href="#fn5" id="ref5">5</a></sup>

```
c.TerminalInteractiveShell.editor = 'vim'
```

---

<sup class="footnote-definition" id="fn4">4. Once `%edit` is invoked, a temporary file is created. In Sublime's case, it immediately executes the code instead of waiting for the save signal to execute it, so there is never a chance of actually editing the file. <a href="#ref4" title="Jump back to footnote 4 in the text.">↩</a></sup><br>
<sup class="footnote-definition" id="fn5">5. A thousand apologies if I angered any Emacs wizards. I use Vim here because I know the basics, and watching me try to use Emacs is just an embarrassing spectacle that no one should have to witness.<a href="#ref5" title="Jump back to footnote 5 in the text.">↩</a></sup>
