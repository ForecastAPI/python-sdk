# BatchForecastStatusResponsePartsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**status** | **str** |  | [optional] 
**started_at** | **datetime** |  | [optional] 
**completed_at** | **datetime** |  | [optional] 

## Example

```python
from forecastapi.models.batch_forecast_status_response_parts_inner import BatchForecastStatusResponsePartsInner

# TODO update the JSON string below
json = "{}"
# create an instance of BatchForecastStatusResponsePartsInner from a JSON string
batch_forecast_status_response_parts_inner_instance = BatchForecastStatusResponsePartsInner.from_json(json)
# print the JSON string representation of the object
print(BatchForecastStatusResponsePartsInner.to_json())

# convert the object into a dict
batch_forecast_status_response_parts_inner_dict = batch_forecast_status_response_parts_inner_instance.to_dict()
# create an instance of BatchForecastStatusResponsePartsInner from a dict
batch_forecast_status_response_parts_inner_from_dict = BatchForecastStatusResponsePartsInner.from_dict(batch_forecast_status_response_parts_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


