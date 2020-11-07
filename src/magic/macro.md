# macro

<pre class="output">
%macro:
    Define a macro for future re-execution. It accepts ranges of history,
    filenames or string objects.
</pre>

`%macro` is a great way of storing code snippets into a bundle that can be re-used for future use. 

An example:

```python
In [1]: a = 10

In [2]: b = 2

In [3]: c = a * b

In [4]: print(c)
20

In [5]: %macro abc 1-4
Macro `abc` created. To execute, type its name (without quotes).
=== Macro contents: ===
a = 10
b = 2
c = a * b
print(c)

In [6]: abc
20
```


You can view a macro's contents by explicitly printing it:

```python
print(macro_name)
```

```python
In [7]: print(abc)
a = 10
b = 2
c = a * b
print(c)
```
