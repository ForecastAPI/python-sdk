# TrafficForecastingResponseResultScalingRecommendationsRecommendationsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**action** | **str** | Recommended scaling action | [optional] 
**current_capacity** | **float** | Current capacity | [optional] 
**recommended_capacity** | **float** | Recommended capacity | [optional] 
**scaling_factor** | **float** | Scaling multiplier | [optional] 
**reason** | **str** | Explanation for the recommendation | [optional] 
**urgency** | **str** | Urgency level of the action | [optional] 
**estimated_time_to_scale** | **int** | Estimated minutes needed for scaling | [optional] 
**potential_savings** | **float** | Potential cost savings (for scale down) | [optional] 

## Example

```python
from forecastapi.models.traffic_forecasting_response_result_scaling_recommendations_recommendations_inner import TrafficForecastingResponseResultScalingRecommendationsRecommendationsInner

# TODO update the JSON string below
json = "{}"
# create an instance of TrafficForecastingResponseResultScalingRecommendationsRecommendationsInner from a JSON string
traffic_forecasting_response_result_scaling_recommendations_recommendations_inner_instance = TrafficForecastingResponseResultScalingRecommendationsRecommendationsInner.from_json(json)
# print the JSON string representation of the object
print(TrafficForecastingResponseResultScalingRecommendationsRecommendationsInner.to_json())

# convert the object into a dict
traffic_forecasting_response_result_scaling_recommendations_recommendations_inner_dict = traffic_forecasting_response_result_scaling_recommendations_recommendations_inner_instance.to_dict()
# create an instance of TrafficForecastingResponseResultScalingRecommendationsRecommendationsInner from a dict
traffic_forecasting_response_result_scaling_recommendations_recommendations_inner_from_dict = TrafficForecastingResponseResultScalingRecommendationsRecommendationsInner.from_dict(traffic_forecasting_response_result_scaling_recommendations_recommendations_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


