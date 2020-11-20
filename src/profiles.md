# Profiles

IPython has support for multiple profiles. This is handy if you are working on different projects and want to tweak some behaviors, or test out new settings without changing how IPython will behave globally. By default, IPython will always run the `default` profile. Once you specify a new profile to create, new configuration files will be created. To create a new profile named `zagnut`, enter: <sup class="footnote-reference"><a href="#fn2" id="ref2">2</a></sup>

```
ipython profile create zagnut
```
<pre class="output">
[ProfileCreate] Generating default config file: '/Users/eric/.ipython/profile_zagnut/ipython_config.py'
</pre>

If at some point you forget where this configuration file was created, you can `locate` it:

```
ipython locate profile zagnut
```
<pre class="output">
/Users/eric/.ipython/profile_zagnut
</pre>

To launch IPython with this configuration, pass in the name to the `profile` argument:

```
ipython --profile=zagnut
```
<pre class="output">
Python 3.9.0 (default, Nov  2 2020, 18:14:37)
Type 'copyright', 'credits' or 'license' for more information
IPython 7.19.0 -- An enhanced Interactive Python. Type '?' for help.

IPython profile: zagnut

In [1]:
</pre>

To exit the shell, you can enter `exit` or use the keyboard shortcut `CTRL-D`.

If you are a Django developer and want to use an IPython profile in conjunction with the Django shell, you can do it by using the `django-extensions` package:

```
pip install django-extensions
```

It has a [`shell_plus`](https://django-extensions.readthedocs.io/en/latest/shell_plus.html) extension (which gives you some niceties like auto importing your models), and you can pass the profile name in as:

```
python manage.py shell_plus --ipython -- --profile=zagnut
```

> <i class="fa fa-fw fa-warning"></i> Note that there is a separate double dash (`--`) before the `--profile`.

Since this is kind of a long command to type each time you want to pop into a shell, I alias mine to something much simpler to remember: **P**ython **m**anage **s**hell_plus:

```
alias pms='python manage.py shell_plus --ipython -- --profile=zagnut'
```

---

<sup class="footnote-definition" id="fn2">2. We all remember [the candy bar of choice for Beetlejuice](https://www.youtube.com/watch?v=IwV90NvsmAI&t=0m20s), right? No? Just me?<a href="#ref2" title="Jump back to footnote 2 in the text.">↩</a></sup>
