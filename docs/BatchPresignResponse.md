# BatchPresignResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**upload_url** | **str** | Presigned URL — HTTP PUT the JSON file here, including any returned headers | [optional] 
**headers** | **Dict[str, str]** | Headers that must be sent with the upload request | [optional] 
**file_key** | **str** | Pass this as &#x60;file_key&#x60; to POST /v2/batch/forecast after uploading | [optional] 
**expires_in** | **int** | Seconds the upload URL stays valid | [optional] 

## Example

```python
from forecastapi.models.batch_presign_response import BatchPresignResponse

# TODO update the JSON string below
json = "{}"
# create an instance of BatchPresignResponse from a JSON string
batch_presign_response_instance = BatchPresignResponse.from_json(json)
# print the JSON string representation of the object
print(BatchPresignResponse.to_json())

# convert the object into a dict
batch_presign_response_dict = batch_presign_response_instance.to_dict()
# create an instance of BatchPresignResponse from a dict
batch_presign_response_from_dict = BatchPresignResponse.from_dict(batch_presign_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


