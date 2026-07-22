# AnomalyDetectionResponseResult


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**anomalies** | [**List[AnomalyDetectionResponseResultAnomaliesInner]**](AnomalyDetectionResponseResultAnomaliesInner.md) | Detected anomalies, most severe first | [optional] 
**analysis** | [**AnomalyDetectionResponseResultAnalysis**](AnomalyDetectionResponseResultAnalysis.md) |  | [optional] 
**alternatives** | **List[Dict[str, object]]** | Other suitable methods (present on auto selection) | [optional] 
**statistics** | **Dict[str, object]** | Method statistics (present when a method was named in the request) | [optional] 
**interpretation** | **Dict[str, object]** | Human-readable interpretation (present when a method was named in the request) | [optional] 

## Example

```python
from forecastapi.models.anomaly_detection_response_result import AnomalyDetectionResponseResult

# TODO update the JSON string below
json = "{}"
# create an instance of AnomalyDetectionResponseResult from a JSON string
anomaly_detection_response_result_instance = AnomalyDetectionResponseResult.from_json(json)
# print the JSON string representation of the object
print(AnomalyDetectionResponseResult.to_json())

# convert the object into a dict
anomaly_detection_response_result_dict = anomaly_detection_response_result_instance.to_dict()
# create an instance of AnomalyDetectionResponseResult from a dict
anomaly_detection_response_result_from_dict = AnomalyDetectionResponseResult.from_dict(anomaly_detection_response_result_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


