# CreateBatchProductInsights500Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**error** | **str** |  | [optional] 
**time_taken_ms** | **float** |  | [optional] 

## Example

```python
from forecastapi.models.create_batch_product_insights500_response import CreateBatchProductInsights500Response

# TODO update the JSON string below
json = "{}"
# create an instance of CreateBatchProductInsights500Response from a JSON string
create_batch_product_insights500_response_instance = CreateBatchProductInsights500Response.from_json(json)
# print the JSON string representation of the object
print(CreateBatchProductInsights500Response.to_json())

# convert the object into a dict
create_batch_product_insights500_response_dict = create_batch_product_insights500_response_instance.to_dict()
# create an instance of CreateBatchProductInsights500Response from a dict
create_batch_product_insights500_response_from_dict = CreateBatchProductInsights500Response.from_dict(create_batch_product_insights500_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


