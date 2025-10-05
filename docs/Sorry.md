# Sorry


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**repo** | [**RepoInfo**](RepoInfo.md) |  | 
**location** | [**Location**](Location.md) |  | 
**debug_info** | [**DebugInfo**](DebugInfo.md) |  | 
**metadata** | [**Metadata**](Metadata.md) |  | 
**id** | **str** |  | [optional] 

## Example

```python
from sorrydb_api_client.models.sorry import Sorry

# TODO update the JSON string below
json = "{}"
# create an instance of Sorry from a JSON string
sorry_instance = Sorry.from_json(json)
# print the JSON string representation of the object
print(Sorry.to_json())

# convert the object into a dict
sorry_dict = sorry_instance.to_dict()
# create an instance of Sorry from a dict
sorry_from_dict = Sorry.from_dict(sorry_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


