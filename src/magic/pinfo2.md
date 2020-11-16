# pinfo2

<pre class="output">
%pinfo2:
    Provide extra detailed information about an object.
</pre>

`%pinfo2` is `%pinfo` taken one step further, and diving into the source code. Also similarly, `%pinfo2` is a synonym for `object??` or `??object`. Again, we examine the source code that actually makes `%pinfo2` tick:

```python
In [1]: pinfo2??
Source:
    @line_magic
    def pinfo2(self, parameter_s='', namespaces=None):
        """Provide extra detailed information about an object.

        '%pinfo2 object' is just a synonym for object?? or ??object."""
        self.shell._inspect('pinfo', parameter_s, detail_level=1,
                            namespaces=namespaces)
File:   ~/.virtualenvs/ipython-book/lib/python3.9/site-packages/IPython/core/magics/namespace.py
```

If you wondered what happens when you base64 encode a file, you can see for yourself:

```python
In [2]: import base64

In [3]: base64.encode??
Signature: base64.encode(input, output)
Source:
def encode(input, output):
    """Encode a file; input and output are binary files."""
    while True:
        s = input.read(MAXBINSIZE)
        if not s:
            break
        while len(s) < MAXBINSIZE:
            ns = input.read(MAXBINSIZE-len(s))
            if not ns:
                break
            s += ns
        line = binascii.b2a_base64(s)
        output.write(line)
File:      ~/.pyenv/versions/3.9.0/lib/python3.9/base64.py
Type:      function
```