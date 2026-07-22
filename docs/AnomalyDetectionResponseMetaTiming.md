# AnomalyDetectionResponseMetaTiming


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**validation** | **float** |  | [optional] 
**detection** | **float** |  | [optional] 
**total** | **float** |  | [optional] 

## Example

```python
from forecastapi.models.anomaly_detection_response_meta_timing import AnomalyDetectionResponseMetaTiming

# TODO update the JSON string below
json = "{}"
# create an instance of AnomalyDetectionResponseMetaTiming from a JSON string
anomaly_detection_response_meta_timing_instance = AnomalyDetectionResponseMetaTiming.from_json(json)
# print the JSON string representation of the object
print(AnomalyDetectionResponseMetaTiming.to_json())

# convert the object into a dict
anomaly_detection_response_meta_timing_dict = anomaly_detection_response_meta_timing_instance.to_dict()
# create an instance of AnomalyDetectionResponseMetaTiming from a dict
anomaly_detection_response_meta_timing_from_dict = AnomalyDetectionResponseMetaTiming.from_dict(anomaly_detection_response_meta_timing_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


