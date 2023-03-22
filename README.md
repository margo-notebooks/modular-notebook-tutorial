# Writing Modular Jupyter Notebooks

by Jake Kara <jake@jakekara.com>

## Overview

This repository includes a set of interactive tutorials on writing modular Jupyter Notebooks and the underlying margin note concept that makes them possible, and the specific syntax for margin notes, called Margo.

## Setup

### Option 1: Run remotely on MyBinder.org

This repositority can be run live without any installation using MyBinder.org.

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/margo-notebooks/modular-notebook-tutorial/HEAD?filepath=README.ipynb)

> Note: Occasionally, MyBinder.org fails to set up and launch a container, and in my experience this has been temporary, due to server capacity limitations on their end. If it doesn't launch for you at first, try again later or follow one of the local setup steps below.

### Option 2: Run locally with repo2docker

If you are a Docker user, you can run these notebooks locally in a container, using repo2docker, the same tool that is used by MyBinder.org.

First, install repo2docker:

```bash
pip install repo2docker
```

Next, run:

```bash
repo2docker https://github.com/margo-notebooks/modular-notebook-tutorial
```

This step will take a moment and output a lot of text to the terminal. At the end, you should see something like:

```
    To access the notebook, open this file in a browser:
        file:///home/karaj/.local/share/jupyter/runtime/nbserver-25-open.html
    Or copy and paste this URL:
        http://127.0.0.1:53244/?token=123456123456123456123456123456123456123456
```

Follow the link in a browser to the notebook environment.

### Option 3: Run locally with Python

If you cannot or prefer not to run these lessons remotely or in Docker, follow these steps to install this project and run on your machine.

Clone this repo and `cd` into it:

```bash
git clone git@github.com:margo-notebooks/modular-notebook-tutorial.git
cd modular-notebook-tutorial
```

This is optional, but I recommend setting up a virtual environment for this (and any) Python project to isolate your dependencies. Here's an example using `mkvirtualenv`, but there are other tools, like `conda`, or `venv`.

```bash
mkvirtual-env modular-notebook-tutorial
workon modular-notebook-tutorial
```

Next, install project dependencies

```
pip install -r requirements.txt
```

If you don't have a Jupyter environment, [install one](https://jupyter.org/install) as well: 


## Lessons

Now that you've completed setup steps, you're ready to move on to lessons, which are all Jupyter notebooks. They are designed to be read in a particular order.

The first two notebooks will be enough for most readers who just want to learn about modular notebooks — how to write them, and how to import them, and how to exclude cells from export using Margo notes.

* [Importing notebooks.ipynb](./Importing%20Notebooks.ipynb) — Learn to use Margo Loader to import a notebook as a Python module.
* [Met API.ipynb](./Met%20API.ipynb) — Learn to use Margo notes to write a notebook that's useful both as a notebook and a module.

Margo notes can be used for more than using notebooks as modules. They can also be used to encode information about the notebook that can be read by other applications. This next notebook shows one way this can be very useful:

* [Generating requirements.txt.ipynb](./Generating%20requirements.txt.ipynb) — In this demo, we'll store a notebook's dependencies in Margo notes, retrieve them with a Margo's built-in command-line tool, and use them to generate a requirements.txt file.

The next two notebooks look in a little more depth at the syntax and keywords of Margo notes that we've used in the previous notebooks.

* [Margo keyword reference.ipynb](./Margo%20keyword%20reference.ipynb) — Throughout these notebooks, we use Margo notes with specific keywords, like `ignore-cell` and `module-stop`, that have special meaning to the application Margo Loader. This notebook defines their meanings all in one place.
* [Margo syntax primer.ipynb](./Margo%20syntax%20primer.ipynb) — This notebook describes in a bit more detail how the underlying Margo syntax works. Knowing the mechanics of the syntax, you can define new keywords for your own purposes, including developing new applications that extend Jupyter Notebooks in different ways.

## More realistic example

This suite of notebooks is a walk-through meant to ease you into using modular notebooks. But you might ask, "why bother with modular notebooks at all?" The answer is that with modular notebooks you can break your methodology into smaller pieces, allowing you to write higher quality software than is possible in monolithic notebooks, and allows you to demonstrate discrete steps of your methodology in smaller, more comprehensible notebooks. The following link demonstrates this with a much more robust suite of notebooks designed to perform color palette extraction on prints by the artist William Blake: [https://mybinder.org/v2/zenodo/10.5281/zenodo.4554402/](https://mybinder.org/v2/zenodo/10.5281/zenodo.4554402/).
