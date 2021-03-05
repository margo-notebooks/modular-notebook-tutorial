# Writing Modular Jupyter Notebooks

by Jake Kara <jake@jakekara.com>

## Overview

This repository includes a set of interactive tutorials on writing modular Jupyter Notebooks and the underlying margin note concept that makes them possible, and the specific syntax for margin notes, called Margo.

This repositority can be run live without any installation using MyBinder.org.  

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/margo-notebooks/modular-notebook-tutorial/HEAD?filepath=README.ipynb)

## Prerequisites

These notebooks assumes some basic experience with Python and Jupyter Notebooks.

## Lessons

The notebooks in this repository are designed to be read in a particular order.

The first two notebooks will be enough for most readers who just want to learn about modular notebooks — how to write them, and how to import them.

* [Importing notebooks.ipynb](./Importing%20Notebooks.ipynb) — Learn to use Margo Loader to import a notebook as a Python module.
* [Met API.ipynb](./Met%20API.ipynb) — Learn to use Margo notes to write a notebook that's useful both as a notebook and a module.

Margo notes can be used for more than making notebooks more useful as reusable modules. They can also be used to encode information about the notebook that can be read by other applications. This next notebook shows one way this can be very useful.

* [Generating requirements.txt.ipynb](./Generating%20requirements.txt.ipynb) — Learn store a notebook's dependencies in Margo notes and retrieve them with a command-line tool.

The next two notebooks look in a little more depth at the syntax and keywords we've used in the previous notebooks.

* [Margo keyword reference.ipynb](./Margo%20keyword%20reference.ipynb) — Throughout these notebooks, we use Margo notes with specific keywords, like `ignore-cell` and `module-stop`, that have special meaning to the application Margo Loader. This notebook defines their meanings all in one place.
* [Margo syntax primer.ipynb](./Margo%20syntax%20primer.ipynb) — The keywords we've learned about so far are not part of the underlying Margo syntax — they're keywords that are defined by applications built on top of Margo. This notebook describes in a bit more detail how the underlying Margo syntax works. Knowing the mechanics of the syntax, you can define new keywords for your own purposes, including developing new applications that extend Jupyter Notebooks in different ways.

## More realistic example

This suite of notebooks is a walk-through meant to ease you into using modular notebooks. But you might ask, "why bother with modular notebooks at all?" The answer is that with modular notebooks you can break your methodology into smaller pieces, allowing you to write more robust software than is possible in monolithic notebooks, and allows you to demonstrate each step of your methodology in its own notebook. The following link demonstrates this with a much more robust suite of notebooks designed to perform color palette extraction on prints by the artist William Blake: [https://mybinder.org/v2/zenodo/10.5281/zenodo.4554402/](https://mybinder.org/v2/zenodo/10.5281/zenodo.4554402/).
