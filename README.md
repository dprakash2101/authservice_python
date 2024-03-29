# authservice
This API provides token-based authentication for user registration, login, and client credential management. It ensures secure communication by utilizing tokens for authentication. Users can register with unique usernames and passwords, authenticate using client credentials, retrieve client IDs and secrets, and regenerate client credentials as needed. The API supports various user roles, including 'user', 'admin', 'moderator', 'guest', and 'superadmin'.

This package is published in PyPI:
```sh
https://pypi.org/project/authservice/
```
## Requirements.

Python 3.7+

## Installation & Usage
### pip install
If your package is hosted in PyPI:
```sh
pip install authservice
```
If the python package is hosted on a repository, you can install directly using:

```sh
pip install git+https://github.com/CodeCrew24/authservice_python
```
(you may need to run `pip` with root permission: `sudo pip install git+https://github.com/CodeCrew24/authservice_python`)

Then import the package:
```python
import authservice
```

### Setuptools

Install via [Setuptools](http://pypi.python.org/pypi/setuptools).

```sh
python setup.py install --user
```
(or `sudo python setup.py install` to install the package for all users)

Then import the package:
```python
import authservice
```

### Tests

Execute `pytest` to run the tests.

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```python

import authservice
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
    except ApiException as e:
        print("Exception when calling DefaultApi->client_get: %s\n" % e)

```

## Documentation for API Endpoints

All URIs are relative to *https://auth-service-latest.onrender.com/auth*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*DefaultApi* | [**client_get**](docs/DefaultApi.md#client_get) | **GET** /client | Get client ID and secret
*DefaultApi* | [**login_client_post**](docs/DefaultApi.md#login_client_post) | **POST** /login/client | Logs in a user using client ID and secret
*DefaultApi* | [**regenerate_client_credentials_post**](docs/DefaultApi.md#regenerate_client_credentials_post) | **POST** /regenerate-client-credentials | Regenerate client credentials
*DefaultApi* | [**register_post**](docs/DefaultApi.md#register_post) | **POST** /register | Registers a new user


## Documentation For Models

 - [ClientGet200Response](docs/ClientGet200Response.md)
 - [ClientGet401Response](docs/ClientGet401Response.md)
 - [LoginClientPost200Response](docs/LoginClientPost200Response.md)
 - [LoginClientPost401Response](docs/LoginClientPost401Response.md)
 - [RegenerateClientCredentialsPost200Response](docs/RegenerateClientCredentialsPost200Response.md)
 - [RegisterPost201Response](docs/RegisterPost201Response.md)
 - [RegisterPost400Response](docs/RegisterPost400Response.md)
 - [RegisterPost500Response](docs/RegisterPost500Response.md)


<a id="documentation-for-authorization"></a>
## Documentation For Authorization

Endpoints do not require authorization.


## Author




