# AccumulateOptions

Collapse the forecast path into a cumulative total — Σ (value × survival × discount). The same operation covers cumulative demand over a lead time (safety stock), customer lifetime value, TCO and NPV. Returns an `accumulated` block. Honoured by /v2/forecast and /v2/batch/forecast (request-level default or per-series override); rejected on grouped forecasts; ignored by other endpoints sharing this request shape. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**decay** | **float** | Per-period survival factor — 0.95 means 5% attrition each period | [optional] [default to 1.0]
**discount_rate** | **float** | Annual discount rate, converted to the series frequency (a 10% annual rate on monthly periods discounts period 2 by 1.10^(-1/12), not by 1.10) | [optional] [default to 0]
**correlation** | **float** | How correlated the per-period errors are assumed to be; controls only the width of the total&#39;s band. 0 &#x3D; independent periods (measurably too narrow), 1 &#x3D; sum of the bounds (conservative envelope). The default 0.5 was measured across the benchmark suite; a value you supply is your assumption and is never labelled measured.  | [optional] [default to 0.5]

## Example

```python
from forecastapi.models.accumulate_options import AccumulateOptions

# TODO update the JSON string below
json = "{}"
# create an instance of AccumulateOptions from a JSON string
accumulate_options_instance = AccumulateOptions.from_json(json)
# print the JSON string representation of the object
print(AccumulateOptions.to_json())

# convert the object into a dict
accumulate_options_dict = accumulate_options_instance.to_dict()
# create an instance of AccumulateOptions from a dict
accumulate_options_from_dict = AccumulateOptions.from_dict(accumulate_options_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


