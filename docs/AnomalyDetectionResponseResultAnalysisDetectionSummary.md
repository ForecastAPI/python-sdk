# AnomalyDetectionResponseResultAnalysisDetectionSummary

Present on auto selection

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**total_points** | **int** |  | [optional] 
**anomalies_found** | **int** |  | [optional] 
**anomaly_percentage** | **float** |  | [optional] 
**severity_distribution** | **Dict[str, int]** |  | [optional] 

## Example

```python
from forecastapi.models.anomaly_detection_response_result_analysis_detection_summary import AnomalyDetectionResponseResultAnalysisDetectionSummary

# TODO update the JSON string below
json = "{}"
# create an instance of AnomalyDetectionResponseResultAnalysisDetectionSummary from a JSON string
anomaly_detection_response_result_analysis_detection_summary_instance = AnomalyDetectionResponseResultAnalysisDetectionSummary.from_json(json)
# print the JSON string representation of the object
print(AnomalyDetectionResponseResultAnalysisDetectionSummary.to_json())

# convert the object into a dict
anomaly_detection_response_result_analysis_detection_summary_dict = anomaly_detection_response_result_analysis_detection_summary_instance.to_dict()
# create an instance of AnomalyDetectionResponseResultAnalysisDetectionSummary from a dict
anomaly_detection_response_result_analysis_detection_summary_from_dict = AnomalyDetectionResponseResultAnalysisDetectionSummary.from_dict(anomaly_detection_response_result_analysis_detection_summary_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


