# BatchForecastAccepted


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**batch_id** | **str** | Id to poll via GET /v2/batch/forecast/{batch_id} | [optional] 
**status** | **str** |  | [optional] 
**series_count** | **int** | Number of series accepted. Present on inline submissions; a file-based submission counts its series during processing. | [optional] 
**time_taken_ms** | **float** |  | [optional] 

## Example

```python
from forecastapi.models.batch_forecast_accepted import BatchForecastAccepted

# TODO update the JSON string below
json = "{}"
# create an instance of BatchForecastAccepted from a JSON string
batch_forecast_accepted_instance = BatchForecastAccepted.from_json(json)
# print the JSON string representation of the object
print(BatchForecastAccepted.to_json())

# convert the object into a dict
batch_forecast_accepted_dict = batch_forecast_accepted_instance.to_dict()
# create an instance of BatchForecastAccepted from a dict
batch_forecast_accepted_from_dict = BatchForecastAccepted.from_dict(batch_forecast_accepted_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


