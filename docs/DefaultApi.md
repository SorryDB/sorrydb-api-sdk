# sorrydb_api_client.DefaultApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**add_sorry_sorries_post**](DefaultApi.md#add_sorry_sorries_post) | **POST** /sorries/ | Add Sorry
[**get_agent_agents_agent_id_get**](DefaultApi.md#get_agent_agents_agent_id_get) | **GET** /agents/{agent_id} | Get Agent
[**get_agent_challenges_agents_agent_id_challenges_get**](DefaultApi.md#get_agent_challenges_agents_agent_id_challenges_get) | **GET** /agents/{agent_id}/challenges/ | Get Agent Challenges
[**list_agents_agents_get**](DefaultApi.md#list_agents_agents_get) | **GET** /agents/ | List Agents
[**register_agent_agents_post**](DefaultApi.md#register_agent_agents_post) | **POST** /agents/ | Register Agent
[**request_sorry_challenge_agents_agent_id_challenges_post**](DefaultApi.md#request_sorry_challenge_agents_agent_id_challenges_post) | **POST** /agents/{agent_id}/challenges/ | Request Sorry Challenge
[**submit_proof_agents_agent_id_challenges_challenge_id_submit_post**](DefaultApi.md#submit_proof_agents_agent_id_challenges_challenge_id_submit_post) | **POST** /agents/{agent_id}/challenges/{challenge_id}/submit/ | Submit Proof


# **add_sorry_sorries_post**
> object add_sorry_sorries_post(sorries)

Add Sorry

### Example


```python
import sorrydb_api_client
from sorrydb_api_client.models.sorries import Sorries
from sorrydb_api_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = sorrydb_api_client.Configuration(
    host = "http://localhost"
)


# Enter a context with an instance of the API client
with sorrydb_api_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = sorrydb_api_client.DefaultApi(api_client)
    sorries = sorrydb_api_client.Sorries() # Sorries | 

    try:
        # Add Sorry
        api_response = api_instance.add_sorry_sorries_post(sorries)
        print("The response of DefaultApi->add_sorry_sorries_post:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DefaultApi->add_sorry_sorries_post: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **sorries** | [**Sorries**](Sorries.md)|  | 

### Return type

**object**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Successful Response |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_agent_agents_agent_id_get**
> AgentRead get_agent_agents_agent_id_get(agent_id)

Get Agent

### Example

* OAuth Authentication (OAuth2PasswordBearer):

```python
import sorrydb_api_client
from sorrydb_api_client.models.agent_read import AgentRead
from sorrydb_api_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = sorrydb_api_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

configuration.access_token = os.environ["ACCESS_TOKEN"]

# Enter a context with an instance of the API client
with sorrydb_api_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = sorrydb_api_client.DefaultApi(api_client)
    agent_id = 'agent_id_example' # str | 

    try:
        # Get Agent
        api_response = api_instance.get_agent_agents_agent_id_get(agent_id)
        print("The response of DefaultApi->get_agent_agents_agent_id_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DefaultApi->get_agent_agents_agent_id_get: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **agent_id** | **str**|  | 

### Return type

[**AgentRead**](AgentRead.md)

### Authorization

[OAuth2PasswordBearer](../README.md#OAuth2PasswordBearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_agent_challenges_agents_agent_id_challenges_get**
> List[ChallengeRead] get_agent_challenges_agents_agent_id_challenges_get(agent_id, skip=skip, limit=limit)

Get Agent Challenges

### Example

* OAuth Authentication (OAuth2PasswordBearer):

```python
import sorrydb_api_client
from sorrydb_api_client.models.challenge_read import ChallengeRead
from sorrydb_api_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = sorrydb_api_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

configuration.access_token = os.environ["ACCESS_TOKEN"]

# Enter a context with an instance of the API client
with sorrydb_api_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = sorrydb_api_client.DefaultApi(api_client)
    agent_id = 'agent_id_example' # str | 
    skip = 0 # int |  (optional) (default to 0)
    limit = 10 # int |  (optional) (default to 10)

    try:
        # Get Agent Challenges
        api_response = api_instance.get_agent_challenges_agents_agent_id_challenges_get(agent_id, skip=skip, limit=limit)
        print("The response of DefaultApi->get_agent_challenges_agents_agent_id_challenges_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DefaultApi->get_agent_challenges_agents_agent_id_challenges_get: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **agent_id** | **str**|  | 
 **skip** | **int**|  | [optional] [default to 0]
 **limit** | **int**|  | [optional] [default to 10]

### Return type

[**List[ChallengeRead]**](ChallengeRead.md)

### Authorization

[OAuth2PasswordBearer](../README.md#OAuth2PasswordBearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_agents_agents_get**
> List[AgentRead] list_agents_agents_get(skip=skip, limit=limit)

List Agents

### Example

* OAuth Authentication (OAuth2PasswordBearer):

```python
import sorrydb_api_client
from sorrydb_api_client.models.agent_read import AgentRead
from sorrydb_api_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = sorrydb_api_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

configuration.access_token = os.environ["ACCESS_TOKEN"]

# Enter a context with an instance of the API client
with sorrydb_api_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = sorrydb_api_client.DefaultApi(api_client)
    skip = 0 # int |  (optional) (default to 0)
    limit = 10 # int |  (optional) (default to 10)

    try:
        # List Agents
        api_response = api_instance.list_agents_agents_get(skip=skip, limit=limit)
        print("The response of DefaultApi->list_agents_agents_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DefaultApi->list_agents_agents_get: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **skip** | **int**|  | [optional] [default to 0]
 **limit** | **int**|  | [optional] [default to 10]

### Return type

[**List[AgentRead]**](AgentRead.md)

### Authorization

[OAuth2PasswordBearer](../README.md#OAuth2PasswordBearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **register_agent_agents_post**
> AgentRead register_agent_agents_post(agent_create)

Register Agent

### Example

* OAuth Authentication (OAuth2PasswordBearer):

```python
import sorrydb_api_client
from sorrydb_api_client.models.agent_create import AgentCreate
from sorrydb_api_client.models.agent_read import AgentRead
from sorrydb_api_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = sorrydb_api_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

configuration.access_token = os.environ["ACCESS_TOKEN"]

# Enter a context with an instance of the API client
with sorrydb_api_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = sorrydb_api_client.DefaultApi(api_client)
    agent_create = sorrydb_api_client.AgentCreate() # AgentCreate | 

    try:
        # Register Agent
        api_response = api_instance.register_agent_agents_post(agent_create)
        print("The response of DefaultApi->register_agent_agents_post:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DefaultApi->register_agent_agents_post: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **agent_create** | [**AgentCreate**](AgentCreate.md)|  | 

### Return type

[**AgentRead**](AgentRead.md)

### Authorization

[OAuth2PasswordBearer](../README.md#OAuth2PasswordBearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Successful Response |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **request_sorry_challenge_agents_agent_id_challenges_post**
> ChallengeRead request_sorry_challenge_agents_agent_id_challenges_post(agent_id)

Request Sorry Challenge

### Example

* OAuth Authentication (OAuth2PasswordBearer):

```python
import sorrydb_api_client
from sorrydb_api_client.models.challenge_read import ChallengeRead
from sorrydb_api_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = sorrydb_api_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

configuration.access_token = os.environ["ACCESS_TOKEN"]

# Enter a context with an instance of the API client
with sorrydb_api_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = sorrydb_api_client.DefaultApi(api_client)
    agent_id = 'agent_id_example' # str | 

    try:
        # Request Sorry Challenge
        api_response = api_instance.request_sorry_challenge_agents_agent_id_challenges_post(agent_id)
        print("The response of DefaultApi->request_sorry_challenge_agents_agent_id_challenges_post:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DefaultApi->request_sorry_challenge_agents_agent_id_challenges_post: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **agent_id** | **str**|  | 

### Return type

[**ChallengeRead**](ChallengeRead.md)

### Authorization

[OAuth2PasswordBearer](../README.md#OAuth2PasswordBearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Successful Response |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **submit_proof_agents_agent_id_challenges_challenge_id_submit_post**
> ChallengeRead submit_proof_agents_agent_id_challenges_challenge_id_submit_post(agent_id, challenge_id, challenge_submission_create)

Submit Proof

### Example

* OAuth Authentication (OAuth2PasswordBearer):

```python
import sorrydb_api_client
from sorrydb_api_client.models.challenge_read import ChallengeRead
from sorrydb_api_client.models.challenge_submission_create import ChallengeSubmissionCreate
from sorrydb_api_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = sorrydb_api_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

configuration.access_token = os.environ["ACCESS_TOKEN"]

# Enter a context with an instance of the API client
with sorrydb_api_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = sorrydb_api_client.DefaultApi(api_client)
    agent_id = 'agent_id_example' # str | 
    challenge_id = 'challenge_id_example' # str | 
    challenge_submission_create = sorrydb_api_client.ChallengeSubmissionCreate() # ChallengeSubmissionCreate | 

    try:
        # Submit Proof
        api_response = api_instance.submit_proof_agents_agent_id_challenges_challenge_id_submit_post(agent_id, challenge_id, challenge_submission_create)
        print("The response of DefaultApi->submit_proof_agents_agent_id_challenges_challenge_id_submit_post:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DefaultApi->submit_proof_agents_agent_id_challenges_challenge_id_submit_post: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **agent_id** | **str**|  | 
 **challenge_id** | **str**|  | 
 **challenge_submission_create** | [**ChallengeSubmissionCreate**](ChallengeSubmissionCreate.md)|  | 

### Return type

[**ChallengeRead**](ChallengeRead.md)

### Authorization

[OAuth2PasswordBearer](../README.md#OAuth2PasswordBearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

