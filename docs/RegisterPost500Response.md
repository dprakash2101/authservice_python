# RegisterPost500Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**error** | **str** | Error message | [optional] 

## Example

```python
from authservice.models.register_post500_response import RegisterPost500Response

# TODO update the JSON string below
json = "{}"
# create an instance of RegisterPost500Response from a JSON string
register_post500_response_instance = RegisterPost500Response.from_json(json)
# print the JSON string representation of the object
print RegisterPost500Response.to_json()

# convert the object into a dict
register_post500_response_dict = register_post500_response_instance.to_dict()
# create an instance of RegisterPost500Response from a dict
register_post500_response_form_dict = register_post500_response.from_dict(register_post500_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


