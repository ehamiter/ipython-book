# confirm_exit

<pre class="output">
## Set to confirm when you try to exit IPython with an EOF (Control-D in Unix,
#  Control-Z/Enter in Windows). By typing 'exit' or 'quit', you can force a
#  direct exit without any confirmation.
#  Default: True
</pre>

Whenever I quit an IPython session, I'm asked if I really want to quit. I do. Eventually I figured out that you don't actually have to enter `y` for yes, though— you can just hit `return` and it will allow you to quit. There's a better way, though, which saves you an additional key stroke. Setting this value to `False` will let you exit immediately.

```
c.TerminalInteractiveShell.confirm_exit = False
```
