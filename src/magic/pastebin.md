# pastebin

<pre class="output">
%pastebin:
    Upload code to dpaste's paste bin, returning the URL.
</pre>

Sharing code with a collaborator can be tricky sometimes– formatting in e-mails can be hit or miss, Slack has pretty good support, but if it's a free account, then the history gets erased after a couple of days. Pastebin sites are usually a good way to do this, but it can still be a pain to copy and paste using the correct indentation and erasing all of the `In` and `Out` prompts. 

`%pastebin` allows you to upload a history range, filename, string, or macro to [dpaste.com](https://dpaste.com), which is a publicly-accessible pastebin site. The snippet that you upload is shareable through a unique link, and expires after 7 days.

By default, the title is "Pasted from IPython" but you can set the description with `-d`:

```python
In [1]: import codecs

In [2]: def my_secret_translator(message):
    ...:     coded_message = codecs.encode(message, 'rot_13')
    ...:     print(coded_message)
    ...:

In [3]: my_secret_translator('My cat meows at midnight')
Zl png zrbjf ng zvqavtug

In [4]: my_secret_translator('Zl png zrbjf ng zvqavtug')
My cat meows at midnight

In [5]: %pastebin -d 'I learned this in "IPython for Web Devs"!' 1-2
Out[5]: 'http://dpaste.com/CVQQQLVKX'
```
