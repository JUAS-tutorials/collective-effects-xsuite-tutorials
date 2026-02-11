# JUAS Collective Effects simulation

## Introduction

This repository contains the JUAS Collective Effects tutorial notebook.


## Content of the notebooks

### 3D numerical simulation of Wakefields and Impedance in `Impedance-demo.ipynb`

Study the impedance of the LHC Bellows and explore shielding mitigation options using the numerical open-source solver [Wakis](https://github.com/ImpedanCEI/wakis)

### Transverse instability threshold of the HL-LHC at injection energy `JUAS_tutorial.ipynb`

Study the transverse instability threshold for various beam parameters and find mitigation strategies to stabilize the beam.

## Installation

### Xsuite/Xwakes

Follow first the installation instructions detailed in the [dedicated repository](https://github.com/JUAS-tutorials/xsuite-installation).
This repository can be cloned using git `git clone https://github.com/JUAS-tutorials/collective-effects-xsuite-tutorials.git` or the repository content can be downloaded directly via [this link](https://github.com/JUAS-tutorials/collective-effects-xsuite-tutorials/archive/refs/heads/main.zip).

### Wakis

The instructions to install Wakis can be found in the [Wakis repository](https://github.com/ImpedanCEI/wakis), and are summarized here:

#### Basic install in a python environment with versions 3.9 - 3.12
```bash
pip install wakis['notebook']    # complete installation for notebook use
```

#### Multithreaded version
```bash
# create dev python environment
conda create --name wakis-env python=3.12 mkl mkl-service
conda activate wakis-env

# pip install wakis and other useful packages
pip install sparse_dot_mkl       # multithreaded version of scipy.sparse
pip install wakis['notebook']    # complete installation for notebook use
pip install bihc neffint iddefix # optional satellite packages
```

#### Editable installation for latest changes
```bash
git clone https://github.com/ImpedanCEI/wakis.git
cd wakis
pip install -e .
```