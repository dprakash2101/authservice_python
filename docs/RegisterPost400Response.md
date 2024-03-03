# RegisterPost400Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** | Error message | [optional] 

## Example

```python
from authservice.models.register_post400_response import RegisterPost400Response

# TODO update the JSON string below
json = "{}"
# create an instance of RegisterPost400Response from a JSON string
register_post400_response_instance = RegisterPost400Response.from_json(json)
# print the JSON string representation of the object
print RegisterPost400Response.to_json()

# convert the object into a dict
register_post400_response_dict = register_post400_response_instance.to_dict()
# create an instance of RegisterPost400Response from a dict
register_post400_response_form_dict = register_post400_response.from_dict(register_post400_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


