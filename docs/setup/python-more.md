# Additional Python packages

Anaconda's Python Distribution comes with many of the packages we need to do scientific computing.
If you're interested in all the packages included, click [here](https://docs.continuum.io/anaconda/packages/pkg-docs) and go to the Python 3.6 tab.

Howevever, you may come across packages that are not installed by default.
In this case we recommend you use the `pip` package management tool to install them.

!!! note
    If your python 3 was found via `python3 --version` on the previous page, then type `pip3` instead of `pip` for all of the following python plugins.

First let us update pip by typing the following into the terminal

```bash
pip install --upgrade pip
```

If you get an error, try typing instead:
```bash
python -m pip install --upgrade pip
```

For this course, we will need the package `Selenium` as part of the web scraping tool kit we will build up. First let us install a depency for it via

```bash
pip install msgpack
```

We then install `selenium` by entering the following into a terminal:

```bash
pip install selenium
```

`pip` will then go through and install the package we asked for, and any other dependencies.
If this succeeded, the last line it printed out should be:

```
Successfully installed selenium-3.14.0
```

## More packages

Please also install the following packages:

```bash
pip install textblob
```
