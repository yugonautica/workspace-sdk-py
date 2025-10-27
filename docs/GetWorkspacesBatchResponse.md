# GetWorkspacesBatchResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ids** | [**Dict[str, Workspace]**](Workspace.md) |  | [optional] 
**handles** | [**Dict[str, Workspace]**](Workspace.md) |  | [optional] 

## Example

```python
from nauticalstream_workspace.models.get_workspaces_batch_response import GetWorkspacesBatchResponse

# TODO update the JSON string below
json = "{}"
# create an instance of GetWorkspacesBatchResponse from a JSON string
get_workspaces_batch_response_instance = GetWorkspacesBatchResponse.from_json(json)
# print the JSON string representation of the object
print(GetWorkspacesBatchResponse.to_json())

# convert the object into a dict
get_workspaces_batch_response_dict = get_workspaces_batch_response_instance.to_dict()
# create an instance of GetWorkspacesBatchResponse from a dict
get_workspaces_batch_response_from_dict = GetWorkspacesBatchResponse.from_dict(get_workspaces_batch_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


