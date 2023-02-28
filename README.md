# MA999-slides

Lecturing slides for MA999 - Agent based modelling

You will need Julia installed with the IJulia kernel for Jupyter.

To view the notebooks as slides you need to add some extensions to Jupyter:

* [RISE](https://rise.readthedocs.io/en/stable/)
* The splitcell extension from [Jupyter notebook extensions](https://github.com/ipython-contrib/jupyter_contrib_nbextensions)


## Prerequsities

To complete this coursework you will simply need Julia and Jupyter. 

### 1. Julia

You will need Julia >= 1.8.0. An earlier version should work but you might need to install a few packages yourself and/or a make a few tweaks.

You can download Julia from here: https://julialang.org/downloads/, and then follow isntallation instructions for your operating system. 

Check if Julia works by typing `julia` in the terminal.

### 2. Jupyter 

You can install Jupyter using Anaconda, https://www.anaconda.com/products/distribution. You can also run Jupyter notebooks in VSCode using the Python extension.

### 3. IJulia

To add Julia to Jupyter: 
- Launch Julia in the terminal 
- Press `]` to enter the pkg mode (the arrow should change to blue and say `pkg`)
- Type `add IJulia` to install the Julia kernel for Jupyter

After this, simply go to the terminal and type `jupyter notebook` to open the Jupyter window. You now should be able to run the coursework notebook.

Any issues should be directed to s.zhydkov@warwick.ac.uk.

# Troubleshooting

## General tips

If something doesn't work, try deleting the `Manifest.toml` file and running it again.

## GLMakie Error

Ubuntu users might experience an error when loading the GLMakie package in the Coursework. This is due to an issue with Ubuntu drivers.

Here's some steps from Elliot that helped him:

"In order, I did:

1. sudo apt install xorg-dev (as recommended here)

2. sudo add-apt-repository ppa:ubuntu-x-swat/updates
     and
  sudo apt-get dist-upgrade (as recommended here)

Restarted my laptop to make sure it had all set in, ran the coursework again, GLMakie still didn't work.

3. Went into .bashrc (you can edit it by typing, e.g., `code ~/.bashrc` in the terminal if you have vscode) and added the line "export LD_PRELOAD=/usr/lib/x86_64-linux-gnu/libstdc++.so.6" at the bottom (as recommended here)

After restarting the terminals so it would know that bash stuff was changed, the Makie code runs and the game interface works."

