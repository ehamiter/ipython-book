# Custom magic commands

Along with the standard magic commands IPython provides, [you can create custom magic commands](https://ipython.readthedocs.io/en/stable/config/custommagics.html) that can be useful. Some good candidates would be to simplify tasks that you normally do but they take significant time to set up, initializing an object or objects for extensive testing, or maintenance routines that you find yourself doing over and over.

Just like we used cell and line magic, these two types exist for creating your own magic commands. For most of my use cases, line magic suffices, because I either don't need an argument, or I can use a singular one-- I haven't come across a case where it would benefit me to use the multiple lines available for cell magic, but it is an option if you so choose.

To use custom magic, create a Python file (I name mine `custom_magic.py` but the name can be anything you like) and place it in your profile's `startup` directory.

When working on a local machine, it makes things easier if all users have the same password, which may not always be the case, especially right after a database refresh. I typically use something trivial because locally, security is not an issue, so I'd like to get around the sometimes stringent requirements that a user's password must abide by. We can invoke this password normalizer using a line magic decorator:

```python
# /Users/eric/.ipython/profile_zagnut/startup/custom_magic.py
from IPython.core.magic import register_line_magic


@register_line_magic
def reset_passwords(line):
    new_password = line or 'foobar'
    all_users = User.objects.all()
    first_user = all_users.first()
    first_user.set_password(new_password)
    hashed_password = first_user.password
    num_users = all_users.update(password=hashed_password)
    print(f'{num_users} passwords were changed to "{new_password}"')
```

This can be executed in the shell by simply running `%reset_passwords`. If you want to use something besides the given default of `foobar`, just pass it in:

```python
In [1]: %reset_passwords apples
15 passwords were changed to "apples"
```

Another use case that you may find handy is generating UUIDs. I had a task where I needed to be able to generate one or more on the fly, and having a command that can do so is quite useful:

```python
# /Users/eric/.ipython/profile_zagnut/startup/custom_magic.py
import uuid


@register_line_magic
def generate_uuid(line):
    def gen(n=1):
        for _ in range(n):
            print(uuid.uuid4())
    if line:
        try:
            gen(n=int(line))
        except ValueError:
            print('You must pass in an integer.')
    else:
        gen()
```

Again, you can pass `%generate_uuid` by itself or with an argument:

```
In [1]: %generate_uuid
bbaa0515-2c19-42dd-847e-55cde8451e6f

In [2]: %generate_uuid 4
e8843287-a213-4c46-be8c-ac4b71f1614b
7112e1b9-7467-465d-973f-96d423abccee
9d599896-0aa6-4002-b24c-02fff858f2b7
8b0b23c4-9257-4fdf-9d26-c8e5b1dff128

In [3]: %generate_uuid abc
You must pass in an integer.
```
