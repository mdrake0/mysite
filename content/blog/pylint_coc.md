---
title: "Fixing Broken Imports with Neovim, Pylint, venv, and CoC"
date: 2021-04-04T16:21:03-04:00
draft: false
---

I strugged with this for a while, so I assume someone else will as well. As is
often the case with configuration issues, the solution turned out to be
straightforward.

## Relevant parts of my dev environment

- Neovim
- Pylint
- venv
- CoC

## Problem statement

CoC/Pylint reports "E0401" import errors on libraries that
are correctly installed in a virtual environment.

![Pylint E0401](/img/pylint_e0401.png)

## Cause

CoC is using the wrong Python interpreter to run pylint. In my case, it was
running the system installation, when I needed it to run the interpreter for
my virtual environment.

## Fix

Point CoC to the right interpreter using `:CocCommand python.setInterpreter`
and then selecting the one in my virtual environment.

![Fixing pylint E0401](/img/pylint_e0401_fix.png)

Hope this helps!
