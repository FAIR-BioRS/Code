

[![Contributors][contributors-shield]][contributors-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]


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
This is the dataset associated with our manuscript on FAIR Biomedical Research Software (FAIR-BioRS) guidelines [1]. As part of that effort, we conducted a literature review to identify actionable guidelines for making research software FAIR. The data collected in that review is available in the dedicated GitHub repository [2]. This respository contains the Jupyter notebook used to analyze that review data. We refer to the manuscript for details about the use of this Jupyter notebook.

## Standards followed
The overall code is structured according to the FAIR-BioRS guidelines using FAIRshare [1,3,4]. The Python code in the Jupyter notebook [main.ipynb](main.ipynb) follows the PEP8 guidelines [5]. All the dependencies are documented in the [environment.yml](environment.yml) file.

## Using the Jupyter notebook

### Prerequisites 
We recommend using Anaconda to create and manage your development environment. All the subsequent instructions are provided assuming you are using [Anaconda (Python 3 version)](https://www.anaconda.com/products/individual).

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

### Setup kernell for Jupyter lab
```sh
$ conda activate env-GI-review
$ conda ipython kernel install --user --name=<any_name_for_kernel>
$ conda deactivate
```
### Launch Jupyter lab
Launch Jupyter lab and naviguate to open the main.ipynb file. Make sure to change the kernel to the one created above (e.g., see https://doc.cocalc.com/howto/jupyter-kernel-selection.html#cocalc-s-jupyter-notebook)

## Inputs/outputs

The Jupyter notebook makes use of files in the associated GitHub repository (2). The code points directly to the required files so it is not required to download them. The csv file in the [input](input) folder can also be called as input to avoid re-running some time consuming code-block.

Outputs of the code tables display directly in the notebook are plots displayed in the notebook but also saved as files to be included in our manuscript [1]. These saved plots are included in the [output](output) folder. 

## References
[1] Patel, B., Soundarajan, S., & Hu, Z. Making Biomedical Research Software FAIR: Actionable Step-by-step Guidelines with a User-support Tool [DOI: TBA]

[2] https://github.com/fairdataihub/FAIR-BioRS-data

[3] Soundarajan, S. & Patel, B. FAIRshare: FAIR data and software sharing made easy. (2022). doi:10.5281/zenodo.6464058

[4] https://github.com/fairdataihub/FAIRshare

[5] https://peps.python.org/pep-0008/
