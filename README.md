## ESI for "Bayesian determination of the effect of a deep eutectic solvent on the structure of lipid monolayers"

[Andrew R. McCluskey](https://orcid.org/0000-0003-3381-5911)

This is the electronic supplementary information (ESI) associated with the publication "Bayesian determination of the effect of a deep eutectic solvent on the structure of lipid monolayers" [1].

### [Data](https://researchdata.bath.ac.uk/id/eprint/548)

The reduced X-ray  and neutron reflectometry data can be obtained from the University of Bath Research Data Archive.

[https://researchdata.bath.ac.uk/id/eprint/548](https://researchdata.bath.ac.uk/id/eprint/548)

The full neutron reflectometry data can be obtained from the ILL Data Archive.

DOI: [10.5291/ILL-DATA.9-13-612](http://doi.org/10.5291/ILL-DATA.9-13-612)

### Analysis

This ESI aims to provide a fully reproducible workflow to the data analysis presented within the paper.

Requirements:

- anaconda or miniconda python
- make

The supplied Makefile, will reproduce all of the analysis, plot the figures, and build a preprint version of the paper when run. Be aware that the analyses within this work are non-trivial and take many hours to run so **use caution** before re-running.

If you **still** want to re-run all of the analysis, please download the [experimental data](https://researchdata.bath.ac.uk/id/eprint/548), place it in a directory named `data/processed` before running the following commands:

```
conda create --name paper_env python

source activate paper_env

pip install -r config/requirements.txt

make clean # this will remove all of the output from previous runs

make
```

### [Figures](/reports/figures)

PDF versions of the figures, can be found in the `reports/figures` directory.

### Citing this ESI

Cite as:

#### BibteX

```
bibtex here
```

### Acknowledgements

A. R. M. Is grateful to the University of Bath and Diamond Light Source for co-funding a studentship (Studentship Number STU0149). The authors thank the European Spallation Source and the University of Bath Alumni Fund for supporting A. S.-F.

### Bibliography

1. REFERENCE TO THE PAPER

### Project Organization

    .
    ├── AUTHORS.md
    ├── LICENSE              # MIT License
    ├── README.md            # You are here
    ├── Makefile             # Makefile to outline workflow
    ├── output               # Files and data output by analysis scripts
        ├── dlpc             #
        ├── dmpc             #
        ├── dmpg             #
        └── dppc             #
    ├── config               # requirements.txt file
    ├── notebooks            # Notebooks for analysis
    ├── reports              # Paper and ESI
    │   └── figures
    └── src
        ├── models           # mol_vol.py custom model for refnx
        ├── tools            # helper.py script
        └── visualization    # Plotting scripts
