# TerminalInteractiveShell.autoformatter

<pre class="output">
## Autoformatter to reformat Terminal code. Can be `'black'` or `None`
#  Default: None
</pre>

`black` is [the uncompromising Python code formatter](https://github.com/psf/black). It can make collaboration on a project consistent— no matter the style of the coder, `black` will format the code to its specifications, so everything is nice and tidy.

```python
c.TerminalInteractiveShell.autoformatter = 'black'
```

Enabling this can turn something like this:

```python
In [1]: cost = {
    ...: 'apple': 0.40,
    ...: 'banana': 0.50}
    ...: bought = {
    ...:     'apple': 1,
    ...:     'banana': 6}
    ...: bill = sum(
    ...: cost[fruit] * bought[fruit]
    ...:                    for fruit in bought
    ...:                    )
    ...: print(
    ...: 'I owe the grocer $%.2f' % bill
    ...: )
I owe the grocer $3.40
```

…into this:

```python
In [1]: cost = {"apple": 0.40, "banana": 0.50}
    ...: bought = {"apple": 1, "banana": 6}
    ...: bill = sum(cost[fruit] * bought[fruit] for fruit in bought)
    ...: print("I owe the grocer $%.2f" % bill)
I owe the grocer $3.40
```

It's very handy for cleaning up your code style, especially if the project you're working on uses `black`. In order for this to work, you need to have `black` installed in your environment:

```
pip install black
```

Once caveat that I have found is that if you *do* set the autoformatter to `black`, sometimes it will try and format things that aren't necessarily code. To be specific, there is a magic command [`%history`](../magic/history.md), or its alias `%hist`. You use this to list the history of your IPython session's inputs, and by default it lists them without a corresponding number beside each entry. If you *do* want to see a numbered list, you need to pass in the parameter `n`. So, it should look like this:

```python
%history -n
```

…but `black` reformats that, which turns it into

```python
%history - n
```

…which isn't an actual command, so you don't see the numbers beside each line. So, this is something you should be aware of.
