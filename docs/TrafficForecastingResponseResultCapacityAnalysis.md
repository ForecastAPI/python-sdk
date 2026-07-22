# TrafficForecastingResponseResultCapacityAnalysis

Detailed capacity utilization analysis

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**current_capacity** | **float** | Current infrastructure capacity | [optional] 
**utilization_periods** | [**List[TrafficForecastingResponseResultCapacityAnalysisUtilizationPeriodsInner]**](TrafficForecastingResponseResultCapacityAnalysisUtilizationPeriodsInner.md) | Capacity utilization for each forecast period | [optional] 
**over_capacity_periods** | **int** | Number of periods exceeding capacity | [optional] 
**critical_periods** | **int** | Number of periods above 90% utilization | [optional] 
**forecast_duration_minutes** | **int** | Total forecast duration in minutes | [optional] 
**next_capacity_breach** | **date** | Date when capacity will be breached | [optional] 
**capacity_efficiency** | **float** | Efficiency score (0-100, optimal around 75% utilization) | [optional] 

## Example

```python
from forecastapi.models.traffic_forecasting_response_result_capacity_analysis import TrafficForecastingResponseResultCapacityAnalysis

# TODO update the JSON string below
json = "{}"
# create an instance of TrafficForecastingResponseResultCapacityAnalysis from a JSON string
traffic_forecasting_response_result_capacity_analysis_instance = TrafficForecastingResponseResultCapacityAnalysis.from_json(json)
# print the JSON string representation of the object
print(TrafficForecastingResponseResultCapacityAnalysis.to_json())

# convert the object into a dict
traffic_forecasting_response_result_capacity_analysis_dict = traffic_forecasting_response_result_capacity_analysis_instance.to_dict()
# create an instance of TrafficForecastingResponseResultCapacityAnalysis from a dict
traffic_forecasting_response_result_capacity_analysis_from_dict = TrafficForecastingResponseResultCapacityAnalysis.from_dict(traffic_forecasting_response_result_capacity_analysis_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


