# cpaste

<pre class="output">
%cpaste:
    Paste & execute a pre-formatted code block from clipboard.
</pre>

`%cpaste` and [`%paste`](./paste.md) are pretty similar— they allow you to copy a block of code from somewhere outside of the shell and paste it in without having to tweak the indentation or removal of common Python snippet characters, like `>` or `+` that are common in e-mails, diff files, and doctests.

The primary difference is that `%cpaste` allows you to paste in your snippet, and then continue to add more or edit what you pasted before it's executed. You have to terminate your block with either two minus signs (`--`) or `CTRL-D` alone on an empty line.

```python
In [1]: %cpaste
Pasting code; enter '--' alone on the line to stop.
:>>> a = ["world!", "Hello"]
:>>> print " ".join(sorted(a))
:--
Hello world!
```
