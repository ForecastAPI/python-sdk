# TrafficForecastingResponseResultForecastDataInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**period** | **int** | Forecast period number | [optional] 
**var_date** | **datetime** | Date/time for this forecast period | [optional] 
**forecast** | **float** | Forecasted traffic value | [optional] 
**lower** | **float** | Lower confidence bound | [optional] 
**upper** | **float** | Upper confidence bound | [optional] 

## Example

```python
from forecastapi.models.traffic_forecasting_response_result_forecast_data_inner import TrafficForecastingResponseResultForecastDataInner

# TODO update the JSON string below
json = "{}"
# create an instance of TrafficForecastingResponseResultForecastDataInner from a JSON string
traffic_forecasting_response_result_forecast_data_inner_instance = TrafficForecastingResponseResultForecastDataInner.from_json(json)
# print the JSON string representation of the object
print(TrafficForecastingResponseResultForecastDataInner.to_json())

# convert the object into a dict
traffic_forecasting_response_result_forecast_data_inner_dict = traffic_forecasting_response_result_forecast_data_inner_instance.to_dict()
# create an instance of TrafficForecastingResponseResultForecastDataInner from a dict
traffic_forecasting_response_result_forecast_data_inner_from_dict = TrafficForecastingResponseResultForecastDataInner.from_dict(traffic_forecasting_response_result_forecast_data_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


