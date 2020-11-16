# paste

<pre class="output">
%paste:
    Paste & execute a pre-formatted code block from clipboard.
</pre>

Similar to [`%cpaste`](./cpaste.md), `%paste` allows you to paste a copied block of text properly into the shell, and it automatically handles any indentation differences, and ignores the `>` and `+` characters that may be present in e-mails, diffs, doctests, or code samples.

Unlike `%cpaste`, once you execute `%paste`, it automatically pastes and executes the block, so there is no further editing involved. It *does* however assign a variable to the pasted block, which is aptly named `pasted_block`, so you can then later edit it, e.g. `%edit pasted_block`. You can override this variable name by passing in a variable name directly:

```python
%paste my_cool_code
```
