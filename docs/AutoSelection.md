# AutoSelection

Present only when `model: auto` was requested — which model actually answered, and why. On /v2/forecast and batch results it appears inside `model_info`; on /v2/inventory-planning and /v2/traffic-forecasting it appears under `meta`. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**requested** | **str** |  | [optional] 
**selected** | **str** | The model that produced this response | [optional] 
**reason** | **str** | Why this model was selected. &#x60;scored_winner&#x60; means one model beat every alternative by a clear margin on realized accuracy for this identifier; everything else means the evidence-gathering default was served.  | [optional] 
**scores** | [**Dict[str, AutoSelectionScoresValue]**](AutoSelectionScoresValue.md) | Per-model realized-accuracy scorecard for this identifier, when one exists | [optional] 

## Example

```python
from forecastapi.models.auto_selection import AutoSelection

# TODO update the JSON string below
json = "{}"
# create an instance of AutoSelection from a JSON string
auto_selection_instance = AutoSelection.from_json(json)
# print the JSON string representation of the object
print(AutoSelection.to_json())

# convert the object into a dict
auto_selection_dict = auto_selection_instance.to_dict()
# create an instance of AutoSelection from a dict
auto_selection_from_dict = AutoSelection.from_dict(auto_selection_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


