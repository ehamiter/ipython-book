# pdb

<pre class="output">
%pdb:
    Control the automatic calling of the pdb interactive debugger.
</pre>

Just as you can set [`pdb`](../config/pdb.md) to trigger on an exception in the `ipython_config.py` file, you can set it directly with the magic command `%pdb`.

It accepts "truthy" (`%pdb on` or `%pdb 1`) or "falsey" (`%pdb off` or `%pdb 0`) values, and if called without the argument it works as a toggle.

If you want to just activate the debugger after an exception has fired,
without having to type `%pdb on` and rerunning your code, you can use
the [`%debug`](./debug.md) magic.
