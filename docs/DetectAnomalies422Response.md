# DetectAnomalies422Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** |  | [optional] 
**errors** | **Dict[str, List[str]]** |  | [optional] 
**error** | **str** |  | [optional] 
**time_taken_ms** | **float** |  | [optional] 

## Example

```python
from forecastapi.models.detect_anomalies422_response import DetectAnomalies422Response

# TODO update the JSON string below
json = "{}"
# create an instance of DetectAnomalies422Response from a JSON string
detect_anomalies422_response_instance = DetectAnomalies422Response.from_json(json)
# print the JSON string representation of the object
print(DetectAnomalies422Response.to_json())

# convert the object into a dict
detect_anomalies422_response_dict = detect_anomalies422_response_instance.to_dict()
# create an instance of DetectAnomalies422Response from a dict
detect_anomalies422_response_from_dict = DetectAnomalies422Response.from_dict(detect_anomalies422_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


