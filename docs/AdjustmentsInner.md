# AdjustmentsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **str** | multiplier scales the value; level_shift adds a constant | 
**value** | **float** | The factor or the offset. A multiplier must be zero or greater. | 
**from_period** | **int** | Optional 1-based inclusive start of the window; omit to start at period 1 | [optional] 
**to_period** | **int** | Optional 1-based inclusive end of the window; omit to run to the horizon. Must fall within &#x60;periods&#x60;. | [optional] 

## Example

```python
from forecastapi.models.adjustments_inner import AdjustmentsInner

# TODO update the JSON string below
json = "{}"
# create an instance of AdjustmentsInner from a JSON string
adjustments_inner_instance = AdjustmentsInner.from_json(json)
# print the JSON string representation of the object
print(AdjustmentsInner.to_json())

# convert the object into a dict
adjustments_inner_dict = adjustments_inner_instance.to_dict()
# create an instance of AdjustmentsInner from a dict
adjustments_inner_from_dict = AdjustmentsInner.from_dict(adjustments_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


