# script

<pre class="output">
%%script:
    Run a cell via a shell command

    The `%%script` line is like the #! line of script,
    specifying a program (bash, perl, ruby, etc.) with which to run.

    The rest of the cell is run by that program.
</pre>

`%%script` is a cell magic that can be used to run scripts other than Python in your shell, like Bash, Perl, Ruby, or different versions of Python.

Each language has a shortcut, so `%%ruby` is the equivalent of `%%script ruby`, `%%bash` is the equivalent of `%%script bash`, etc.

```python
In [1]: %%script bash
    ...: for i in 1 2 3; do
    ...:   echo $i
    ...: done
    ...:
    ...:
1
2
3
```

```python
In [2]: %%ruby
    ...: things = %w( granite snails calcium pie )
    ...: puts things
    ...:
    ...:
granite
snails
calcium
pie
```

```python
In [3]: %%perl
    ...: not exp log srand xor s qq qx xor
    ...: s x x length uc ord and print chr
    ...: ord for qw q join use sub tied qx
    ...: xor eval xor print qq q q xor int
    ...: eval lc q m cos and print chr ord
    ...: for qw y abs ne open tied hex exp
    ...: ref y m xor scalar srand print qq
    ...: q q xor int eval lc qq y sqrt cos
    ...: and print chr ord for qw x printf
    ...: each return local x y or print qq
    ...: s s and eval q s undef or oct xor
    ...: time xor ref print chr int ord lc
    ...: foreach qw y hex alarm chdir kill
    ...: exec return y s gt sin sort split
    ...:
    ...:
just another perl hacker
```