---
title: Virtual environment in Python
date: 2022-12-26 09:00:00 +0100
categories: [Python]
tags: [python] # TAG names should always be lowercase
---

![virtual environment Python](https://files.realpython.com/media/Python-Virtual-Environments_Watermarked.4c787192d42f.jpg)

A virtual environment is a Python tool for dependency management and project isolation. That means you can separate dependencies for one project from dependencies for other ones, so they can have different versions of the same library. That usually happens when we start projects at different times. Using a virtual environment also allows you to avoid installing Python packages globally which could break system tools or other projects.
You can install venv to your host Python by running this command in your terminal:

```shell
pip install virtualenv
```

To use venv in your project, in your terminal, create a new project folder, cd to the project folder in your terminal, and run the following command:

```shell
python<version> -m venv <virtual-environment-name>
```

After making the ven we need to activate it:

```shell
source env/bin/activate
```

Source: freecodecamp.org
