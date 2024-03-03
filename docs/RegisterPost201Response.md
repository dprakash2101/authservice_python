# RegisterPost201Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** | Success message | [optional] 
**client_id** | **str** | Generated client ID | [optional] 
**client_secret** | **str** | Generated client secret | [optional] 

## Example

```python
from authservice.models.register_post201_response import RegisterPost201Response

# TODO update the JSON string below
json = "{}"
# create an instance of RegisterPost201Response from a JSON string
register_post201_response_instance = RegisterPost201Response.from_json(json)
# print the JSON string representation of the object
print RegisterPost201Response.to_json()

# convert the object into a dict
register_post201_response_dict = register_post201_response_instance.to_dict()
# create an instance of RegisterPost201Response from a dict
register_post201_response_form_dict = register_post201_response.from_dict(register_post201_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


