# TrafficForecastingResponseResultCostOptimizationRecommendationsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **str** | Type of cost optimization | [optional] 
**description** | **str** | Recommendation description | [optional] 
**current_capacity** | **float** | Current capacity (for capacity optimization) | [optional] 
**recommended_capacity** | **float** | Recommended capacity (for capacity optimization) | [optional] 
**potential_savings** | **float** | Potential cost savings | [optional] 

## Example

```python
from forecastapi.models.traffic_forecasting_response_result_cost_optimization_recommendations_inner import TrafficForecastingResponseResultCostOptimizationRecommendationsInner

# TODO update the JSON string below
json = "{}"
# create an instance of TrafficForecastingResponseResultCostOptimizationRecommendationsInner from a JSON string
traffic_forecasting_response_result_cost_optimization_recommendations_inner_instance = TrafficForecastingResponseResultCostOptimizationRecommendationsInner.from_json(json)
# print the JSON string representation of the object
print(TrafficForecastingResponseResultCostOptimizationRecommendationsInner.to_json())

# convert the object into a dict
traffic_forecasting_response_result_cost_optimization_recommendations_inner_dict = traffic_forecasting_response_result_cost_optimization_recommendations_inner_instance.to_dict()
# create an instance of TrafficForecastingResponseResultCostOptimizationRecommendationsInner from a dict
traffic_forecasting_response_result_cost_optimization_recommendations_inner_from_dict = TrafficForecastingResponseResultCostOptimizationRecommendationsInner.from_dict(traffic_forecasting_response_result_cost_optimization_recommendations_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


