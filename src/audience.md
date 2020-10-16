# Who this book is for

This is not a "learn how to program" book, nor is it geared toward data visualization or high performance processing that many may use Jupyter for. The audience in question are Python web developers who are comfortable with [object-oriented programming](https://en.wikipedia.org/wiki/Object-oriented_programming) in a command line environment.

If the following blurb looks familiar to you, you're in the right place:

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

If this leaves you slightly befuddled, the rest may be a bit hard to follow. You can learn more about [the shell and Python here](https://www.python.org/about/gettingstarted/).
