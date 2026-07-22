# AnomalyDetectionRequestAllOfAnomalySettings

Optional detection configuration; omit for automatic method selection

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**method** | **str** | Detection method; auto picks the best fit for the data&#39;s characteristics | [optional] [default to 'auto']
**threshold** | **float** | Z-score threshold for the zscore method | [optional] 
**multiplier** | **float** | IQR multiplier for the iqr method | [optional] 
**seasonal_period** | **int** | Season length for the seasonal method; detected automatically when omitted | [optional] 
**minimum_periods** | **int** | Minimum data points required before detection runs | [optional] 

## Example

```python
from forecastapi.models.anomaly_detection_request_all_of_anomaly_settings import AnomalyDetectionRequestAllOfAnomalySettings

# TODO update the JSON string below
json = "{}"
# create an instance of AnomalyDetectionRequestAllOfAnomalySettings from a JSON string
anomaly_detection_request_all_of_anomaly_settings_instance = AnomalyDetectionRequestAllOfAnomalySettings.from_json(json)
# print the JSON string representation of the object
print(AnomalyDetectionRequestAllOfAnomalySettings.to_json())

# convert the object into a dict
anomaly_detection_request_all_of_anomaly_settings_dict = anomaly_detection_request_all_of_anomaly_settings_instance.to_dict()
# create an instance of AnomalyDetectionRequestAllOfAnomalySettings from a dict
anomaly_detection_request_all_of_anomaly_settings_from_dict = AnomalyDetectionRequestAllOfAnomalySettings.from_dict(anomaly_detection_request_all_of_anomaly_settings_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


