# CreateForecast400Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**error** | **str** |  | [optional] 
**reason** | **str** |  | [optional] 
**time_taken_ms** | **float** |  | [optional] 

## Example

```python
from forecastapi.models.create_forecast400_response import CreateForecast400Response

# TODO update the JSON string below
json = "{}"
# create an instance of CreateForecast400Response from a JSON string
create_forecast400_response_instance = CreateForecast400Response.from_json(json)
# print the JSON string representation of the object
print(CreateForecast400Response.to_json())

# convert the object into a dict
create_forecast400_response_dict = create_forecast400_response_instance.to_dict()
# create an instance of CreateForecast400Response from a dict
create_forecast400_response_from_dict = CreateForecast400Response.from_dict(create_forecast400_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


