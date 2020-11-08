# magic

<pre class="output">
%magic
    Print information about the magic function system.
</pre>

Think of `%magic` as the user's guide to magic commands. It steps through all of the commands listed in [`%lsmagic`](./lsmagic.md) with extensive examples and all available parameters.

It supports three optional display parameters: `-latex`, `-brief`, and `-rest`. Here's an example of the results for the first entry, [`aimport`](./aimport.md):

```
%magic
```

<pre class="output">
%aimport:
    %aimport => Import modules for automatic reloading.

    %aimport
    List modules to automatically import and not to import.

    %aimport foo
    Import module 'foo' and mark it to be autoreloaded for %autoreload 1

    %aimport foo, bar
    Import modules 'foo', 'bar' and mark them to be autoreloaded for %autoreload 1

    %aimport -foo
    Mark module 'foo' to not be autoreloaded for %autoreload 1
</pre>

```
%magic -latex
```

<pre class="output">
\bigskip
\texttt{\textbf{ \%aimport}}:
    \texttt{\%aimport} => Import modules for automatic reloading.

    \texttt{\%aimport}
    List modules to automatically import and not to import.

    \texttt{\%aimport} foo
    Import module 'foo' and mark it to be autoreloaded for \texttt{\%autoreload} 1

    \texttt{\%aimport} foo, bar
    Import modules 'foo', 'bar' and mark them to be autoreloaded for \texttt{\%autoreload} 1

    \texttt{\%aimport} -foo
    Mark module 'foo' to not be autoreloaded for \texttt{\%autoreload} 1
</pre>

```
%magic -brief
```

<pre class="output">
%aimport:
    %aimport => Import modules for automatic reloading.
</pre>

```
magic -rest
```

<pre class="output">
**%aimport**::

    %aimport => Import modules for automatic reloading.

    %aimport
    List modules to automatically import and not to import.

    %aimport foo
    Import module 'foo' and mark it to be autoreloaded for %autoreload 1

    %aimport foo, bar
    Import modules 'foo', 'bar' and mark them to be autoreloaded for %autoreload 1

    %aimport -foo
    Mark module 'foo' to not be autoreloaded for %autoreload 1
</pre>
