# Setup

Some slight assumptions are going to be made. I presume you own a computer, or at least have access to one. I am also going to assume it is of a Mac, Linux, or Windows variety. A further presumption is that you have Python 3 installed, a terminal program to access it, and the Python package installer,  `pip`.

If the above is not true, there are a few remedies:

* [Buy a computer](https://www.wikihow.com/Buy-a-New-Computer)
* [Figure out how to install Python](https://wiki.python.org/moin/BeginnersGuide/Download)
* [Select and install a terminal program](https://en.wikipedia.org/wiki/List_of_terminal_emulators)
* [Install pip](https://pip.pypa.io/en/stable/installing/)

I also highly suggest [using a virtual environment](https://docs.python.org/3/tutorial/venv.html) so you can keep your global Python installation nice and tidy, and can work in a separate environment that you can play around with and install different Python packages. This is a complex topic by itself, so for the remainder of this book, the assumption is that you are operating in such an environment. I use [virtualenv](https://virtualenv.pypa.io/en/latest/) and [virtualenvwrapper](https://virtualenvwrapper.readthedocs.io/en/latest/), but you should use whatever works for you.

Once you are ready, you can install IPython by running:

```
pip install ipython
```
We can test that IPython was successfully installed by entering:

```
ipython --version
```

<pre class="output">
7.18.1
</pre>
