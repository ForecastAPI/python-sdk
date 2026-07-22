# AnalysisResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**result** | [**AnalysisResponseResult**](AnalysisResponseResult.md) |  | [optional] 
**meta** | [**AnalysisResponseMeta**](AnalysisResponseMeta.md) |  | [optional] 

## Example

```python
from forecastapi.models.analysis_response import AnalysisResponse

# TODO update the JSON string below
json = "{}"
# create an instance of AnalysisResponse from a JSON string
analysis_response_instance = AnalysisResponse.from_json(json)
# print the JSON string representation of the object
print(AnalysisResponse.to_json())

# convert the object into a dict
analysis_response_dict = analysis_response_instance.to_dict()
# create an instance of AnalysisResponse from a dict
analysis_response_from_dict = AnalysisResponse.from_dict(analysis_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


