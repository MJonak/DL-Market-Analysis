## Deep Learning Market Analysis

This project is an attempt to use historical market data to train different deep learning models to spot profitable trades and profit.


# Design

In the repo you can find 4 top level folders:
 - dl-market-analysis
 - experiments
 - docs
 - tests

The dl-market-analysis folder contains the source code for the solution

The experiments folder contains jupyter notebooks with the experiments carried out with various deep learning models as well as various hyperparameter configurations. This is also where plots of graphs, charts and tables can be found displaying experiment results.

The docs folder naturally contains the documentation

The test folder contains the unit test suite


Deep Learning Pipeline:
----------------------
- Gather Data
- Prepare it for trianing
- Divive dataset into 3
- Define & compile model
- Train Model
- Tune Hyperparameters
- Deploy

The functions required are:
- Functions to gather data from the web 
- (AND) Functions to convert files into a set format
- Functions to divide the dataset (due to the time series nature, can't just randomly split the data)


- Do we want to store them in just a set order of numbers, or do we want a custom object which can be serialised into a tensor?
- Probably best to have a custom class which represents a candle, which will be stored in a chart class as a list of candles, we can then incorporate indicator classes into both the candle and the chart class to calculate important indicators which rely on previous candles.


Gathering data from EATradingAcademy for initial attempt, probably incorporate this to an api with live prices upon deployment.


# Initial Setup

This project requires poetry to be initialised. See https://python-poetry.org/docs/basic-usage/ for usage instructions. 

After cloning this repository down, from the root project directory run:

`poetry init`

To ensure packages are recognised by your IDE set the python interpreter to the one found at the path given by: 

`poetry env info --path`

# Usual Usage

As this project uses poetry, scripts should be ran via the poetry shell:

(from root directory)
`poetry shell`

Then execute scripts as usual via this shell to access poetry venv. 
For correct functionalty of jupyter notebooks run `jupyter notebook` from within this shell.
