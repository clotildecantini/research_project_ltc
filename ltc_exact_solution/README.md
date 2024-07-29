# Customer Feedback classifier 

This repository aims to implement our exact soltuion for LTC neural network with neuron whose dynamics is governed by an ODE.

Make sure you are in the folder of the project after cloning.

## Installation

Create the conda environment and install the package:

```bash
conda create -n ltc_env pip python=3.12
conda activate ltc_env
pip install .
```

If you want to install the package in  developement mode you can do : 

```bash
conda create -n ltc_env_dev pip python=3.12

conda activate ltc_env_dev
pip install -e .
```

## Instructions 

If you want to launch the experiment for a neuron index, type in the terminal : 


```bash
python3 script_experiment.py 0
```

Neuron index should be a int. First neuron is denoted by index 0.

This script require to have solved the odeint for this specific experiment, so before, make sure you ran the corresponding file. 

If you want to run the experiment for random input (you can modifiy number of synapse and time steps in the script) :

```bash
python3 odeint_solver_script.py random 
```

If you want to run the experiment for ecg input :

```bash
python3 odeint_solver_script.py ecg 
```

If you want to run the experiment for hasani data, you can choose the index of the neuron you want to solve the dynamic of :

```bash
python3 odeint_solver_script.py 10
```
To run the experiment you need to download the data provided by Hasani on the associated repository : 

[https://github.com/raminmh/CfC]


These are provided in the Matlab file. The structure of the experiment rely on this exact format.

## Download and Extract Dataset

To download and extract the MIT-BIH Arrhythmia Database (ECG data), run the following command in your terminal:

```bash
wget https://www.physionet.org/static/published-projects/mitdb/mit-bih-arrhythmia-database-1.0.0.zip && unzip mit-bih-arrhythmia-database-1.0.0.zip && rm mit-bih-arrhythmia-database-1.0.0.zip