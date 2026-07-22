# ProductInsightsBatchRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**series** | [**List[ProductInsightsRequest]**](ProductInsightsRequest.md) | One entry per product, each the same shape as a single /v2/product-insights request | 
**batch** | **str** | Existing batch identifier to append this upload to, for submitting one logical batch in chunks | [optional] 
**parts** | **int** | Total number of parts the batch will consist of, when submitting in chunks | [optional] 

## Example

```python
from forecastapi.models.product_insights_batch_request import ProductInsightsBatchRequest

# TODO update the JSON string below
json = "{}"
# create an instance of ProductInsightsBatchRequest from a JSON string
product_insights_batch_request_instance = ProductInsightsBatchRequest.from_json(json)
# print the JSON string representation of the object
print(ProductInsightsBatchRequest.to_json())

# convert the object into a dict
product_insights_batch_request_dict = product_insights_batch_request_instance.to_dict()
# create an instance of ProductInsightsBatchRequest from a dict
product_insights_batch_request_from_dict = ProductInsightsBatchRequest.from_dict(product_insights_batch_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


