# CreateInventoryPlan400Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**error** | **str** |  | [optional] 
**reason** | **str** |  | [optional] 
**time_taken_ms** | **float** |  | [optional] 

## Example

```python
from forecastapi.models.create_inventory_plan400_response import CreateInventoryPlan400Response

# TODO update the JSON string below
json = "{}"
# create an instance of CreateInventoryPlan400Response from a JSON string
create_inventory_plan400_response_instance = CreateInventoryPlan400Response.from_json(json)
# print the JSON string representation of the object
print(CreateInventoryPlan400Response.to_json())

# convert the object into a dict
create_inventory_plan400_response_dict = create_inventory_plan400_response_instance.to_dict()
# create an instance of CreateInventoryPlan400Response from a dict
create_inventory_plan400_response_from_dict = CreateInventoryPlan400Response.from_dict(create_inventory_plan400_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


