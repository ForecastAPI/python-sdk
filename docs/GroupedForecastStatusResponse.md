# GroupedForecastStatusResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**grouped_forecast_id** | **str** |  | [optional] 
**status** | **str** | The run is all-or-nothing — there is no per-node failure state | [optional] 
**node_count** | **int** |  | [optional] 
**results** | [**GroupedForecastResults**](GroupedForecastResults.md) | Populated once status is &#x60;completed&#x60;; null before that and on failure | [optional] 
**error** | **str** | Failure reason when status is &#x60;failed&#x60; | [optional] 
**started_at** | **datetime** |  | [optional] 
**completed_at** | **datetime** |  | [optional] 
**created_at** | **datetime** |  | [optional] 

## Example

```python
from forecastapi.models.grouped_forecast_status_response import GroupedForecastStatusResponse

# TODO update the JSON string below
json = "{}"
# create an instance of GroupedForecastStatusResponse from a JSON string
grouped_forecast_status_response_instance = GroupedForecastStatusResponse.from_json(json)
# print the JSON string representation of the object
print(GroupedForecastStatusResponse.to_json())

# convert the object into a dict
grouped_forecast_status_response_dict = grouped_forecast_status_response_instance.to_dict()
# create an instance of GroupedForecastStatusResponse from a dict
grouped_forecast_status_response_from_dict = GroupedForecastStatusResponse.from_dict(grouped_forecast_status_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


