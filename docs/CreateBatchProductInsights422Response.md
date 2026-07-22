# CreateBatchProductInsights422Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**error** | **str** |  | [optional] 
**validation_errors** | **Dict[str, Dict[str, List[str]]]** | Failing entries, keyed by their index in &#x60;series&#x60; | [optional] 
**valid_count** | **int** |  | [optional] 
**total_count** | **int** |  | [optional] 
**time_taken_ms** | **float** |  | [optional] 

## Example

```python
from forecastapi.models.create_batch_product_insights422_response import CreateBatchProductInsights422Response

# TODO update the JSON string below
json = "{}"
# create an instance of CreateBatchProductInsights422Response from a JSON string
create_batch_product_insights422_response_instance = CreateBatchProductInsights422Response.from_json(json)
# print the JSON string representation of the object
print(CreateBatchProductInsights422Response.to_json())

# convert the object into a dict
create_batch_product_insights422_response_dict = create_batch_product_insights422_response_instance.to_dict()
# create an instance of CreateBatchProductInsights422Response from a dict
create_batch_product_insights422_response_from_dict = CreateBatchProductInsights422Response.from_dict(create_batch_product_insights422_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


