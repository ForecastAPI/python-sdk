# ValidationFailedResponse

The validation-error shape shared by the grouped, batch and product-insights endpoints

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**error** | **str** |  | [optional] 
**errors** | **Dict[str, List[str]]** |  | [optional] 
**time_taken_ms** | **float** |  | [optional] 

## Example

```python
from forecastapi.models.validation_failed_response import ValidationFailedResponse

# TODO update the JSON string below
json = "{}"
# create an instance of ValidationFailedResponse from a JSON string
validation_failed_response_instance = ValidationFailedResponse.from_json(json)
# print the JSON string representation of the object
print(ValidationFailedResponse.to_json())

# convert the object into a dict
validation_failed_response_dict = validation_failed_response_instance.to_dict()
# create an instance of ValidationFailedResponse from a dict
validation_failed_response_from_dict = ValidationFailedResponse.from_dict(validation_failed_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


