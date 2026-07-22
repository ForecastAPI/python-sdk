# AnomalyDetectionResponseResultAnomaliesInner

Method-specific fields (z_score, deviation, iqr_multiple, …) accompany the common ones below

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**index** | **int** | Position of the point in the submitted data | [optional] 
**var_date** | **str** |  | [optional] 
**value** | **float** |  | [optional] 
**expected_range** | **Dict[str, object]** | The range the point was expected to fall within | [optional] 
**severity** | **str** |  | [optional] 
**type** | **str** | spike/dip for zscore, outlier_high/outlier_low for iqr, seasonal variants for seasonal | [optional] 

## Example

```python
from forecastapi.models.anomaly_detection_response_result_anomalies_inner import AnomalyDetectionResponseResultAnomaliesInner

# TODO update the JSON string below
json = "{}"
# create an instance of AnomalyDetectionResponseResultAnomaliesInner from a JSON string
anomaly_detection_response_result_anomalies_inner_instance = AnomalyDetectionResponseResultAnomaliesInner.from_json(json)
# print the JSON string representation of the object
print(AnomalyDetectionResponseResultAnomaliesInner.to_json())

# convert the object into a dict
anomaly_detection_response_result_anomalies_inner_dict = anomaly_detection_response_result_anomalies_inner_instance.to_dict()
# create an instance of AnomalyDetectionResponseResultAnomaliesInner from a dict
anomaly_detection_response_result_anomalies_inner_from_dict = AnomalyDetectionResponseResultAnomaliesInner.from_dict(anomaly_detection_response_result_anomalies_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


