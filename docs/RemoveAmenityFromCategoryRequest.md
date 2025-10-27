# RemoveAmenityFromCategoryRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**amenity_id** | **int** |  | 

## Example

```python
from nauticalstream_workspace.models.remove_amenity_from_category_request import RemoveAmenityFromCategoryRequest

# TODO update the JSON string below
json = "{}"
# create an instance of RemoveAmenityFromCategoryRequest from a JSON string
remove_amenity_from_category_request_instance = RemoveAmenityFromCategoryRequest.from_json(json)
# print the JSON string representation of the object
print(RemoveAmenityFromCategoryRequest.to_json())

# convert the object into a dict
remove_amenity_from_category_request_dict = remove_amenity_from_category_request_instance.to_dict()
# create an instance of RemoveAmenityFromCategoryRequest from a dict
remove_amenity_from_category_request_from_dict = RemoveAmenityFromCategoryRequest.from_dict(remove_amenity_from_category_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


