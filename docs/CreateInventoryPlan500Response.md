# CreateInventoryPlan500Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**error** | **str** |  | [optional] 
**time_taken_ms** | **float** |  | [optional] 

## Example

```python
from forecastapi.models.create_inventory_plan500_response import CreateInventoryPlan500Response

# TODO update the JSON string below
json = "{}"
# create an instance of CreateInventoryPlan500Response from a JSON string
create_inventory_plan500_response_instance = CreateInventoryPlan500Response.from_json(json)
# print the JSON string representation of the object
print(CreateInventoryPlan500Response.to_json())

# convert the object into a dict
create_inventory_plan500_response_dict = create_inventory_plan500_response_instance.to_dict()
# create an instance of CreateInventoryPlan500Response from a dict
create_inventory_plan500_response_from_dict = CreateInventoryPlan500Response.from_dict(create_inventory_plan500_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


