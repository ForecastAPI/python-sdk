# GroupedForecastAccepted


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**grouped_forecast_id** | **str** | Id to poll via GET /v2/forecast/grouped/{grouped_forecast_id} | [optional] 
**status** | **str** |  | [optional] 
**series_count** | **int** | Leaf series submitted | [optional] 
**node_count** | **int** | What will actually be forecast and reconciled — the leaves plus every derived aggregate and the total | [optional] 
**reconciliation** | **str** |  | [optional] 
**time_taken_ms** | **float** |  | [optional] 

## Example

```python
from forecastapi.models.grouped_forecast_accepted import GroupedForecastAccepted

# TODO update the JSON string below
json = "{}"
# create an instance of GroupedForecastAccepted from a JSON string
grouped_forecast_accepted_instance = GroupedForecastAccepted.from_json(json)
# print the JSON string representation of the object
print(GroupedForecastAccepted.to_json())

# convert the object into a dict
grouped_forecast_accepted_dict = grouped_forecast_accepted_instance.to_dict()
# create an instance of GroupedForecastAccepted from a dict
grouped_forecast_accepted_from_dict = GroupedForecastAccepted.from_dict(grouped_forecast_accepted_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


