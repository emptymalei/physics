# My Physics Notebook

I have been taking notes on physics for many years. I wanted to build a knowledge base for myself to make sure that I can recreate as many physics as possible. However, things turned out to be much harder than I expected. This becamse a legacy project. I am only maintaining a few special topics, such as statistical physics, at this moment.


## Related notebooks

1. `Statistical Physics <http://statisticalphysics.openmetric.org/>`_
2. `Intelligence <http://intelligence.readthedocs.io/>`_
4. `Neutrino Physics <http://docs.neutrino.xyz/>`_


## Structure of the project


```
.
├── LICENSE
├── README.rst
└── docs
    ├── Makefile
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




## DOI


[![](https://zenodo.org/badge/7726/CosmologyTaskForce/PhysicsResearchSurvivalManual.svg)](http://dx.doi.org/10.5281/zenodo.13216)
