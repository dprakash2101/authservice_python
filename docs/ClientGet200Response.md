# ClientGet200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**client_id** | **str** | User&#39;s client ID | [optional] 
**client_secret** | **str** | User&#39;s client secret | [optional] 

## Example

```python
from authservice.models.client_get200_response import ClientGet200Response

# TODO update the JSON string below
json = "{}"
# create an instance of ClientGet200Response from a JSON string
client_get200_response_instance = ClientGet200Response.from_json(json)
# print the JSON string representation of the object
print ClientGet200Response.to_json()

# convert the object into a dict
client_get200_response_dict = client_get200_response_instance.to_dict()
# create an instance of ClientGet200Response from a dict
client_get200_response_form_dict = client_get200_response.from_dict(client_get200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


