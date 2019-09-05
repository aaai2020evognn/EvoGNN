# Evolutionary Graph Neural Networks

**Description: This repository contains the reference implementation of the EvoGNN model proposed in paper *Evolutionary Graph Neural Networks* submitted to AAAI 2020**

## Usage
### 1. Environment
This project uses `python3` and `PyTorch` (<https://pytorch.org/>). Please make sure you have installed all necessary packages specified in `./requirements.txt` file.
You can install pacakages by
```
pip install -r ./requirements.txt
```

### 2. Execute
To run the **EvoGNN** model on D^(2K) dataset:
```
python main.py --dataset 2k --K 2
```
List of parameters:
+ --dataset: Specify the dataset to use (`2k` or `10k`)
+ --t_0: Start index of available time points; default is 0.
+ --T: Length of available training time points; default is 8.
+ --t_train: Length of training time points (from --t_0); default is 8.
+ --K: Num of layers fusing new time point; default is 2.
+ --epochs: Number of epochs for training; default is 10.
+ --H_0_npf: File for initializing H_0; default is `./emb/H_0.2k.npy`.

## Data
The `./data/` folder contains all files for the D^(2K) dataset. Due to size constraints, files for the D^(10K) dataset are compressed in `./data/data_10k.zip`. If you need to run on the D^(10K) dataset, please decompress the zip file and ensure all `.csv` files are directly under `./data/`. 

## Example
Other examples are provided in the `./example.sh` file.

## Acknowledgement
We thank the anonymous reviewers for providing suggestions to this original paper *Evolutionary Graph Neural Networks*.
