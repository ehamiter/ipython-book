# psearch

<pre class="output">
%psearch:
    Search for object in namespaces by wildcard.
</pre>

`%psearch` lets you search for objects in namespaces, both built-in objects like `dict`, as well as any user-created objects in the session.

`?` can be used as a synonym at the beginning or end for `%psearch`, if used with `*` as a wildcard. For example:

```python
In [1]: a*?
abs
all
any
ascii
```

You can pass in `-i` to make it a case-insensitive search:
```python
In [2]: %psearch -i a*
ArithmeticError
AssertionError
AttributeError
abs
all
any
ascii
```

To list all available object types for object matching, pass in `-l`:

```python
In [3]: %psearch -l
asyncgenerator
builtinfunction
builtinmethod
cell
classmethoddescriptor
code
coroutine
frame
function
generator
getsetdescriptor
lambda
mappingproxy
memberdescriptor
method
methoddescriptor
methodwrapper
module
traceback
wrapperdescriptor
```
