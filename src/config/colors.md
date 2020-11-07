# InteractiveShell.colors

<pre class="output">
## Set the color scheme (NoColor, Neutral, Linux, or LightBG).
#  Choices: any of ['Neutral', 'NoColor', 'LightBG', 'Linux'] (case-insensitive)
#  Default: 'Neutral'
</pre>

You can select from a few color schemes— I use a dark background for my terminal so the default `Neutral` works for me, but try out `LightBG` if you use a light background color, or `Linux` if you're really into Linux, or `NoColor` if you hate rainbows and happiness.

```python
c.InteractiveShell.colors = 'LightBG'
```

You can also change this on-the-fly in the shell by invoking the magic command `%colors`:

```python
%colors Linux
```
