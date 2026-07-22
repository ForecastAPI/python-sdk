# TrafficForecastingResponseResult


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**metric** | **str** | Metric identifier from the request | [optional] 
**current_capacity** | **float** | Current infrastructure capacity | [optional] 
**baseline_traffic** | **float** | Baseline traffic level | [optional] 
**scaling_recommendations** | [**TrafficForecastingResponseResultScalingRecommendations**](TrafficForecastingResponseResultScalingRecommendations.md) |  | [optional] 
**capacity_analysis** | [**TrafficForecastingResponseResultCapacityAnalysis**](TrafficForecastingResponseResultCapacityAnalysis.md) |  | [optional] 
**traffic_alerts** | [**TrafficForecastingResponseResultTrafficAlerts**](TrafficForecastingResponseResultTrafficAlerts.md) |  | [optional] 
**cost_optimization** | [**TrafficForecastingResponseResultCostOptimization**](TrafficForecastingResponseResultCostOptimization.md) |  | [optional] 
**forecast_data** | [**List[TrafficForecastingResponseResultForecastDataInner]**](TrafficForecastingResponseResultForecastDataInner.md) | Underlying forecast data used for analysis | [optional] 

## Example

```python
from forecastapi.models.traffic_forecasting_response_result import TrafficForecastingResponseResult

# TODO update the JSON string below
json = "{}"
# create an instance of TrafficForecastingResponseResult from a JSON string
traffic_forecasting_response_result_instance = TrafficForecastingResponseResult.from_json(json)
# print the JSON string representation of the object
print(TrafficForecastingResponseResult.to_json())

# convert the object into a dict
traffic_forecasting_response_result_dict = traffic_forecasting_response_result_instance.to_dict()
# create an instance of TrafficForecastingResponseResult from a dict
traffic_forecasting_response_result_from_dict = TrafficForecastingResponseResult.from_dict(traffic_forecasting_response_result_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


