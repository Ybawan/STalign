# STalign

`STalign` aligns spatial transcriptomics (ST) tissue sections to each other and to 3D atlases like the Allen Brain Atlas using algorithms that build upon diffeomorphic metric mapping. 

More information regarding the overall approach, methods and validations can be found on the bioRxiv preprint:
<a href="https://www.biorxiv.org/content/10.1101/2023.04.11.534630v1">
<b>Alignment of spatial transcriptomics data using diffeomorphic metric mapping</b>
Kalen Clifton*, Manjari Anant*, Osagie K Aimiuwu, Justus M Kebschull, Michael I Miller, Daniel Tward^, Jean Fan^
</a>

## Overview

<img src="https://jef.works/assets/papers/STalign_anim_small.gif">

STalign enables:
- alignment of single-cell resolution ST datasets within technologies
- alignment single-cell resolution ST datasets to histology
- alignment of ST datasets across technologies
- alignment of ST datasets to a 3D common coordinate framework 

## Installation & Import

### Installation using pip

This installation method is intended for users who sets up a Python environment without `pipenv`.

`$ pip install "git+https://github.com/JEFworks-Lab/STalign.git"`

*All dependencies will be installed with the above command. Dependencies can be found in the requirements.txt file.*

### Installation using Pipfile from source

This installation method is intended for users who sets up a Python environment with `pipenv`. `pipenv` allows users to create and activate a virtual environment with all dependencies within the Python project. More information and installation method for `pipenv` can be found here: https://pipenv.pypa.io/en/latest/.

Fork and `git clone` the `STalign` github repository.

From the base directory of your local `STalign` git repo. create a `Pipfile.lock` file from `Pipfile` using:
`$ pipenv lock`

> **_NOTE:_** Since `Pipfile.lock` is platform-dependent and different across operating systems, do not commit `Pipfile.lock` to the git repo if contributing to `STalign` or collaborating with other people.

Install `PyTorch` dependency using:
`pipenv install torch==2.0.0`

Activate the virtual environment using:
`pipenv shell`

Deactivate the virtual environment using:
`exit`

### Import
To import STalign into your Python script, use: `from STalign import STalign`

## Input Data
To use this tool, you will need provide the following information:

### single-cell resolution ST alignment
- Source: Arrays of x and y positions of cells
- Target: Arrays of x and y positions of cells

### single-cell and spot-resolution ST alignment
- Source: Arrays of x and y positions of cells from single-cell resolution ST data
- Target: Registered H&E image from spot-resolution ST data

### 3D-2D alignment
- Source: (Default: Adult mouse Allen Brain Altas CCFv3) 3D Matrix with voxels corresponding to (1) cell intensity and (2) annotated tissue regions
- Target: Arrays of x and y positions of cells

## Usage

To use `STalign`, please refer to our [tutorials](https://jef.works/STalign/tutorials.html) with usage examples.

## Tutorials
To use `STalign`, please refer to the following Jupyter Notebooks with usage examples: <br />
- [MERFISH-MERFISH Alignment](https://jef.works/STalign/notebooks/merfish-merfish-alignment.html) <br />
- [Xenium-Xenium Alignment](https://jef.works/STalign/notebooks/xenium-xenium-alignment.html) <br />
- [Xenium-H&E Image Alignment](https://jef.works/STalign/notebooks/xenium-heimage-alignment.html) <br />
- [3D alignment to the Allen Brain Atlas](https://jef.works/STalign/notebooks/merfish-allen3Datlas-alignment.html) <br />
- [MERFISH-Visium Alignment](https://jef.works/STalign/notebooks/merfish-visium-alignment-with-point-annotator.html) <br />
>>>>>>> 9b545f80abee4a6eeca7a99fcb969dae996cf74a

