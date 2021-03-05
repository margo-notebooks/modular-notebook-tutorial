# Modular notebooks quickstart

## Overview

Modular notebooks are notebooks that can be imported like Python modules. We do
this using the Margo Loader library, which lets you import notebooks using
Python's built-in `import` statement, and use special comments called "margin
notes" to tell the importer which cells to include or exclude. This lets you
write notebooks that are full of scratch code and demonstration code with
outputs that make notebooks great but then drop those cells to make the
notebooks more useful as modules.

## Prerequisites

This guide requires you to have a working Jupyter Notebook environment, or some
other notebook authoring tool, such as Jupyter Lab, or even Visual Studio Code.

It also requires you to install the margo-loader library. You can do this with:

```bash
$ pip install margo-loader
```

## Importing a notebook

To import a notebook, first import `margo_loader` and then import the notebook,
in this case, let's assume it's called greetings.