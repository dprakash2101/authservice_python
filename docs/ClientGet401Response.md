# ClientGet401Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** | Error message | [optional] 

## Example

```python
from authservice.models.client_get401_response import ClientGet401Response

# TODO update the JSON string below
json = "{}"
# create an instance of ClientGet401Response from a JSON string
client_get401_response_instance = ClientGet401Response.from_json(json)
# print the JSON string representation of the object
print ClientGet401Response.to_json()

# convert the object into a dict
client_get401_response_dict = client_get401_response_instance.to_dict()
# create an instance of ClientGet401Response from a dict
client_get401_response_form_dict = client_get401_response.from_dict(client_get401_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


