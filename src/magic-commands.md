# Magic Commands

```
%magic
```
<pre class="output">
The magic function system provides a series of functions which allow you to
control the behavior of IPython itself, plus a lot of system-type
features.
</pre>

There are two kinds of magics: line and cell.

> Line magics are prefixed with the `%` character and work much like OS
command-line calls: they get as an argument the rest of the line, where
arguments are passed without parentheses or quotes.

> Cell magics are prefixed with a double `%%`, and they are functions that get as an argument not only the rest of the line, but also the lines below it in a
separate argument.  These magics are called with two arguments: the rest of the
call line and the body of the cell, consisting of the lines below the first.

Magic commands can be used *without* typing the `%` sign by default— this behavior is altered by running the magic command `%automagic`, which toggles the necessity of the preceding `%` character.

<i class="fa fa-fw fa-warning"></i> Keep in mind that if you create a variable that collides with an automagic command, using your variable (without the explicit `%` prefix) will override the magic command's reference, e.g.

<pre class="output">
In [1]: automagic

Automagic is OFF, % prefix IS needed for line magics.

In [2]: %automagic

Automagic is ON, % prefix IS NOT needed for line magics.

In [3]: automagic = print

In [4]: automagic
Out[4]: &lt;function print&gt;

In [5]: %automagic

Automagic is OFF, % prefix IS needed for line magics.
</pre>

You can view all available magic commands by running `%lsmagic`. Some of them will be recognizable as system commands and they behave as you might expect:

<pre class="output">
%alias  %cat  %cd  %clear  %less  %ls  %man  %mkdir  %more  %mv  %pip  %popd  %pushd  %pwd  %rm  %rmdir
</pre>

Let's look at some of the other commands that might be unfamiliar, and some examples of how you might use them.
