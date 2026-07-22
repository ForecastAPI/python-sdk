# TrafficForecastingResponseResultScalingRecommendations

Infrastructure scaling analysis and recommendations

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**peak_traffic** | **float** | Predicted peak traffic across forecast periods | [optional] 
**average_traffic** | **float** | Average predicted traffic | [optional] 
**current_utilization** | **float** | Peak utilization percentage of current capacity | [optional] 
**recommendations** | [**List[TrafficForecastingResponseResultScalingRecommendationsRecommendationsInner]**](TrafficForecastingResponseResultScalingRecommendationsRecommendationsInner.md) | Scaling action recommendations | [optional] 

## Example

```python
from forecastapi.models.traffic_forecasting_response_result_scaling_recommendations import TrafficForecastingResponseResultScalingRecommendations

# TODO update the JSON string below
json = "{}"
# create an instance of TrafficForecastingResponseResultScalingRecommendations from a JSON string
traffic_forecasting_response_result_scaling_recommendations_instance = TrafficForecastingResponseResultScalingRecommendations.from_json(json)
# print the JSON string representation of the object
print(TrafficForecastingResponseResultScalingRecommendations.to_json())

# convert the object into a dict
traffic_forecasting_response_result_scaling_recommendations_dict = traffic_forecasting_response_result_scaling_recommendations_instance.to_dict()
# create an instance of TrafficForecastingResponseResultScalingRecommendations from a dict
traffic_forecasting_response_result_scaling_recommendations_from_dict = TrafficForecastingResponseResultScalingRecommendations.from_dict(traffic_forecasting_response_result_scaling_recommendations_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


