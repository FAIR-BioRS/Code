[![Contributors][contributors-shield]][contributors-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.6468963.svg)](https://doi.org/10.5281/zenodo.6468963)
[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/fairdataihub/FAIR-BioRS-code/HEAD?labpath=main.ipynb)

[contributors-shield]: https://img.shields.io/github/contributors/bvhpatel/GI-review-dataset.svg?style=flat-square
[contributors-url]: https://github.com/bvhpatel/GI-review-dataset/graphs/contributors
[stars-shield]: https://img.shields.io/github/stars/bvhpatel/GI-review-dataset.svg?style=flat-square
[stars-url]: https://github.com/bvhpatel/GI-review-dataset/stargazers
[issues-shield]: https://img.shields.io/github/issues/bvhpatel/GI-review-dataset.svg?style=flat-square
[issues-url]: https://github.com/bvhpatel/GI-review-dataset/issues
[license-shield]: https://img.shields.io/github/license/bvhpatel/GI-review-dataset.svg?style=flat-square
[license-url]: https://github.com/bvhpatel/GI-review-dataset/blob/master/LICENSE

# FAIR-BioRS-code

## About
This is the dataset associated with our manuscript on FAIR Biomedical Research Software (FAIR-BioRS) guidelines [1]. As part of that effort, we conducted a literature review to identify actionable guidelines for making research software FAIR. The data collected in that review is available in the dedicated GitHub repository [2]. This repository contains the Jupyter notebook used to analyze that review data. We refer to the manuscript [1] for further details about the use of this Jupyter notebook.

## Standards followed
The overall code is structured according to the FAIR-BioRS guidelines using FAIRshare [1,3,4]. The Python code in the Jupyter notebook [main.ipynb](main.ipynb) follows the [PEP8 guidelines](https://peps.python.org/pep-0008). Functions are documented with docstring formatted following [Google's style guide](https://google.github.io/styleguide/pyguide.html#38-comments-and-docstrings). All the dependencies are documented in the [environment.yml](environment.yml) file.

## Using the Jupyter notebook

### Prerequisites 
We recommend using Anaconda to create and manage your development environment and using JupyterLab to run the notebook. All the subsequent instructions are provided assuming you are using [Anaconda (Python 3 version)](https://www.anaconda.com/products/individual) and JupyterLab.

### Clone repo
Clone the repo or download as a zip and extract.

### cd into the code folder

Open Anaconda prompt (Windows) or the system Command line interface then naviguate to the code
```sh
cd .FAIR-BioRS-code

```

### Setup conda env
```sh
$ conda env create -f environment.yml
```
### Setup env vars
The environment variables required are listed in the table below along with information on how to get them


<table>
<thead>
  <tr>
    <th>Name</th>
    <th>Value or instructions for obtaining it</th>
    <th>Purpose</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td> GITHUB_ACCESS_TOKEN </td>
    <td> <a href="https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token">GitHub documentation</a> </td>
    <td>Required (optionally) to run the code block related to counting the number of biomedical-related repositories on GitHub</td>
  </tr>
</tbody>
</table>


Each of them can be set in your conda environment as follows
```sh
$ conda activate FAIR-BioRS-code
$ conda env config vars set MY_VAR=value1 MY_OTHER_VAR=value2
```
### Setup kernell for Jupyter lab
```sh
$ conda activate FAIR-BioRS-code
$ conda install ipykernel
$ ipython kernel install --user --name=<any_name_for_kernel>
$ conda deactivate
```
### Launch Jupyter lab
Launch Jupyter lab and naviguate to open the main.ipynb file. Make sure to change the kernel to the one created above (e.g., see [here](https://doc.cocalc.com/howto/jupyter-kernel-selection.html#cocalc-s-jupyter-notebook)). We recommend to use the [JupyterLab code formatter](https://github.com/ryantam626/jupyterlab_code_formatter) along with the [Black](https://github.com/psf/black) and [isort](https://github.com/PyCQA/isort) formatters to facilitate compliance with PEP8 if you are editing the notebook.

## Inputs/outputs

The Jupyter notebook makes use of files in the associated GitHub repository [2]. The code points directly to the required files so it is not required to download them. The csv file in the [input](input) folder can also be called as input to avoid re-running some time consuming code-block.

Outputs of the code include tables displayed directly in the notebook and plots displayed in the notebook but also saved as files to be included in our manuscript [1]. These saved plot files are included in the [output](output) folder here. 

## References
[1] Patel, B., Soundarajan, S., Hu, Z. (2022) *Making Biomedical Research Software FAIR: Actionable Step-by-step Guidelines with a User-support Tool*. bioRxiv (https://doi.org/10.1101/2022.04.18.488694)

[2] https://github.com/fairdataihub/FAIR-BioRS-data

[3] Soundarajan, S. & Patel, B. (2022) *FAIRshare: FAIR data and software sharing made easy*. Zenodo (https://doi.org/10.5281/zenodo.6464058)

[4] https://github.com/fairdataihub/FAIRshare

