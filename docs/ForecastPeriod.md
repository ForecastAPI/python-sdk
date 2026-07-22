# ForecastPeriod


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**period** | **int** | 1-based forecast period number | [optional] 
**var_date** | **date** | Date of this forecast period | [optional] 
**forecast** | **float** | Point forecast for this period | [optional] 
**lower** | **float** | Lower prediction bound at the requested confidence level | [optional] 
**upper** | **float** | Upper prediction bound at the requested confidence level | [optional] 
**quantiles** | **Dict[str, float]** | Present only when &#x60;quantiles&#x60; was requested — the forecast at each requested decile level for this period | [optional] 

## Example

```python
from forecastapi.models.forecast_period import ForecastPeriod

# TODO update the JSON string below
json = "{}"
# create an instance of ForecastPeriod from a JSON string
forecast_period_instance = ForecastPeriod.from_json(json)
# print the JSON string representation of the object
print(ForecastPeriod.to_json())

# convert the object into a dict
forecast_period_dict = forecast_period_instance.to_dict()
# create an instance of ForecastPeriod from a dict
forecast_period_from_dict = ForecastPeriod.from_dict(forecast_period_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


