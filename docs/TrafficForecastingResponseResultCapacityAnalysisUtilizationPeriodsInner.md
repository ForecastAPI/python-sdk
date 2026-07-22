# TrafficForecastingResponseResultCapacityAnalysisUtilizationPeriodsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**period** | **int** | Period number | [optional] 
**traffic** | **float** | Predicted traffic | [optional] 
**utilization** | **float** | Utilization percentage | [optional] 
**status** | **str** | Capacity status | [optional] 

## Example

```python
from forecastapi.models.traffic_forecasting_response_result_capacity_analysis_utilization_periods_inner import TrafficForecastingResponseResultCapacityAnalysisUtilizationPeriodsInner

# TODO update the JSON string below
json = "{}"
# create an instance of TrafficForecastingResponseResultCapacityAnalysisUtilizationPeriodsInner from a JSON string
traffic_forecasting_response_result_capacity_analysis_utilization_periods_inner_instance = TrafficForecastingResponseResultCapacityAnalysisUtilizationPeriodsInner.from_json(json)
# print the JSON string representation of the object
print(TrafficForecastingResponseResultCapacityAnalysisUtilizationPeriodsInner.to_json())

# convert the object into a dict
traffic_forecasting_response_result_capacity_analysis_utilization_periods_inner_dict = traffic_forecasting_response_result_capacity_analysis_utilization_periods_inner_instance.to_dict()
# create an instance of TrafficForecastingResponseResultCapacityAnalysisUtilizationPeriodsInner from a dict
traffic_forecasting_response_result_capacity_analysis_utilization_periods_inner_from_dict = TrafficForecastingResponseResultCapacityAnalysisUtilizationPeriodsInner.from_dict(traffic_forecasting_response_result_capacity_analysis_utilization_periods_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


