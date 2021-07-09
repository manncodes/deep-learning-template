# Pytorch Deep Learning Template

The main features are:

- modularity: we split each logic piece into a different python submodule
- data-augmentation: we included [imgaug](https://imgaug.readthedocs.io/en/latest/)
- ready to go: by using [poutyne](https://pypi.org/project/Poutyne/) a Keras-like framework you don't have to write any train loop.
- [torchsummary](https://github.com/sksq96/pytorch-summary) to show a summary of your models
- reduce the learning rate on a plateau
- auto-saving the best model
- experiment tracking with [comet](https://www.comet.ml/)
- logging using python [logging](https://docs.python.org/3/library/logging.html) module
- a playground notebook to quick test/play around

## Installation

Clone the repo and go inside it. Then, run:

```bash
pip install -r requirements.txt
```

## Structure

The template is inside `./template`.

```bash
.
├── callbacks // here you can create your custom callbacks
├── checkpoint // were we store the trained models
├── data // here we define our dataset
│ └── transformation // custom transformation, e.g. resize and data augmentation
├── dataset // the data
│ ├── train
│ └── val
├── logger.py // were we define our logger
├── losses // custom losses
├── main.py
├── models // here we create our models
│ ├── MyCNN.py
│ ├── resnet.py
│ └── utils.py
├── playground.ipynb // a notebook that can be used to fast experiment with things
├── Project.py // a class that represents the project structure
├── README.md
├── requirements.txt
├── test // you should always perform some basic testing
│ └── test_myDataset.py
└── utils.py // utilities functions
```

### Keep your structure clean and concise

Every deep learning project has at least three mains steps:

- data gathering/processing
- modeling
- training/evaluating
