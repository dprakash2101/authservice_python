# LoginClientPost401Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** | Error message | [optional] 

## Example

```python
from authservice.models.login_client_post401_response import LoginClientPost401Response

# TODO update the JSON string below
json = "{}"
# create an instance of LoginClientPost401Response from a JSON string
login_client_post401_response_instance = LoginClientPost401Response.from_json(json)
# print the JSON string representation of the object
print LoginClientPost401Response.to_json()

# convert the object into a dict
login_client_post401_response_dict = login_client_post401_response_instance.to_dict()
# create an instance of LoginClientPost401Response from a dict
login_client_post401_response_form_dict = login_client_post401_response.from_dict(login_client_post401_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


