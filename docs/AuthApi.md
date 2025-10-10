# sorrydb_api_client.AuthApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**change_password_auth_change_password_post**](AuthApi.md#change_password_auth_change_password_post) | **POST** /auth/change-password | Change Password
[**get_current_user_info_auth_me_get**](AuthApi.md#get_current_user_info_auth_me_get) | **GET** /auth/me | Get Current User Info
[**login_auth_token_post**](AuthApi.md#login_auth_token_post) | **POST** /auth/token | Login
[**register_auth_register_post**](AuthApi.md#register_auth_register_post) | **POST** /auth/register | Register


# **change_password_auth_change_password_post**
> UserRead change_password_auth_change_password_post(password_change)

Change Password

Change the password for the currently authenticated user.

### Example

* OAuth Authentication (OAuth2PasswordBearer):

```python
import sorrydb_api_client
from sorrydb_api_client.models.password_change import PasswordChange
from sorrydb_api_client.models.user_read import UserRead
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
    api_instance = sorrydb_api_client.AuthApi(api_client)
    password_change = sorrydb_api_client.PasswordChange() # PasswordChange | 

    try:
        # Change Password
        api_response = api_instance.change_password_auth_change_password_post(password_change)
        print("The response of AuthApi->change_password_auth_change_password_post:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AuthApi->change_password_auth_change_password_post: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **password_change** | [**PasswordChange**](PasswordChange.md)|  | 

### Return type

[**UserRead**](UserRead.md)

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

# **get_current_user_info_auth_me_get**
> UserRead get_current_user_info_auth_me_get()

Get Current User Info

### Example

* OAuth Authentication (OAuth2PasswordBearer):

```python
import sorrydb_api_client
from sorrydb_api_client.models.user_read import UserRead
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
    api_instance = sorrydb_api_client.AuthApi(api_client)

    try:
        # Get Current User Info
        api_response = api_instance.get_current_user_info_auth_me_get()
        print("The response of AuthApi->get_current_user_info_auth_me_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AuthApi->get_current_user_info_auth_me_get: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**UserRead**](UserRead.md)

### Authorization

[OAuth2PasswordBearer](../README.md#OAuth2PasswordBearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **login_auth_token_post**
> Token login_auth_token_post(username, password, grant_type=grant_type, scope=scope, client_id=client_id, client_secret=client_secret)

Login

### Example


```python
import sorrydb_api_client
from sorrydb_api_client.models.token import Token
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
    api_instance = sorrydb_api_client.AuthApi(api_client)
    username = 'username_example' # str | 
    password = 'password_example' # str | 
    grant_type = 'grant_type_example' # str |  (optional)
    scope = '' # str |  (optional) (default to '')
    client_id = 'client_id_example' # str |  (optional)
    client_secret = 'client_secret_example' # str |  (optional)

    try:
        # Login
        api_response = api_instance.login_auth_token_post(username, password, grant_type=grant_type, scope=scope, client_id=client_id, client_secret=client_secret)
        print("The response of AuthApi->login_auth_token_post:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AuthApi->login_auth_token_post: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **username** | **str**|  | 
 **password** | **str**|  | 
 **grant_type** | **str**|  | [optional] 
 **scope** | **str**|  | [optional] [default to &#39;&#39;]
 **client_id** | **str**|  | [optional] 
 **client_secret** | **str**|  | [optional] 

### Return type

[**Token**](Token.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **register_auth_register_post**
> UserRead register_auth_register_post(user_create)

Register

### Example


```python
import sorrydb_api_client
from sorrydb_api_client.models.user_create import UserCreate
from sorrydb_api_client.models.user_read import UserRead
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
    api_instance = sorrydb_api_client.AuthApi(api_client)
    user_create = sorrydb_api_client.UserCreate() # UserCreate | 

    try:
        # Register
        api_response = api_instance.register_auth_register_post(user_create)
        print("The response of AuthApi->register_auth_register_post:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AuthApi->register_auth_register_post: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_create** | [**UserCreate**](UserCreate.md)|  | 

### Return type

[**UserRead**](UserRead.md)

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

