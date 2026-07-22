# TrafficForecastingRequestTrafficSettings

Infrastructure and traffic configuration

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**current_capacity** | **float** | Current infrastructure capacity (requests, users, etc.) | 
**baseline_traffic** | **float** | Normal/expected traffic level for comparison | 
**scaling_buffer** | **float** | Buffer percentage for scaling decisions (default 0.2 &#x3D; 20%) | [optional] 
**scale_up_threshold** | **float** | Utilization threshold to trigger scale up (default 0.8 &#x3D; 80%) | [optional] 
**scale_down_threshold** | **float** | Utilization threshold to trigger scale down (default 0.3 &#x3D; 30%) | [optional] 
**alert_threshold** | **float** | Traffic spike alert threshold as multiplier of baseline (default 1.5 &#x3D; 150%) | [optional] 
**anomaly_threshold** | **float** | Standard deviations for anomaly detection (default 3.0) | [optional] 
**cost_per_unit** | **float** | Variable cost per traffic unit (default 0.01) | [optional] 
**fixed_cost_per_capacity** | **float** | Fixed cost per capacity unit (default 0.1) | [optional] 
**base_scaling_time** | **int** | Base time in minutes for scaling operations (default 5) | [optional] 
**enable_auto_scaling** | **bool** | Whether auto-scaling is currently enabled (default false) | [optional] 

## Example

```python
from forecastapi.models.traffic_forecasting_request_traffic_settings import TrafficForecastingRequestTrafficSettings

# TODO update the JSON string below
json = "{}"
# create an instance of TrafficForecastingRequestTrafficSettings from a JSON string
traffic_forecasting_request_traffic_settings_instance = TrafficForecastingRequestTrafficSettings.from_json(json)
# print the JSON string representation of the object
print(TrafficForecastingRequestTrafficSettings.to_json())

# convert the object into a dict
traffic_forecasting_request_traffic_settings_dict = traffic_forecasting_request_traffic_settings_instance.to_dict()
# create an instance of TrafficForecastingRequestTrafficSettings from a dict
traffic_forecasting_request_traffic_settings_from_dict = TrafficForecastingRequestTrafficSettings.from_dict(traffic_forecasting_request_traffic_settings_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


