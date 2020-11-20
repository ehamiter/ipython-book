# store

<pre class="output">
%store:
    Lightweight persistence for python variables.
</pre>

`%store` allows you to save a variable and access it after exiting a session. To save a variable, you simply pass it as the sole argument:

```python
In [1]: my_name = 'Eric'

In [2]: %store my_name
Stored 'my_name' (str)
```

You can then exit the session, enter a new one, and recall it with the `-r` parameter:

```python
In [3]: exit
```

```
ipython --profile=zagnut
```

```python
In [1]: my_name
Out[1]: NameError: name 'my_name' is not defined

In [2]: %store -r

In [3]: my_name
Out[3]: 'Eric'
```

You can edit your IPython configuration to [always autoload any stored variables](../config/autorestore.md).

## Additional options

Show a list of all variables and their current values:

```python
%store
```

Store the *current* value of the variables `eggs` and `motorcycles`:

```python
%store eggs motorcycles
```

Remove the variable `eggs` and its value from storage:

```python
%store -d eggs
```

Remove all variables from storage:

```python
%store -z
```

> <i class="fa fa-fw fa-warning"></i> It should be noted that if you change the value of a variable, you need to `%store` it again if you want to persist the new value.
