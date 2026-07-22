# AnomalyDetectionResponseMeta


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**timing** | [**AnomalyDetectionResponseMetaTiming**](AnomalyDetectionResponseMetaTiming.md) |  | [optional] 

## Example

```python
from forecastapi.models.anomaly_detection_response_meta import AnomalyDetectionResponseMeta

# TODO update the JSON string below
json = "{}"
# create an instance of AnomalyDetectionResponseMeta from a JSON string
anomaly_detection_response_meta_instance = AnomalyDetectionResponseMeta.from_json(json)
# print the JSON string representation of the object
print(AnomalyDetectionResponseMeta.to_json())

# convert the object into a dict
anomaly_detection_response_meta_dict = anomaly_detection_response_meta_instance.to_dict()
# create an instance of AnomalyDetectionResponseMeta from a dict
anomaly_detection_response_meta_from_dict = AnomalyDetectionResponseMeta.from_dict(anomaly_detection_response_meta_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


