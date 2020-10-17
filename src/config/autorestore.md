# autorestore

<pre class="output">
## If True, any %store-d variables will be automatically restored when IPython
#  starts.
#  Default: False
</pre>

`%store` is a "magic" command that we will discuss in just a bit— for the context needed for the `autorestore` setting, this allows you to store variables, aliases, and macros in IPython's database during a session, then after exiting that session, having those values be retrieved automatically upon entering a new session.

```
c.StoreMagics.autorestore = True
```