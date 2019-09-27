# Team Data Preparator - LEC Data Challenge 2019

[![License](https://img.shields.io/badge/License-AGPL%203.0-yellow?style=popout-square)](LICENSE.txt)

This is the source code of **Team Data Preparator** for the [1st LEC Data Challenge](https://www.lec.at/lec-data-challenge-2019/).

:2nd_place_medal: This solution reached the **2nd place** in the competition.

You may want to check out the following:

- [Presentation slides](presentation-armax-forecasting-2019.pdf)
- [Jupyter notebook](lec-data-challenge.ipynb) - [HTML](lec-data-challenge.html)

:mag: :mag: :mag:

The task was to detect faults in sensor measurements.

Our solution forecasts the sensor measurements and flags regions if the real values significantly deviate from the forecast. 
We train an ensemble of [ARMAX models](https://en.wikipedia.org/wiki/Autoregressive%E2%80%93moving-average_model#Autoregressive%E2%80%93moving-average_model_with_exogenous_inputs_model_(ARMAX_model)) and combine their predictions with a [weigthed median](https://en.wikipedia.org/wiki/Weighted_median), where the weights are based on the [Spearman's rank correlation coefficient](https://en.wikipedia.org/wiki/Spearman%27s_rank_correlation_coefficient) of the sensors, along with a bit of post-processing filter magic.

## Requirements

### Python 3.7

Package requirements are specified in the [requirements.txt](requirements.txt) file.

```
pip3 install -r requirements.txt
```
