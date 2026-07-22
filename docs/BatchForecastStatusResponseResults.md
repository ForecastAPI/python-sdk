# BatchForecastStatusResponseResults


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**summary** | [**BatchForecastStatusResponseResultsSummary**](BatchForecastStatusResponseResultsSummary.md) |  | [optional] 
**data** | [**Dict[str, BatchSeriesResult]**](BatchSeriesResult.md) | Each series&#39; results, keyed by ENTITY id rather than by your identifier — one batch may legitimately contain the same identifier under several tenant_context values, so the identifier alone would not be unique. Match series via the identifier and tenant_context echoed inside each result.  | [optional] 

## Example

```python
from forecastapi.models.batch_forecast_status_response_results import BatchForecastStatusResponseResults

# TODO update the JSON string below
json = "{}"
# create an instance of BatchForecastStatusResponseResults from a JSON string
batch_forecast_status_response_results_instance = BatchForecastStatusResponseResults.from_json(json)
# print the JSON string representation of the object
print(BatchForecastStatusResponseResults.to_json())

# convert the object into a dict
batch_forecast_status_response_results_dict = batch_forecast_status_response_results_instance.to_dict()
# create an instance of BatchForecastStatusResponseResults from a dict
batch_forecast_status_response_results_from_dict = BatchForecastStatusResponseResults.from_dict(batch_forecast_status_response_results_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


