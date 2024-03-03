# RegenerateClientCredentialsPost200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** | Success message | [optional] 
**client_id** | **str** | New client ID | [optional] 
**client_secret** | **str** | New client secret | [optional] 

## Example

```python
from authservice.models.regenerate_client_credentials_post200_response import RegenerateClientCredentialsPost200Response

# TODO update the JSON string below
json = "{}"
# create an instance of RegenerateClientCredentialsPost200Response from a JSON string
regenerate_client_credentials_post200_response_instance = RegenerateClientCredentialsPost200Response.from_json(json)
# print the JSON string representation of the object
print RegenerateClientCredentialsPost200Response.to_json()

# convert the object into a dict
regenerate_client_credentials_post200_response_dict = regenerate_client_credentials_post200_response_instance.to_dict()
# create an instance of RegenerateClientCredentialsPost200Response from a dict
regenerate_client_credentials_post200_response_form_dict = regenerate_client_credentials_post200_response.from_dict(regenerate_client_credentials_post200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


