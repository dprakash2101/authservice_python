# LoginClientPost200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**token** | **str** | JWT token | [optional] 
**token_type** | **str** | Type of token | [optional] 
**expires_in** | **int** | Expiry time of token in seconds | [optional] 

## Example

```python
from authservice.models.login_client_post200_response import LoginClientPost200Response

# TODO update the JSON string below
json = "{}"
# create an instance of LoginClientPost200Response from a JSON string
login_client_post200_response_instance = LoginClientPost200Response.from_json(json)
# print the JSON string representation of the object
print LoginClientPost200Response.to_json()

# convert the object into a dict
login_client_post200_response_dict = login_client_post200_response_instance.to_dict()
# create an instance of LoginClientPost200Response from a dict
login_client_post200_response_form_dict = login_client_post200_response.from_dict(login_client_post200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


