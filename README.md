# ipython-book
IPython for Web Devs

Want to contribute? Follow the instructions below for getting a local instance of the book up and running on your computer.

`mdBook` is required to run this book locally. If you have `cargo` installed, you can simply run

```
cargo install mdbook
```

and you should be good to go. If you don't have it installed, or have any idea what `cargo` is, you can [follow the directions here](https://github.com/rust-lang/mdBook#installation) to get `mdbook` up and running on your system.

Once `mdbook` is installed, fork and clone this branch.

1. Click the `fork` button on the top right
2. Clone said branch

```
git clone git@github.com:<your github username here>/ipython-book.git
```

Run the `serve` command to get a local server up and running:

```
mdbook serve

2020-10-22 15:52:21 [INFO] (mdbook::book): Book building has started
2020-10-22 15:52:21 [INFO] (mdbook::book): Running the html backend
2020-10-22 15:52:21 [INFO] (mdbook::cmd::serve): Serving on: http://localhost:3000
2020-10-22 15:52:21 [INFO] (warp::server): Server::run; addr=V6([::1]:3000)
2020-10-22 15:52:21 [INFO] (warp::server): listening on http://[::1]:3000
2020-10-22 15:52:21 [INFO] (mdbook::cmd::watch): Listening for changes...
```

You can then visit the site on `http://localhost:3000`.

For more details about using `mdbook`, visit the official docs here:

https://github.com/rust-lang/mdBook#usage
