# DetectAnomalies500Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**error** | **str** |  | [optional] 
**time_taken_ms** | **float** |  | [optional] 

## Example

```python
from forecastapi.models.detect_anomalies500_response import DetectAnomalies500Response

# TODO update the JSON string below
json = "{}"
# create an instance of DetectAnomalies500Response from a JSON string
detect_anomalies500_response_instance = DetectAnomalies500Response.from_json(json)
# print the JSON string representation of the object
print(DetectAnomalies500Response.to_json())

# convert the object into a dict
detect_anomalies500_response_dict = detect_anomalies500_response_instance.to_dict()
# create an instance of DetectAnomalies500Response from a dict
detect_anomalies500_response_from_dict = DetectAnomalies500Response.from_dict(detect_anomalies500_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


