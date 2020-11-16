# Who this book is for

This is not a "learn how to program" book, nor is it geared toward data visualization or high performance processing that many may use Jupyter for. The audience in question are Python software developers who are comfortable with [object-oriented programming](https://en.wikipedia.org/wiki/Object-oriented_programming) in a command line environment.

If you're a Django or Flask developer that will run `python manage.py shell` or `flask shell` in order to examine objects and test out bits of code, you're in the right place. This should look familiar to you:

```python
>>> u = User.objects.filter(email__icontains='dev')

>>> len(u)
14

>>> first_dev = u[0]

>>> first_dev.is_staff
True

>>> first_dev.username
'samanthasmithdev'

>>> first_dev.email
'samanthasmithdev@techiecompany.com'
```


If this leaves you slightly befuddled, the rest may be a bit hard to follow. You can learn more about [Python and the shell here](https://www.python.org/about/gettingstarted/).
