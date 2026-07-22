# CreateForecast502Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**error** | **str** |  | [optional] 
**time_taken_ms** | **float** |  | [optional] 

## Example

```python
from forecastapi.models.create_forecast502_response import CreateForecast502Response

# TODO update the JSON string below
json = "{}"
# create an instance of CreateForecast502Response from a JSON string
create_forecast502_response_instance = CreateForecast502Response.from_json(json)
# print the JSON string representation of the object
print(CreateForecast502Response.to_json())

# convert the object into a dict
create_forecast502_response_dict = create_forecast502_response_instance.to_dict()
# create an instance of CreateForecast502Response from a dict
create_forecast502_response_from_dict = CreateForecast502Response.from_dict(create_forecast502_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


