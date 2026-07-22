# TrafficForecastingResponseResultTrafficAlertsAlertsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **str** | Type of alert | [optional] 
**severity** | **str** | Alert severity | [optional] 
**period** | **int** | Period number where alert occurs | [optional] 
**var_date** | **datetime** | Date/time of the alert | [optional] 
**predicted_traffic** | **float** | Predicted traffic value | [optional] 
**baseline_traffic** | **float** | Baseline traffic (for spikes) | [optional] 
**increase_factor** | **float** | Traffic increase factor (for spikes) | [optional] 
**z_score** | **float** | Z-score for anomaly detection | [optional] 
**message** | **str** | Alert message | [optional] 

## Example

```python
from forecastapi.models.traffic_forecasting_response_result_traffic_alerts_alerts_inner import TrafficForecastingResponseResultTrafficAlertsAlertsInner

# TODO update the JSON string below
json = "{}"
# create an instance of TrafficForecastingResponseResultTrafficAlertsAlertsInner from a JSON string
traffic_forecasting_response_result_traffic_alerts_alerts_inner_instance = TrafficForecastingResponseResultTrafficAlertsAlertsInner.from_json(json)
# print the JSON string representation of the object
print(TrafficForecastingResponseResultTrafficAlertsAlertsInner.to_json())

# convert the object into a dict
traffic_forecasting_response_result_traffic_alerts_alerts_inner_dict = traffic_forecasting_response_result_traffic_alerts_alerts_inner_instance.to_dict()
# create an instance of TrafficForecastingResponseResultTrafficAlertsAlertsInner from a dict
traffic_forecasting_response_result_traffic_alerts_alerts_inner_from_dict = TrafficForecastingResponseResultTrafficAlertsAlertsInner.from_dict(traffic_forecasting_response_result_traffic_alerts_alerts_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


