# SQLSorry


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**remote** | **str** |  | 
**branch** | **str** |  | 
**commit** | **str** |  | 
**lean_version** | **str** |  | 
**path** | **str** |  | 
**start_line** | **int** |  | 
**start_column** | **int** |  | 
**end_line** | **int** |  | 
**end_column** | **int** |  | 
**goal** | **str** |  | 
**url** | **str** |  | 
**blame_email_hash** | **str** |  | 
**blame_date** | **datetime** |  | 
**inclusion_date** | **datetime** |  | 

## Example

```python
from sorrydb_api_client.models.sql_sorry import SQLSorry

# TODO update the JSON string below
json = "{}"
# create an instance of SQLSorry from a JSON string
sql_sorry_instance = SQLSorry.from_json(json)
# print the JSON string representation of the object
print(SQLSorry.to_json())

# convert the object into a dict
sql_sorry_dict = sql_sorry_instance.to_dict()
# create an instance of SQLSorry from a dict
sql_sorry_from_dict = SQLSorry.from_dict(sql_sorry_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


