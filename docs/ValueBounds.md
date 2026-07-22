# ValueBounds

The range the series cannot leave — a rate has both sides, a backlog only a floor. At least one side must be declared, and min must be less than max. The series is forecast on a transformed scale and mapped back, so the point, both bounds and every quantile land inside the range and the band takes the right asymmetric shape near a bound. Checked against the series' own history: bounds the history already contradicts are rejected up front (usually a unit mismatch, e.g. 0–1 rates declared as 0–100). Honoured by /v2/forecast and /v2/batch/forecast (request-level default or per-series override); rejected on grouped forecasts; ignored by other endpoints sharing this request shape. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**min** | **float** | Floor the series cannot go below | [optional] 
**max** | **float** | Ceiling the series cannot exceed | [optional] 

## Example

```python
from forecastapi.models.value_bounds import ValueBounds

# TODO update the JSON string below
json = "{}"
# create an instance of ValueBounds from a JSON string
value_bounds_instance = ValueBounds.from_json(json)
# print the JSON string representation of the object
print(ValueBounds.to_json())

# convert the object into a dict
value_bounds_dict = value_bounds_instance.to_dict()
# create an instance of ValueBounds from a dict
value_bounds_from_dict = ValueBounds.from_dict(value_bounds_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


