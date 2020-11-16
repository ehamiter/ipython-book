# aimport

<pre class="output">
%aimport:
    %aimport => Import modules for automatic reloading.
</pre>

`%aimport` lets you specify a module to import that will automatically be reloaded. This command works alongside [`%autoreload`](./autoreload.md), which lets you specify the frequency or inclusion of what modules will be autoreloaded.

List modules to automatically import and not to import:
```python
%aimport
```

Import module 'foo' and mark it to be autoreloaded for `%autoreload 1`:
```python
%aimport foo
```

Import modules 'foo', 'bar' and mark them to be autoreloaded for `%autoreload 1`:
```python
%aimport foo, bar
```

Mark module 'foo' to not be autoreloaded for `%autoreload 1`:
```python
%aimport -foo
```
