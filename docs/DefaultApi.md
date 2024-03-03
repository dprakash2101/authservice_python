# authservice.DefaultApi

All URIs are relative to *https://auth-service-latest.onrender.com/auth*

Method | HTTP request | Description
------------- | ------------- | -------------
[**client_get**](DefaultApi.md#client_get) | **GET** /client | Get client ID and secret
[**login_client_post**](DefaultApi.md#login_client_post) | **POST** /login/client | Logs in a user using client ID and secret
[**regenerate_client_credentials_post**](DefaultApi.md#regenerate_client_credentials_post) | **POST** /regenerate-client-credentials | Regenerate client credentials
[**register_post**](DefaultApi.md#register_post) | **POST** /register | Registers a new user


# **client_get**
> ClientGet200Response client_get(username, password)

Get client ID and secret

Returns the client ID and client secret of the user associated with the provided username and password.

### Example


```python
import authservice
from authservice.models.client_get200_response import ClientGet200Response
from authservice.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://auth-service-latest.onrender.com/auth
# See configuration.py for a list of all supported configuration parameters.
configuration = authservice.Configuration(
    host = "https://auth-service-latest.onrender.com/auth"
)


# Enter a context with an instance of the API client
with authservice.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = authservice.DefaultApi(api_client)
    username = 'johndoe' # str | User's username
    password = 'password123' # str | User's password

    try:
        # Get client ID and secret
        api_response = api_instance.client_get(username, password)
        print("The response of DefaultApi->client_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DefaultApi->client_get: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **username** | **str**| User&#39;s username | 
 **password** | **str**| User&#39;s password | 

### Return type

[**ClientGet200Response**](ClientGet200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Client ID and client secret retrieved successfully |  -  |
**401** | Unauthorized (invalid credentials) |  -  |
**500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **login_client_post**
> LoginClientPost200Response login_client_post(client_id, client_secret)

Logs in a user using client ID and secret

Authenticates a user with the provided client ID and secret. Returns a JWT token, token type (Bearer), and expiry time in seconds.

### Example


```python
import authservice
from authservice.models.login_client_post200_response import LoginClientPost200Response
from authservice.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://auth-service-latest.onrender.com/auth
# See configuration.py for a list of all supported configuration parameters.
configuration = authservice.Configuration(
    host = "https://auth-service-latest.onrender.com/auth"
)


# Enter a context with an instance of the API client
with authservice.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = authservice.DefaultApi(api_client)
    client_id = 'abc123-xyz456' # str | User's client ID
    client_secret = 'def789-ghi012' # str | User's client secret

    try:
        # Logs in a user using client ID and secret
        api_response = api_instance.login_client_post(client_id, client_secret)
        print("The response of DefaultApi->login_client_post:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DefaultApi->login_client_post: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **client_id** | **str**| User&#39;s client ID | 
 **client_secret** | **str**| User&#39;s client secret | 

### Return type

[**LoginClientPost200Response**](LoginClientPost200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Login successful |  -  |
**401** | Unauthorized (invalid client credentials) |  -  |
**500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **regenerate_client_credentials_post**
> RegenerateClientCredentialsPost200Response regenerate_client_credentials_post(username, password)

Regenerate client credentials

Regenerates the client ID and client secret of the user associated with the provided username and password. Returns the new client ID and client secret in the response.

### Example


```python
import authservice
from authservice.models.regenerate_client_credentials_post200_response import RegenerateClientCredentialsPost200Response
from authservice.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://auth-service-latest.onrender.com/auth
# See configuration.py for a list of all supported configuration parameters.
configuration = authservice.Configuration(
    host = "https://auth-service-latest.onrender.com/auth"
)


# Enter a context with an instance of the API client
with authservice.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = authservice.DefaultApi(api_client)
    username = 'johndoe' # str | User's username
    password = 'password123' # str | User's password

    try:
        # Regenerate client credentials
        api_response = api_instance.regenerate_client_credentials_post(username, password)
        print("The response of DefaultApi->regenerate_client_credentials_post:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DefaultApi->regenerate_client_credentials_post: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **username** | **str**| User&#39;s username | 
 **password** | **str**| User&#39;s password | 

### Return type

[**RegenerateClientCredentialsPost200Response**](RegenerateClientCredentialsPost200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Client credentials regenerated successfully |  -  |
**401** | Unauthorized (invalid credentials) |  -  |
**500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **register_post**
> RegisterPost201Response register_post(username, password, role)

Registers a new user

Creates a new user with the provided username, password, and role. Returns the generated client ID and client secret in the response.

### Example


```python
import authservice
from authservice.models.register_post201_response import RegisterPost201Response
from authservice.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://auth-service-latest.onrender.com/auth
# See configuration.py for a list of all supported configuration parameters.
configuration = authservice.Configuration(
    host = "https://auth-service-latest.onrender.com/auth"
)


# Enter a context with an instance of the API client
with authservice.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = authservice.DefaultApi(api_client)
    username = 'johndoe' # str | Unique username for the user
    password = 'password123' # str | User's password
    role = 'user' # str |  (default to 'user')

    try:
        # Registers a new user
        api_response = api_instance.register_post(username, password, role)
        print("The response of DefaultApi->register_post:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DefaultApi->register_post: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **username** | **str**| Unique username for the user | 
 **password** | **str**| User&#39;s password | 
 **role** | **str**|  | [default to &#39;user&#39;]

### Return type

[**RegisterPost201Response**](RegisterPost201Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | User registered successfully |  -  |
**400** | Bad request (e.g., username already taken) |  -  |
**500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

