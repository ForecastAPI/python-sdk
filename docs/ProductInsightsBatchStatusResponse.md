# ProductInsightsBatchStatusResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**identifier** | **str** | The batch id | [optional] 
**status** | **str** |  | [optional] 
**batch_parts** | **int** |  | [optional] 
**results** | **Dict[str, object]** | Summary and per-product analysis results as parts complete | [optional] 
**parts** | **List[Dict[str, object]]** | Per-part progress, each carrying its analyses once processed | [optional] 
**started_at** | **datetime** |  | [optional] 
**completed_at** | **datetime** |  | [optional] 
**created_at** | **datetime** |  | [optional] 
**updated_at** | **datetime** |  | [optional] 

## Example

```python
from forecastapi.models.product_insights_batch_status_response import ProductInsightsBatchStatusResponse

# TODO update the JSON string below
json = "{}"
# create an instance of ProductInsightsBatchStatusResponse from a JSON string
product_insights_batch_status_response_instance = ProductInsightsBatchStatusResponse.from_json(json)
# print the JSON string representation of the object
print(ProductInsightsBatchStatusResponse.to_json())

# convert the object into a dict
product_insights_batch_status_response_dict = product_insights_batch_status_response_instance.to_dict()
# create an instance of ProductInsightsBatchStatusResponse from a dict
product_insights_batch_status_response_from_dict = ProductInsightsBatchStatusResponse.from_dict(product_insights_batch_status_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


