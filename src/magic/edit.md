# edit

<pre class="output">
%edit:
    Bring up an editor and execute the resulting code.
</pre>

`%edit` (or `%ed` as an alias) runs IPython's edit hook. By default, it will call the editor specified by your environment variable `$EDITOR`, but this can be specificed in `ipython_config.py`’s [`editor`](../config/editor.md) setting.

This is nice if you want to edit a lengthy function or potentially save a snippet you've been working on to a file.

If it is called with no arguments, it will open up an empty editor and will execute the contents once you save and exit.

`%edit` also accepts arguments:

  * A filename, which will be loaded into the editor
  * A range of input history, e.g. `%edit 5 7 10-12`
  * A string variable
  * A function name
  * A [macro](./macro.md) name

An example of creating a function, the editing it in an external editor:

```python
In [1]: def brilliant_math_program(num):
    ...:     num += 1
    ...:     print(f'I increased your number to {num}')
    ...:

In [2]: brilliant_math_program(2)
I increased your number to 3

In [3]: %edit brilliant_math_program
Editing In[3]
IPython will make a temporary file named: /var/folders/qx/32hkz1f96yb557l4yd0_c6q80000gn/T/ipython_edit_6gzx7_2p/ipython_edit_s5u64by2.py
Editing... done. Executing edited code...
Out[3]: "def brilliant_math_program(num):\n    num = num * 2\n    print(f'I doubled your number to {num}')\n     \n"

In [4]: brilliant_math_program(2)
I doubled your number to 4
```
