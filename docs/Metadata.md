# Metadata


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**blame_email_hash** | **str** |  | 
**blame_date** | **datetime** |  | 
**inclusion_date** | **datetime** |  | 

## Example

```python
from sorrydb_api_client.models.metadata import Metadata

# TODO update the JSON string below
json = "{}"
# create an instance of Metadata from a JSON string
metadata_instance = Metadata.from_json(json)
# print the JSON string representation of the object
print(Metadata.to_json())

# convert the object into a dict
metadata_dict = metadata_instance.to_dict()
# create an instance of Metadata from a dict
metadata_from_dict = Metadata.from_dict(metadata_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


