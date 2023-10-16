## Random Projection Forest Initialization for Graph Convolutional Networks

[![Paper](http://img.shields.io/badge/arXiv-2302.12001-b31b1b.svg)](https://arxiv.org/abs/2302.12001)
[![Papers with Code](http://img.shields.io/badge/PaperswithCode-2302.12001-21cbce.svg)](https://paperswithcode.com/paper/random-projection-forest-initialization-for)
[![Python 3.9+](https://img.shields.io/badge/python-3.9+-blue.svg)](https://www.python.org/downloads/release/python-390/)
[![TensorFlow](https://img.shields.io/badge/tensorflow-1.15-brightgreen.svg)]()

### arXiv preprint
```bibtex
@misc{https://doi.org/10.48550/arxiv.2302.12001,
	url =       {https://arxiv.org/abs/2302.12001},  	
  	title =     {Random Projection Forest Initialization for Graph Convolutional Networks},
	author =    {Alshammari, Mashaan and Stavrakakis, John and Ahmed, Adel F. and Takatsuka, Masahiro},
  	publisher = {arXiv},
  	year =      {2023}
}
```
### paper
```bibtex
@article{ALSHAMMARI2023102315,
	title = {Random Projection Forest Initialization for Graph Convolutional Networks},
	author = {Mashaan Alshammari and John Stavrakakis and Adel F. Ahmed and Masahiro Takatsuka}
	journal = {MethodsX},
	year = {2023},
	doi = {https://doi.org/10.1016/j.mex.2023.102315},	
}
```

### Files that we modified from the original [GCN](https://github.com/tkipf/gcn) code
- `\GCN\RPTree.py`
	- a code that returns an rpTree given a feature matrix X
- `\GCN\utils.py`
	- in line 99 we added a function called `load_data_rpForest` that returns an adjacency matrix based on rpForest
- `\GCN\train.py`
	- in line 29 we called the function `utils.load_data_rpForest` to work on adjacency matrix based on rpForest
	

### Files that we modified from the original [LDS](https://github.com/lucfra/LDS-GNN) code
- `\LDS\RPTree.py`
	- a code that returns an rpTree given a feature matrix X
- `\LDS\lds.py`
	- in line 302 we added a code that returns an adjacency matrix based on rpForest
- `\LDS\hyperparams.py`
	- in line 177 we added a code that randomly picks a percentage of edges that were missed by rpForest
	

## Setup

- Download and install Anaconda Navigator
- launch Anaconda Prompt and run the following commands:
	- `conda create -n tf15 python tensorflow=1.15`
	- `conda activate tf15`
	- `conda remove --force tensorflow-estimator`
	- `conda install -c anaconda tensorflow-estimator==1.15.1`
	- `conda install -c anaconda scikit-learn`
	- `conda install -c conda-forge munkres`
	- `conda install -c conda-forge python-annoy`
	- `conda install -c conda-forge keras==2.3.1`
	- `conda install -c anaconda spyder`

- To start working in this enviroment, launch Anaconda Prompt and type:
	- `activate tf15`
	- `spyder`
