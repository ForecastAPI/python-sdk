# AnalysisResponseResult


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**pattern_type** | **str** |  | [optional] 
**characteristics** | [**AnalysisResponseResultCharacteristics**](AnalysisResponseResultCharacteristics.md) |  | [optional] 
**recommended_methods** | **List[str]** |  | [optional] 
**confidence** | **str** |  | [optional] 

## Example

```python
from forecastapi.models.analysis_response_result import AnalysisResponseResult

# TODO update the JSON string below
json = "{}"
# create an instance of AnalysisResponseResult from a JSON string
analysis_response_result_instance = AnalysisResponseResult.from_json(json)
# print the JSON string representation of the object
print(AnalysisResponseResult.to_json())

# convert the object into a dict
analysis_response_result_dict = analysis_response_result_instance.to_dict()
# create an instance of AnalysisResponseResult from a dict
analysis_response_result_from_dict = AnalysisResponseResult.from_dict(analysis_response_result_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


