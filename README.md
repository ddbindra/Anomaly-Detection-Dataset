# Anomaly Detection in Time Series Datasets
*author: Dhruv Bindra

## Dataset
This dataset is provided as part of the Yahoo Webscope program, to be used for approved non-commercial research purposes by recipients who have signed a Data Sharing Agreement with Yahoo! Dataset contains real and synthetic time-series with labeled anomalies. Timestamps are replaced by integers with an increment of 1, where each data-point represents 1 hour worth of data. The dataset contains 15 anomalies which are marked by humans and therefore may not be consistent. We decided to choose this dataset because there was a high probability that we would face those kind of task in real live.

Time-series used to evaluate model performance is based on real production traffic of some of the Yahoo! properties. These time series have different scales and length, thus we will be testing models on one of the times series in the dataset. This simplifies anomaly detection task that are produced only by one of the Yahoo! properties. Finding anomalies in other series requires specialized parameter tuning as parameters aren't universal and can't produce models that find anomalies from different sources (there ain't no such thing as a free lunch).

**The dataset fields are:**
* *timestamp*
* *value*
* *is_anomaly*
* *predicted*
    
The is_anomaly field is a boolean indicating if the current value at a given timestamp is considered an anomaly.

The predicted is a real value prediction coming from a black box forecasting model for that timestamp. This black box forecasting model is assumed to be aware of only the true data distribution.


**Dataset snippet:**

```
  timestamp value is_anomaly  predicted
1         1  5.86          0    44.0725
2         2  5.95          0   50.70939
3         3  5.92          0   81.40512
4         4  5.47          0  39.950367
5         5  5.77          0   35.35016
6         6  5.73          0  27.713638
```
