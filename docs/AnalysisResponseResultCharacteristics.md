# AnalysisResponseResultCharacteristics


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**total_periods** | **int** |  | [optional] 
**non_zero_events** | **int** |  | [optional] 
**mean_value** | **float** |  | [optional] 
**std_deviation** | **float** |  | [optional] 
**trend_strength** | **float** |  | [optional] 
**seasonality_detected** | **bool** |  | [optional] 

## Example

```python
from forecastapi.models.analysis_response_result_characteristics import AnalysisResponseResultCharacteristics

# TODO update the JSON string below
json = "{}"
# create an instance of AnalysisResponseResultCharacteristics from a JSON string
analysis_response_result_characteristics_instance = AnalysisResponseResultCharacteristics.from_json(json)
# print the JSON string representation of the object
print(AnalysisResponseResultCharacteristics.to_json())

# convert the object into a dict
analysis_response_result_characteristics_dict = analysis_response_result_characteristics_instance.to_dict()
# create an instance of AnalysisResponseResultCharacteristics from a dict
analysis_response_result_characteristics_from_dict = AnalysisResponseResultCharacteristics.from_dict(analysis_response_result_characteristics_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


