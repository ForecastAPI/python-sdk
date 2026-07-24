# AutoSelectionScoresValue


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**mase** | **float** | Realized MASE on this identifier (lower is better; &lt; 1 beats a naive forecast) | [optional] 
**matched_periods** | **int** | Matured forecast/actual pairs behind the score | [optional] 
**forecast_runs** | **int** | Separate forecast runs the evidence spans | [optional] 

## Example

```python
from forecastapi.models.auto_selection_scores_value import AutoSelectionScoresValue

# TODO update the JSON string below
json = "{}"
# create an instance of AutoSelectionScoresValue from a JSON string
auto_selection_scores_value_instance = AutoSelectionScoresValue.from_json(json)
# print the JSON string representation of the object
print(AutoSelectionScoresValue.to_json())

# convert the object into a dict
auto_selection_scores_value_dict = auto_selection_scores_value_instance.to_dict()
# create an instance of AutoSelectionScoresValue from a dict
auto_selection_scores_value_from_dict = AutoSelectionScoresValue.from_dict(auto_selection_scores_value_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


