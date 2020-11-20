# save

<pre class="output">
%save:
    Save a set of lines or a macro to a given filename.
</pre>

After you have tested and tweaked a few lines in the shell, and would benefit from having the code around permananetly, you can `%save` a set of lines or a macro to a filename.

The default syntax is `%save filename [lines]`:

```python
In [1]: def ends_in_za(word):
   ...:     if word.endswith('za'):
   ...:         print('It ends in za!')
   ...:     else:
   ...:         print('It does not end in za.')
   ...:

In [2]: ends_in_za('pizza')
It ends in za!

In [3]: ends_in_za('asparagus')
It does not end in za.

In [4]: %save ends_in_za 1
The following commands were written to file `ends_in_za.py`:
def ends_in_za(word):
    if word.endswith('za'):
        print('It ends in za!')
    else:
        print('It does not end in za.')
```

There are a few options you can pass in directly after `%save`:

<pre class="output">
-r: use 'raw' input.  By default, the 'processed' history is used,
so that magics are loaded in their transformed version to valid
Python.  If this option is given, the raw input as typed as the
command line is used instead.

-f: force overwrite.  If file exists, %save will prompt for overwrite
unless -f is given.

-a: append to the file instead of overwriting it.
</pre>
