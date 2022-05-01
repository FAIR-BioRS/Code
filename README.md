

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
This is the code associated with our manuscript on actionable guidelines for making research software FAIR [1]. It is structured according to the FAIR-BioRS guidelines using FAIRshare [1,2,3]. We refer to the manuscript for details about the dataset content.

## Using the Jupyter notebook under the code folder

### Prerequisites 
We recommend using Anaconda to create and manage your development environment. All the subsequent instructions are provided assuming you are using [Anaconda (Python 3 version)](https://www.anaconda.com/products/individual).

This dataset is necessary to run the code: https://github.com/fairdataihub/FAIR-BioRS-data

### Clone repo
Clone the repo or download as a zip and extract.

### cd into the code folder

Open Anaconda prompt (Windows) or the system Command line interface then naviguate to the code
```sh
cd .GI-review-dataset/code

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
Launch Jupyter lab and naviguate to open the main.ipynb file under the code folder. Make sure to change the kernel to the one created above (e.g., see https://doc.cocalc.com/howto/jupyter-kernel-selection.html#cocalc-s-jupyter-notebook)


## References
[1] Patel, B., Soundarajan, S., & Hu, Z. Making Biomedical Research Software FAIR: Actionable Step-by-step Guidelines with a User-support Tool [DOI: TBA]

[2] Soundarajan, S. & Patel, B. FAIRshare: FAIR data and software sharing made easy. (2022). doi:10.5281/zenodo.6464058

[3] https://github.com/fairdataihub/FAIRshare
