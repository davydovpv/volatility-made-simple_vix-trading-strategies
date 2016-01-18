* This folder contains the strategy scripts, backtesting script and
the data generation script.

* data_generation.R:

The data generation script is run whenever we want to add some new
time series to the final all time series assimilated data set. 

The data which was used to generate the master data set and final
master data set are all located in '../data/' folder.

* backtest_strategy.R:
This script backtests strategies on the final data set and returns the
time series of portfolio returns.

This script runs from command line.

An example run would be like -
Rscript ./backtest_strategy.R [strategy path] [output path (return vector)]

* strategy_*.R 

These are the strategy scripts.  

The file name is the name of the strategy as per the June strategies
listed on voltility-made-simple.

Each strategy is an independent function and can be ran using the
backtest_strategy.R script

eg: If one wants to run strategy_DFTB_sd.R, then the following command
would give one the returns time series for this strategy.

Rscript ./backtest_strategy.R ./strategy_DFTB_sd.R ../strategy_results/DFTB_sd.RData