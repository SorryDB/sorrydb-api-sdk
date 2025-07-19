# ChallengeRead


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**deadline** | **datetime** |  | 
**sorry** | [**SQLSorry**](SQLSorry.md) |  | 
**status** | [**ChallengeStatus**](ChallengeStatus.md) |  | 
**submission** | **str** |  | 

## Example

```python
from sorrydb_api_client.models.challenge_read import ChallengeRead

# TODO update the JSON string below
json = "{}"
# create an instance of ChallengeRead from a JSON string
challenge_read_instance = ChallengeRead.from_json(json)
# print the JSON string representation of the object
print(ChallengeRead.to_json())

# convert the object into a dict
challenge_read_dict = challenge_read_instance.to_dict()
# create an instance of ChallengeRead from a dict
challenge_read_from_dict = ChallengeRead.from_dict(challenge_read_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


