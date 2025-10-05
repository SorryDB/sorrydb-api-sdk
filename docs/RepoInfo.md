# RepoInfo


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**remote** | **str** |  | 
**branch** | **str** |  | 
**commit** | **str** |  | 
**lean_version** | **str** |  | 

## Example

```python
from sorrydb_api_client.models.repo_info import RepoInfo

# TODO update the JSON string below
json = "{}"
# create an instance of RepoInfo from a JSON string
repo_info_instance = RepoInfo.from_json(json)
# print the JSON string representation of the object
print(RepoInfo.to_json())

# convert the object into a dict
repo_info_dict = repo_info_instance.to_dict()
# create an instance of RepoInfo from a dict
repo_info_from_dict = RepoInfo.from_dict(repo_info_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


