# AnomalyDetectionResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**result** | [**AnomalyDetectionResponseResult**](AnomalyDetectionResponseResult.md) |  | [optional] 
**meta** | [**AnomalyDetectionResponseMeta**](AnomalyDetectionResponseMeta.md) |  | [optional] 

## Example

```python
from forecastapi.models.anomaly_detection_response import AnomalyDetectionResponse

# TODO update the JSON string below
json = "{}"
# create an instance of AnomalyDetectionResponse from a JSON string
anomaly_detection_response_instance = AnomalyDetectionResponse.from_json(json)
# print the JSON string representation of the object
print(AnomalyDetectionResponse.to_json())

# convert the object into a dict
anomaly_detection_response_dict = anomaly_detection_response_instance.to_dict()
# create an instance of AnomalyDetectionResponse from a dict
anomaly_detection_response_from_dict = AnomalyDetectionResponse.from_dict(anomaly_detection_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


