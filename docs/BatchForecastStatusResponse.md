# BatchForecastStatusResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**identifier** | **str** | The batch id | [optional] 
**status** | **str** |  | [optional] 
**batch_parts** | **int** | Number of parts the batch was split into for processing | [optional] 
**results** | [**BatchForecastStatusResponseResults**](BatchForecastStatusResponseResults.md) |  | [optional] 
**parts** | [**List[BatchForecastStatusResponsePartsInner]**](BatchForecastStatusResponsePartsInner.md) | Per-part progress metadata (the forecasts themselves live under results.data) | [optional] 
**started_at** | **datetime** |  | [optional] 
**completed_at** | **datetime** |  | [optional] 
**created_at** | **datetime** |  | [optional] 
**updated_at** | **datetime** |  | [optional] 

## Example

```python
from forecastapi.models.batch_forecast_status_response import BatchForecastStatusResponse

# TODO update the JSON string below
json = "{}"
# create an instance of BatchForecastStatusResponse from a JSON string
batch_forecast_status_response_instance = BatchForecastStatusResponse.from_json(json)
# print the JSON string representation of the object
print(BatchForecastStatusResponse.to_json())

# convert the object into a dict
batch_forecast_status_response_dict = batch_forecast_status_response_instance.to_dict()
# create an instance of BatchForecastStatusResponse from a dict
batch_forecast_status_response_from_dict = BatchForecastStatusResponse.from_dict(batch_forecast_status_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


