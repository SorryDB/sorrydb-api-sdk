# Sorries


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
from sorrydb_api_client.models.sorries import Sorries

# TODO update the JSON string below
json = "{}"
# create an instance of Sorries from a JSON string
sorries_instance = Sorries.from_json(json)
# print the JSON string representation of the object
print(Sorries.to_json())

# convert the object into a dict
sorries_dict = sorries_instance.to_dict()
# create an instance of Sorries from a dict
sorries_from_dict = Sorries.from_dict(sorries_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


