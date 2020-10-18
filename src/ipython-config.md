# ipython_config.py

Once you have created your profile, open up its configuration file in your favorite text editor:

```
ipython locate profile zagnut
```

<pre class="output">
/Users/eric/.ipython/profile_zagnut
</pre>

```
"${EDITOR:-vi}" ~/.ipython/profile_zagnut/ipython_config.py
```

This file is over 1,000 lines of code, so there's a lot to take in— we'll focus on a handful of things that are practical and help tailor your IPython experience. After we've explored the settings in this chapter, I encourage you to dive deep into the file for other settings. Experiment with logging, interacting with `matplotlib`, `numpy`, and [Jedi integration](https://jedi.readthedocs.io/en/latest/) if those are in your wheelhouse.