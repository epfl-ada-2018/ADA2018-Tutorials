# 00 - Intro to Tools

This tutorial should see you up and running with your python environment, plus give you the basics of Jupyter Notebooks.

## Part 1: setting-up your environment

[Anaconda](https://www.anaconda.com/download/)

[Git cheatsheet](http://rogerdudler.github.io/git-guide/)

* clone the tutorials repo in a local folder

```
git clone https://github.com/epfl-ada-2018/ADA2018-Tutorials
```

* or pull new changes if you already have it (from the tutorials local folder)

```
git pull
```
    
[Jupyter](http://jupyter.org)

* create a new environment (use phyton 3.5/6 or 2.7)

```
conda create -n ada python=3.6 scipy pandas numpy matplotlib
```

* activate it
    
```
source activate ada
```

* list your environments
    
```
conda info --envs
```

* deactivate the current environment and remove an environment
    
```
source deactivate
conda remove --name ada --all
```

[more info on managing environments](https://conda.io/docs/user-guide/tasks/manage-environments.html)

* install jupyter using conda
    
```
conda install jupyter bokeh seaborn nb_conda_kernels
```

* install some extensions using the python package manager
    
```
pip install jupyter_nbextensions_configurator
```

If you get an error about packages requiring cython and PyHamcrest, try the following:
```
pip install cython PyHamcrest jupyter_nbextensions_configurator
```

* IF you have later problems with widgets (conda version might not be the last one!)
    
```
pip install --upgrade ipywidgets
    
jupyter nbextension enable --py widgetsnbextension
    
jupyter nbextension enable --py --sys-prefix widgetsnbextension
```

* run a notebook server, be sure to be at the tutorial's folder, a browser window should open up for you

```
jupyter notebook
```

* IF you have more problems with widgets

```
jupyter serverextension enable --sys-prefix jupyter_nbextensions_configurator nb_conda nb_anacondacloud nbpresent
```

* IF you later have warnings about missing fonts, in Ubuntu the missing fonts are in `fonts-humor-sans` (to install them: `sudo apt install fonts-humor-sans`). You may also have to clean `matplotlib`'s font cache (~/.cache/matplotlib/) and restart your current jupyter session, for matplotlib to take notice of the changes.

## Part 2: overview of Jupyter notebooks

In this tutorial we explore the functionalities of the IPython Notebooks. In this repository you can find the notebook we use during the tutorial.

Credits to [saloot](https://github.com/saloot) and [Michele Catasta](https://github.com/pirroh), on whose material this version is based.

## Part 3: Homework 00!

Agree to work on groups of 3 people. Take the first 2 homeworks as an opportunity to get to know your team: you can change before the third homework, after it the groups are made (also for the project!). 3 persons is mandatory, only motivated exceptions will be accepted. Use Mattermost or other means to find a team if in need!

Access your first (OPTIONAL and UNGRADED) homework [here](https://github.com/epfl-ada-2018/ADA2018-Homeworks/tree/master/00%20-%20Optional%20homework). Clone the repo locally and take the opportunity to freshen-up your Python skills, or to acquire them.

For the homework 00, *one* member per group has to use the [this link](https://classroom.github.com/g/eOXaZkyS) to register a team for the exercise and invite the other members, which will create your *team repository for the exercise*.
Also, remember to register BY FRIDAY 28th Sept. [here](https://goo.gl/EfVKhJ). Every member of the group should register with his/her email and the group repository. 

On Friday 28th. the next, graded homework will be released, along with a tutorial on Pandas.
