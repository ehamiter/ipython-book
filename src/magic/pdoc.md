# pdoc

<pre class="output">
%pdoc:
    Print the docstring for an object.
</pre>

`%pdoc` will print out the object's docstring, or if it is a class, it will print both the class and constructor docstrings.

```python
In [1]: from textwrap import dedent

In [2]: %pdoc dedent
Class docstring:
    Remove any common leading whitespace from every line in `text`.

    This can be used to make triple-quoted strings line up with the left
    edge of the display, while still presenting them in the source code
    in indented form.

    Note that tabs and spaces are both treated as whitespace, but they
    are not equal: the lines "  hello" and "\thello" are
    considered to have no common leading whitespace.

    Entirely blank lines are normalized to a newline character.
Call docstring:
    Call self as a function.
```
