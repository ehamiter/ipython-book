# load

<pre class="output">
%load:
    Load code into the current frontend.
</pre>

`%load` lets you load in code from a filename, input history range, macro, an element in the user namespace, or even from a URL. It is very useful for taking a section of code from something like a GitHub repo and being able to load it directly into the shell so you can test it or use it.

If you feed in a large section of code, you can specify which lines you want by passing in the `r`ange parameter. Below is an example of loading a utility function from the `requests` library. It passes in the `import socket` on line 15, and then subsequently loads lines 641-650 for a function that determines if a passed-in string is an IPV4 address:

<pre class="output">
In [1]: %load -r 15,641-650 https://raw.githubusercontent.com/psf/requests/master/requests/utils.py

In [2]: # %load -r 15,641-650 https://raw.githubusercontent.com/psf/requests/master/requests/utils.py
    ...: import socket
    ...:
    ...:
    ...: def is_ipv4_address(string_ip):
    ...:     """
    ...:     :rtype: bool
    ...:     """
    ...:     try:
    ...:         socket.inet_aton(string_ip)
    ...:     except socket.error:
    ...:         return False
    ...:     return True
    ...:

In [3]: is_ipv4_address("192.168.0.1")
Out[3]: True

In [4]: is_ipv4_address("pizza-is-delicious")
Out[4]: False
</pre>
