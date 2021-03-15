# Computational Neural Network Model of Cholinergic Activity in the Hippocampus

This project aims to model the effect of variable acetylcholine levels in the human hippocampus on pattern separation task performance. The underlying hippocampal model is a modified version of the [Emergent HPC Model](https://github.com/CompCogNeuro/sims/tree/master/ch8/hip) which was based on [Ketz et al. (2013)](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1003067). The research accompanying this model can be found [here](https://blog.alexgordienko.com/nnm/).

## Getting Started

These instructions will get you a copy of the project up and running on your local machine.

### Prerequisites

As the model is written in `Golang`, please have this installed first: [https://golang.org/doc/install](https://golang.org/doc/install)

Next, install Emergent (GoGi and Leabra) using these instructions: [https://github.com/emer/emergent/wiki/Install](https://github.com/emer/emergent/wiki/Install)

### Installing

Next, clone this repository to your preferred directory and run it.

Start by `cd`ing to your preferred directory.

```
git clone https://github.com/AlexGordienko/hip-ACh
```

To run the model with the graphical interface:

```
cd hip-ACh
go build
./hip-ACh
```

From here you should see the graphical interface pop up. In this window, click `Train` to begin. There's lots to do here, so check out the [CCN Lab's Textbook](https://github.com/CompCogNeuro/ed4) to get started learning.

## Running existing stimulus sets

If you want to run the model with a dataset of your choosing from the `stimuli` folder, begin by installing `go-bindata` here: [https://github.com/shuLhan/go-bindata](https://github.com/shuLhan/go-bindata). Now, make sure you are `cd`'ed into this project's home directory and run

```
./go-bindata ./stimuli/[YOUR SELECTED DATASET]/test_ab_ps.tsv ./stimuli/[YOUR SELECTED DATASET]/train_ab_ps.tsv
```

From here you can 
```
go build
./hip-ACh
```
as usual. 

## Running your own stimulus sets

If you would like to create and run your own dataset on this model, I would recommend building the dataset with this [dataset creation tool](https://github.com/AlexGordienko/NNM-Dataset-Creation-Tool). You can then place the outputed `.tsv` files into a folder under `stimuli` and bind the files as shown above. I would recommend that you conserve the naming convention of `train_ab_ps.tsv`, `test_ab_ps.tsv` for your training and testing variants so that you don't need to modify any code to try them out. 

## Author

* **Alex Gordienko** - *Initial work* - [Website](https://alexgordienko.com/)