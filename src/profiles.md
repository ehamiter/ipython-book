# Profiles

IPython has support for multiple profiles. This is handy if you are working on different projects and want to tweak some behaviors, or test out new settings without changing how IPython will behave globally. By default, IPython will always run the `default` profile. Once you specify a new profile to create, new configuration files will be created. To create a new profile named `zagnut`, enter: <sup><a href="#fn1" id="ref1">1</a></sup>

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
Python 3.8.2 (default, Jul  5 2020, 15:01:50)
Type 'copyright', 'credits' or 'license' for more information
IPython 7.18.1 -- An enhanced Interactive Python. Type '?' for help.

IPython profile: zagnut

In [1]:
</pre>

---

<sup id="fn1">1. We all remember [the candy bar of choice for Beetlejuice](https://www.youtube.com/watch?v=IwV90NvsmAI&t=0m20s), right? No? Just me?<a href="#ref1" title="Jump back to footnote 1 in the text.">↩</a></sup>
