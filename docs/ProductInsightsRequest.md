# ProductInsightsRequest

At least one of `sales`, `purchases` or `cost_history` must be provided.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**identifier** | **str** | Product identifier | 
**tenant_context** | **str** |  | [optional] 
**product_name** | **str** |  | [optional] 
**product_group_id** | **str** |  | [optional] 
**base_currency** | **str** | ISO 4217 currency the analysis reports in | [optional] 
**baseline_period_days** | [**ProductInsightsRequestBaselinePeriodDays**](ProductInsightsRequestBaselinePeriodDays.md) |  | [optional] 
**locale** | **str** | Locale for insight texts | [optional] [default to 'en']
**sales** | [**List[ProductInsightsRequestSalesInner]**](ProductInsightsRequestSalesInner.md) |  | [optional] 
**purchases** | [**List[ProductInsightsRequestPurchasesInner]**](ProductInsightsRequestPurchasesInner.md) |  | [optional] 
**cost_history** | [**List[ProductInsightsRequestCostHistoryInner]**](ProductInsightsRequestCostHistoryInner.md) |  | [optional] 
**insight_settings** | [**ProductInsightsRequestInsightSettings**](ProductInsightsRequestInsightSettings.md) |  | [optional] 

## Example

```python
from forecastapi.models.product_insights_request import ProductInsightsRequest

# TODO update the JSON string below
json = "{}"
# create an instance of ProductInsightsRequest from a JSON string
product_insights_request_instance = ProductInsightsRequest.from_json(json)
# print the JSON string representation of the object
print(ProductInsightsRequest.to_json())

# convert the object into a dict
product_insights_request_dict = product_insights_request_instance.to_dict()
# create an instance of ProductInsightsRequest from a dict
product_insights_request_from_dict = ProductInsightsRequest.from_dict(product_insights_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


