# autoreload

<pre class="output">
%autoreload:
    %autoreload => Reload modules automatically
</pre>

`%autoreload` will automatically reload modules, so you can edit code in an IDE or text editor, and when a change is made and saved, you can test the new functionality in the IPython shell without having to exit and start a new session. This is incredibly helpful and saves a lot of time-- and it will work *most* of the time. [There are some caveats involved](https://ipython.org/ipython-doc/stable/config/extensions/autoreload.html#caveats), but some of the problems that prevent successful reloading are:

  * Changing a `@property` to a method or a method to a variable within a class
  * Functions that are removed from a module before it is reloaded are not upgraded
  * C extension modules cannot be reloaded

You can pass in a parameter to either disable reloading completely, only use imports that were specified with the command [`%aimport`](./aimport.md), or reload all modules every time before the code is executed.

Disable automatic reloading:
```python
%autoreload 0
```

Reload all modules imported with `%aimport` every time before executing
the Python code typed:
```python
%autoreload 1
```

Reload all modules (except those excluded by `%aimport`) every time
before executing the Python code typed:
```python
%autoreload 2
```
