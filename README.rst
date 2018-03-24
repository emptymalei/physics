# My Physics Notebook

I have been writing physics notes on my computer for many years. Ideally, I would merge all the notes in one place. However, the different formatting, tech stack, and styles make it hard to unify all my notes. Nevertheless, I maintain most of my physics notes here.

## Structure of the project


```
.
├── LICENSE
├── README.rst
└── docs
    ├── Makefile
    ├── _build
    ├── _static
    ├── _templates
    ├── _themes
    ├── astrophysics
    ├── changelog.txt
    ├── cm
    ├── conf.py
    ├── contributors.rst
    ├── cosmology
    ├── electrodynamics
    ├── exts
    ├── fun
    ├── index.rst
    ├── math
    ├── preface.rst
    ├── qualitative-methods
    ├── quantum
    ├── relativity
    ├── statmech
    └── vocabulary
```

All the notes are in the folder `docs`. Files or folders that starts with `_` are supposed to be files of the notebook system. `conf.py` is the configuration file, where you can change the notebook title, authors, etc. `exts` is for plugins. All other files are the contents, where you can modify the notes.

## Build

`sphinx-doc` is required to build the notes.

This notebook itself is hosted on readthedocs.org. 

In any event of development or reuse, clone the repo:

```
git clone https://github.com/emptymalei/physics.git
```

Change current directory to `docs`:

```
cd physics/docs
```

Build html:

```
make html
```



## Related notebooks

1. `Statistical Physics <http://statisticalphysics.openmetric.org/>`_
2. `Intelligence <http://intelligence.readthedocs.io/>`_
3. `Computational Methods <http://computational.neutrino.xyz/>`_
4. `Neutrino Physics <http://docs.neutrino.xyz/>`_

## DOI


.. image:: https://zenodo.org/badge/7726/CosmologyTaskForce/PhysicsResearchSurvivalManual.svg
   :target: http://dx.doi.org/10.5281/zenodo.13216
