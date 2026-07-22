# AnalysisResponseMeta


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**timing** | [**AnalysisResponseMetaTiming**](AnalysisResponseMetaTiming.md) |  | [optional] 

## Example

```python
from forecastapi.models.analysis_response_meta import AnalysisResponseMeta

# TODO update the JSON string below
json = "{}"
# create an instance of AnalysisResponseMeta from a JSON string
analysis_response_meta_instance = AnalysisResponseMeta.from_json(json)
# print the JSON string representation of the object
print(AnalysisResponseMeta.to_json())

# convert the object into a dict
analysis_response_meta_dict = analysis_response_meta_instance.to_dict()
# create an instance of AnalysisResponseMeta from a dict
analysis_response_meta_from_dict = AnalysisResponseMeta.from_dict(analysis_response_meta_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


