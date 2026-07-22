# AnomalyDetectionResponseResultAnalysis


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**method_used** | **str** |  | [optional] 
**confidence** | **str** | Confidence in the method selection; \&quot;user_specified\&quot; when a method was named in the request | [optional] 
**reason** | **str** |  | [optional] 
**data_characteristics** | **Dict[str, object]** | Statistical profile of the data (present on auto selection) | [optional] 
**detection_summary** | [**AnomalyDetectionResponseResultAnalysisDetectionSummary**](AnomalyDetectionResponseResultAnalysisDetectionSummary.md) |  | [optional] 

## Example

```python
from forecastapi.models.anomaly_detection_response_result_analysis import AnomalyDetectionResponseResultAnalysis

# TODO update the JSON string below
json = "{}"
# create an instance of AnomalyDetectionResponseResultAnalysis from a JSON string
anomaly_detection_response_result_analysis_instance = AnomalyDetectionResponseResultAnalysis.from_json(json)
# print the JSON string representation of the object
print(AnomalyDetectionResponseResultAnalysis.to_json())

# convert the object into a dict
anomaly_detection_response_result_analysis_dict = anomaly_detection_response_result_analysis_instance.to_dict()
# create an instance of AnomalyDetectionResponseResultAnalysis from a dict
anomaly_detection_response_result_analysis_from_dict = AnomalyDetectionResponseResultAnalysis.from_dict(anomaly_detection_response_result_analysis_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


