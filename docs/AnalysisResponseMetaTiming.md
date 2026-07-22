# AnalysisResponseMetaTiming


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**validation** | **float** | Time taken for validation in milliseconds | [optional] 
**analysing** | **float** | Time taken for analysis in milliseconds | [optional] 
**total** | **float** | Total processing time in milliseconds | [optional] 

## Example

```python
from forecastapi.models.analysis_response_meta_timing import AnalysisResponseMetaTiming

# TODO update the JSON string below
json = "{}"
# create an instance of AnalysisResponseMetaTiming from a JSON string
analysis_response_meta_timing_instance = AnalysisResponseMetaTiming.from_json(json)
# print the JSON string representation of the object
print(AnalysisResponseMetaTiming.to_json())

# convert the object into a dict
analysis_response_meta_timing_dict = analysis_response_meta_timing_instance.to_dict()
# create an instance of AnalysisResponseMetaTiming from a dict
analysis_response_meta_timing_from_dict = AnalysisResponseMetaTiming.from_dict(analysis_response_meta_timing_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


