# e#-#gdp3_basic_fw_0_0_inbestsol-fwpredNEW.csv
Each zip file contains a data instance, with a given number of vehicles, ranging from 3 to 300.

Each file contains the following columns:
- `scenario`, `pred_direction`, `date`, `weekday`, `week-of-the-year`, `month`, `year`, `solver`: Information about the data generation process. Refer to [G. Agliardi et al., "A Machine Learning Approach to Boost the Vehicle-2-Grid Scheduling," 2024 IEEE Sustainable Power and Energy Conference (iSPEC), Kuching, Sarawak, Malaysia, 2024, pp. 670-675, doi: 10.1109/iSPEC59716.2024.10892547](https://doi.org/10.1109/iSPEC59716.2024.10892547) for more information
- `time-to-go`: The record is reffered to the point in time that happens `time-to-go` time steps before the end of the planning horizon
- `best-aggr-action`: Best action to take at the given point in time, under the given conditions, according to the solver used. **This is the target of the prediction.**
- `in-best-solution`: Always flagged
- `volume-48..volume+47`: Volume at current time +/-t
- `underdelivery_price-48..underdelivery_price+47`: Price (per unit of energy) or penalty for delivering less energy than needed at current time +/-t. (*) See note at the bottom.
- `overdelivery_price-48..overdelivery_price+47`: Price (per unit of energy) or penalty for delivering more energy than needed at current time +/-t. (*) See note at the bottom.
- `volume0..volume47`: Volume at absolute time t
- `underdelivery_price0..underdelivery_price47`: Price or penalty of underdelivery at absolute time t. (*) See note at the bottom.
- `overdelivery_price0..overdelivery_price47`: Price or penalty of overdelivery at absolute time t. (*) See note at the bottom.
- `aggr-soc, soc-var, soc-std, soc-kurt, soc-skew, soc-min, soc-max, soc-q05, soc-q15, soc-q30, soc-q70, soc-q85, soc-q95`: Statistics of the state of charge at current time (sum, variance, std, kurt, skew, min, max, quantiles)

(*) All prices have been removed due to copyright restrictions. An `X` was put as a placeholder for removed data. Empty cells marks missing data from the original file. To reconstruct the original dataset, all `X` values should be replaced with the intraday price of energy at that date/time (for underdelivery), or with 10x the intraday price (for overdelivery).