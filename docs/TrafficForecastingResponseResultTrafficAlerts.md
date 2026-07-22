# TrafficForecastingResponseResultTrafficAlerts

Traffic spike and anomaly alerts

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**total_alerts** | **int** | Total number of alerts generated | [optional] 
**high_severity** | **int** | Number of high severity alerts | [optional] 
**medium_severity** | **int** | Number of medium severity alerts | [optional] 
**alerts** | [**List[TrafficForecastingResponseResultTrafficAlertsAlertsInner]**](TrafficForecastingResponseResultTrafficAlertsAlertsInner.md) | Individual alert details | [optional] 

## Example

```python
from forecastapi.models.traffic_forecasting_response_result_traffic_alerts import TrafficForecastingResponseResultTrafficAlerts

# TODO update the JSON string below
json = "{}"
# create an instance of TrafficForecastingResponseResultTrafficAlerts from a JSON string
traffic_forecasting_response_result_traffic_alerts_instance = TrafficForecastingResponseResultTrafficAlerts.from_json(json)
# print the JSON string representation of the object
print(TrafficForecastingResponseResultTrafficAlerts.to_json())

# convert the object into a dict
traffic_forecasting_response_result_traffic_alerts_dict = traffic_forecasting_response_result_traffic_alerts_instance.to_dict()
# create an instance of TrafficForecastingResponseResultTrafficAlerts from a dict
traffic_forecasting_response_result_traffic_alerts_from_dict = TrafficForecastingResponseResultTrafficAlerts.from_dict(traffic_forecasting_response_result_traffic_alerts_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


