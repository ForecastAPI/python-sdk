# TrafficForecastingResponseResultCostOptimization

Cost analysis and optimization recommendations

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**current_cost** | **float** | Current total cost based on capacity | [optional] 
**optimized_cost** | **float** | Optimized cost after recommendations | [optional] 
**potential_savings** | **float** | Potential cost savings | [optional] 
**savings_percentage** | **float** | Savings as percentage of current cost | [optional] 
**cost_breakdown** | [**TrafficForecastingResponseResultCostOptimizationCostBreakdown**](TrafficForecastingResponseResultCostOptimizationCostBreakdown.md) |  | [optional] 
**recommendations** | [**List[TrafficForecastingResponseResultCostOptimizationRecommendationsInner]**](TrafficForecastingResponseResultCostOptimizationRecommendationsInner.md) | Cost optimization recommendations | [optional] 

## Example

```python
from forecastapi.models.traffic_forecasting_response_result_cost_optimization import TrafficForecastingResponseResultCostOptimization

# TODO update the JSON string below
json = "{}"
# create an instance of TrafficForecastingResponseResultCostOptimization from a JSON string
traffic_forecasting_response_result_cost_optimization_instance = TrafficForecastingResponseResultCostOptimization.from_json(json)
# print the JSON string representation of the object
print(TrafficForecastingResponseResultCostOptimization.to_json())

# convert the object into a dict
traffic_forecasting_response_result_cost_optimization_dict = traffic_forecasting_response_result_cost_optimization_instance.to_dict()
# create an instance of TrafficForecastingResponseResultCostOptimization from a dict
traffic_forecasting_response_result_cost_optimization_from_dict = TrafficForecastingResponseResultCostOptimization.from_dict(traffic_forecasting_response_result_cost_optimization_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


