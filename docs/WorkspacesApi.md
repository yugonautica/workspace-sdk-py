# nauticalstream_workspace.WorkspacesApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**activate_amenity**](WorkspacesApi.md#activate_amenity) | **POST** /workspaces/amenities/{amenity_id}/activate | Activate Amenity
[**activate_category**](WorkspacesApi.md#activate_category) | **POST** /workspaces/categories/{category_id}/activate | Activate Category
[**activate_workspace**](WorkspacesApi.md#activate_workspace) | **POST** /workspaces/{workspace_id}/activate | Activate Workspace
[**activate_workspace_feature**](WorkspacesApi.md#activate_workspace_feature) | **POST** /workspaces/{workspace_id}/features/{feature_id}/activate | Activate Workspace Feature
[**add_amenity_to_category**](WorkspacesApi.md#add_amenity_to_category) | **POST** /workspaces/categories/{category_id}/amenities | Add Amenity To Category
[**are_features_active**](WorkspacesApi.md#are_features_active) | **POST** /workspaces/features/batch/is-active | Are Features Active
[**check_workspace_handle_exists**](WorkspacesApi.md#check_workspace_handle_exists) | **GET** /workspaces/handle/{handle}/exists | Check Workspace Handle Exists
[**create_amenity**](WorkspacesApi.md#create_amenity) | **POST** /workspaces/amenities | Create Amenity
[**create_category**](WorkspacesApi.md#create_category) | **POST** /workspaces/categories | Create Category
[**create_workspace**](WorkspacesApi.md#create_workspace) | **POST** /workspaces/ | Create Workspace
[**create_workspace_feature**](WorkspacesApi.md#create_workspace_feature) | **POST** /workspaces/{workspace_id}/features | Create Workspace Feature
[**deactivate_amenity**](WorkspacesApi.md#deactivate_amenity) | **POST** /workspaces/amenities/{amenity_id}/deactivate | Deactivate Amenity
[**deactivate_category**](WorkspacesApi.md#deactivate_category) | **POST** /workspaces/categories/{category_id}/deactivate | Deactivate Category
[**deactivate_workspace**](WorkspacesApi.md#deactivate_workspace) | **POST** /workspaces/{workspace_id}/deactivate | Deactivate Workspace
[**deactivate_workspace_feature**](WorkspacesApi.md#deactivate_workspace_feature) | **POST** /workspaces/{workspace_id}/features/{feature_id}/deactivate | Deactivate Workspace Feature
[**delete_workspace**](WorkspacesApi.md#delete_workspace) | **DELETE** /workspaces/{workspace_id} | Delete Workspace
[**delete_workspace_feature**](WorkspacesApi.md#delete_workspace_feature) | **DELETE** /workspaces/{workspace_id}/features/{feature_id} | Delete Workspace Feature
[**deprecate_amenity**](WorkspacesApi.md#deprecate_amenity) | **POST** /workspaces/amenities/{amenity_id}/deprecate | Deprecate Amenity
[**deprecate_category**](WorkspacesApi.md#deprecate_category) | **POST** /workspaces/categories/{category_id}/deprecate | Deprecate Category
[**get_amenities_batch**](WorkspacesApi.md#get_amenities_batch) | **POST** /workspaces/amenities/batch | Get Amenities Batch
[**get_amenity**](WorkspacesApi.md#get_amenity) | **GET** /workspaces/amenities/{amenity_id} | Get Amenity
[**get_categories_batch**](WorkspacesApi.md#get_categories_batch) | **POST** /workspaces/categories/batch | Get Categories Batch
[**get_category**](WorkspacesApi.md#get_category) | **GET** /workspaces/categories/{category_id} | Get Category
[**get_features_batch**](WorkspacesApi.md#get_features_batch) | **POST** /workspaces/features/batch | Get Features Batch
[**get_workspace**](WorkspacesApi.md#get_workspace) | **GET** /workspaces/ | Get Workspace
[**get_workspace_feature**](WorkspacesApi.md#get_workspace_feature) | **GET** /workspaces/{workspace_id}/features/{feature_id} | Get Workspace Feature
[**get_workspace_features**](WorkspacesApi.md#get_workspace_features) | **GET** /workspaces/{workspace_id}/features | Get Workspace Features
[**get_workspaces_batch**](WorkspacesApi.md#get_workspaces_batch) | **POST** /workspaces/batch | Get Workspaces Batch
[**get_workspaces_by_bbox**](WorkspacesApi.md#get_workspaces_by_bbox) | **POST** /workspaces/bbox | Get Workspaces By Bbox
[**list_amenities**](WorkspacesApi.md#list_amenities) | **POST** /workspaces/amenities/list | List Amenities
[**list_categories**](WorkspacesApi.md#list_categories) | **POST** /workspaces/categories/list | List Categories
[**list_workspaces**](WorkspacesApi.md#list_workspaces) | **POST** /workspaces/list | List Workspaces
[**remove_amenity_from_category**](WorkspacesApi.md#remove_amenity_from_category) | **DELETE** /workspaces/categories/{category_id}/amenities | Remove Amenity From Category
[**update_workspace**](WorkspacesApi.md#update_workspace) | **PUT** /workspaces/{workspace_id} | Update Workspace
[**update_workspace_feature**](WorkspacesApi.md#update_workspace_feature) | **PUT** /workspaces/{workspace_id}/features/{feature_id} | Update Workspace Feature


# **activate_amenity**
> activate_amenity(amenity_id, x_user_id=x_user_id, x_workspace_id=x_workspace_id)

Activate Amenity

### Example


```python
import nauticalstream_workspace
from nauticalstream_workspace.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = nauticalstream_workspace.Configuration(
    host = "http://localhost"
)


# Enter a context with an instance of the API client
with nauticalstream_workspace.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = nauticalstream_workspace.WorkspacesApi(api_client)
    amenity_id = 56 # int | 
    x_user_id = 'x_user_id_example' # str |  (optional)
    x_workspace_id = 'x_workspace_id_example' # str |  (optional)

    try:
        # Activate Amenity
        api_instance.activate_amenity(amenity_id, x_user_id=x_user_id, x_workspace_id=x_workspace_id)
    except Exception as e:
        print("Exception when calling WorkspacesApi->activate_amenity: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **amenity_id** | **int**|  | 
 **x_user_id** | **str**|  | [optional] 
 **x_workspace_id** | **str**|  | [optional] 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**204** | Successful Response |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **activate_category**
> activate_category(category_id, x_user_id=x_user_id, x_workspace_id=x_workspace_id)

Activate Category

### Example


```python
import nauticalstream_workspace
from nauticalstream_workspace.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = nauticalstream_workspace.Configuration(
    host = "http://localhost"
)


# Enter a context with an instance of the API client
with nauticalstream_workspace.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = nauticalstream_workspace.WorkspacesApi(api_client)
    category_id = 56 # int | 
    x_user_id = 'x_user_id_example' # str |  (optional)
    x_workspace_id = 'x_workspace_id_example' # str |  (optional)

    try:
        # Activate Category
        api_instance.activate_category(category_id, x_user_id=x_user_id, x_workspace_id=x_workspace_id)
    except Exception as e:
        print("Exception when calling WorkspacesApi->activate_category: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **category_id** | **int**|  | 
 **x_user_id** | **str**|  | [optional] 
 **x_workspace_id** | **str**|  | [optional] 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**204** | Successful Response |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **activate_workspace**
> activate_workspace(workspace_id, x_user_id=x_user_id, x_workspace_id=x_workspace_id)

Activate Workspace

### Example


```python
import nauticalstream_workspace
from nauticalstream_workspace.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = nauticalstream_workspace.Configuration(
    host = "http://localhost"
)


# Enter a context with an instance of the API client
with nauticalstream_workspace.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = nauticalstream_workspace.WorkspacesApi(api_client)
    workspace_id = 56 # int | 
    x_user_id = 'x_user_id_example' # str |  (optional)
    x_workspace_id = 'x_workspace_id_example' # str |  (optional)

    try:
        # Activate Workspace
        api_instance.activate_workspace(workspace_id, x_user_id=x_user_id, x_workspace_id=x_workspace_id)
    except Exception as e:
        print("Exception when calling WorkspacesApi->activate_workspace: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_id** | **int**|  | 
 **x_user_id** | **str**|  | [optional] 
 **x_workspace_id** | **str**|  | [optional] 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**204** | Successful Response |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **activate_workspace_feature**
> activate_workspace_feature(workspace_id, feature_id, x_user_id=x_user_id, x_workspace_id=x_workspace_id)

Activate Workspace Feature

Activate a feature within a workspace

### Example


```python
import nauticalstream_workspace
from nauticalstream_workspace.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = nauticalstream_workspace.Configuration(
    host = "http://localhost"
)


# Enter a context with an instance of the API client
with nauticalstream_workspace.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = nauticalstream_workspace.WorkspacesApi(api_client)
    workspace_id = 56 # int | 
    feature_id = 'feature_id_example' # str | 
    x_user_id = 'x_user_id_example' # str |  (optional)
    x_workspace_id = 'x_workspace_id_example' # str |  (optional)

    try:
        # Activate Workspace Feature
        api_instance.activate_workspace_feature(workspace_id, feature_id, x_user_id=x_user_id, x_workspace_id=x_workspace_id)
    except Exception as e:
        print("Exception when calling WorkspacesApi->activate_workspace_feature: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_id** | **int**|  | 
 **feature_id** | **str**|  | 
 **x_user_id** | **str**|  | [optional] 
 **x_workspace_id** | **str**|  | [optional] 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**204** | Successful Response |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **add_amenity_to_category**
> add_amenity_to_category(category_id, add_amenity_to_category_request, x_user_id=x_user_id, x_workspace_id=x_workspace_id)

Add Amenity To Category

### Example


```python
import nauticalstream_workspace
from nauticalstream_workspace.models.add_amenity_to_category_request import AddAmenityToCategoryRequest
from nauticalstream_workspace.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = nauticalstream_workspace.Configuration(
    host = "http://localhost"
)


# Enter a context with an instance of the API client
with nauticalstream_workspace.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = nauticalstream_workspace.WorkspacesApi(api_client)
    category_id = 56 # int | 
    add_amenity_to_category_request = nauticalstream_workspace.AddAmenityToCategoryRequest() # AddAmenityToCategoryRequest | 
    x_user_id = 'x_user_id_example' # str |  (optional)
    x_workspace_id = 'x_workspace_id_example' # str |  (optional)

    try:
        # Add Amenity To Category
        api_instance.add_amenity_to_category(category_id, add_amenity_to_category_request, x_user_id=x_user_id, x_workspace_id=x_workspace_id)
    except Exception as e:
        print("Exception when calling WorkspacesApi->add_amenity_to_category: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **category_id** | **int**|  | 
 **add_amenity_to_category_request** | [**AddAmenityToCategoryRequest**](AddAmenityToCategoryRequest.md)|  | 
 **x_user_id** | **str**|  | [optional] 
 **x_workspace_id** | **str**|  | [optional] 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**204** | Successful Response |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **are_features_active**
> BatchWorkspaceAmenityCheckResponse are_features_active(batch_workspace_amenity_check_request, x_user_id=x_user_id, x_workspace_id=x_workspace_id)

Are Features Active

### Example


```python
import nauticalstream_workspace
from nauticalstream_workspace.models.batch_workspace_amenity_check_request import BatchWorkspaceAmenityCheckRequest
from nauticalstream_workspace.models.batch_workspace_amenity_check_response import BatchWorkspaceAmenityCheckResponse
from nauticalstream_workspace.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = nauticalstream_workspace.Configuration(
    host = "http://localhost"
)


# Enter a context with an instance of the API client
with nauticalstream_workspace.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = nauticalstream_workspace.WorkspacesApi(api_client)
    batch_workspace_amenity_check_request = nauticalstream_workspace.BatchWorkspaceAmenityCheckRequest() # BatchWorkspaceAmenityCheckRequest | 
    x_user_id = 'x_user_id_example' # str |  (optional)
    x_workspace_id = 'x_workspace_id_example' # str |  (optional)

    try:
        # Are Features Active
        api_response = api_instance.are_features_active(batch_workspace_amenity_check_request, x_user_id=x_user_id, x_workspace_id=x_workspace_id)
        print("The response of WorkspacesApi->are_features_active:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WorkspacesApi->are_features_active: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **batch_workspace_amenity_check_request** | [**BatchWorkspaceAmenityCheckRequest**](BatchWorkspaceAmenityCheckRequest.md)|  | 
 **x_user_id** | **str**|  | [optional] 
 **x_workspace_id** | **str**|  | [optional] 

### Return type

[**BatchWorkspaceAmenityCheckResponse**](BatchWorkspaceAmenityCheckResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **check_workspace_handle_exists**
> bool check_workspace_handle_exists(handle, x_user_id=x_user_id, x_workspace_id=x_workspace_id)

Check Workspace Handle Exists

### Example


```python
import nauticalstream_workspace
from nauticalstream_workspace.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = nauticalstream_workspace.Configuration(
    host = "http://localhost"
)


# Enter a context with an instance of the API client
with nauticalstream_workspace.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = nauticalstream_workspace.WorkspacesApi(api_client)
    handle = 'handle_example' # str | 
    x_user_id = 'x_user_id_example' # str |  (optional)
    x_workspace_id = 'x_workspace_id_example' # str |  (optional)

    try:
        # Check Workspace Handle Exists
        api_response = api_instance.check_workspace_handle_exists(handle, x_user_id=x_user_id, x_workspace_id=x_workspace_id)
        print("The response of WorkspacesApi->check_workspace_handle_exists:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WorkspacesApi->check_workspace_handle_exists: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **handle** | **str**|  | 
 **x_user_id** | **str**|  | [optional] 
 **x_workspace_id** | **str**|  | [optional] 

### Return type

**bool**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_amenity**
> Amenity create_amenity(create_amenity_request, x_user_id=x_user_id, x_workspace_id=x_workspace_id)

Create Amenity

### Example


```python
import nauticalstream_workspace
from nauticalstream_workspace.models.amenity import Amenity
from nauticalstream_workspace.models.create_amenity_request import CreateAmenityRequest
from nauticalstream_workspace.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = nauticalstream_workspace.Configuration(
    host = "http://localhost"
)


# Enter a context with an instance of the API client
with nauticalstream_workspace.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = nauticalstream_workspace.WorkspacesApi(api_client)
    create_amenity_request = nauticalstream_workspace.CreateAmenityRequest() # CreateAmenityRequest | 
    x_user_id = 'x_user_id_example' # str |  (optional)
    x_workspace_id = 'x_workspace_id_example' # str |  (optional)

    try:
        # Create Amenity
        api_response = api_instance.create_amenity(create_amenity_request, x_user_id=x_user_id, x_workspace_id=x_workspace_id)
        print("The response of WorkspacesApi->create_amenity:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WorkspacesApi->create_amenity: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **create_amenity_request** | [**CreateAmenityRequest**](CreateAmenityRequest.md)|  | 
 **x_user_id** | **str**|  | [optional] 
 **x_workspace_id** | **str**|  | [optional] 

### Return type

[**Amenity**](Amenity.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_category**
> Category create_category(create_category_request, x_user_id=x_user_id, x_workspace_id=x_workspace_id)

Create Category

### Example


```python
import nauticalstream_workspace
from nauticalstream_workspace.models.category import Category
from nauticalstream_workspace.models.create_category_request import CreateCategoryRequest
from nauticalstream_workspace.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = nauticalstream_workspace.Configuration(
    host = "http://localhost"
)


# Enter a context with an instance of the API client
with nauticalstream_workspace.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = nauticalstream_workspace.WorkspacesApi(api_client)
    create_category_request = nauticalstream_workspace.CreateCategoryRequest() # CreateCategoryRequest | 
    x_user_id = 'x_user_id_example' # str |  (optional)
    x_workspace_id = 'x_workspace_id_example' # str |  (optional)

    try:
        # Create Category
        api_response = api_instance.create_category(create_category_request, x_user_id=x_user_id, x_workspace_id=x_workspace_id)
        print("The response of WorkspacesApi->create_category:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WorkspacesApi->create_category: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **create_category_request** | [**CreateCategoryRequest**](CreateCategoryRequest.md)|  | 
 **x_user_id** | **str**|  | [optional] 
 **x_workspace_id** | **str**|  | [optional] 

### Return type

[**Category**](Category.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_workspace**
> Workspace create_workspace(create_workspace_request, x_user_id=x_user_id, x_workspace_id=x_workspace_id)

Create Workspace

### Example


```python
import nauticalstream_workspace
from nauticalstream_workspace.models.create_workspace_request import CreateWorkspaceRequest
from nauticalstream_workspace.models.workspace import Workspace
from nauticalstream_workspace.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = nauticalstream_workspace.Configuration(
    host = "http://localhost"
)


# Enter a context with an instance of the API client
with nauticalstream_workspace.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = nauticalstream_workspace.WorkspacesApi(api_client)
    create_workspace_request = nauticalstream_workspace.CreateWorkspaceRequest() # CreateWorkspaceRequest | 
    x_user_id = 'x_user_id_example' # str |  (optional)
    x_workspace_id = 'x_workspace_id_example' # str |  (optional)

    try:
        # Create Workspace
        api_response = api_instance.create_workspace(create_workspace_request, x_user_id=x_user_id, x_workspace_id=x_workspace_id)
        print("The response of WorkspacesApi->create_workspace:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WorkspacesApi->create_workspace: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **create_workspace_request** | [**CreateWorkspaceRequest**](CreateWorkspaceRequest.md)|  | 
 **x_user_id** | **str**|  | [optional] 
 **x_workspace_id** | **str**|  | [optional] 

### Return type

[**Workspace**](Workspace.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_workspace_feature**
> Feature create_workspace_feature(workspace_id, create_feature_request, x_user_id=x_user_id, x_workspace_id=x_workspace_id)

Create Workspace Feature

Create a new feature for a workspace

### Example


```python
import nauticalstream_workspace
from nauticalstream_workspace.models.create_feature_request import CreateFeatureRequest
from nauticalstream_workspace.models.feature import Feature
from nauticalstream_workspace.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = nauticalstream_workspace.Configuration(
    host = "http://localhost"
)


# Enter a context with an instance of the API client
with nauticalstream_workspace.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = nauticalstream_workspace.WorkspacesApi(api_client)
    workspace_id = 56 # int | 
    create_feature_request = nauticalstream_workspace.CreateFeatureRequest() # CreateFeatureRequest | 
    x_user_id = 'x_user_id_example' # str |  (optional)
    x_workspace_id = 'x_workspace_id_example' # str |  (optional)

    try:
        # Create Workspace Feature
        api_response = api_instance.create_workspace_feature(workspace_id, create_feature_request, x_user_id=x_user_id, x_workspace_id=x_workspace_id)
        print("The response of WorkspacesApi->create_workspace_feature:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WorkspacesApi->create_workspace_feature: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_id** | **int**|  | 
 **create_feature_request** | [**CreateFeatureRequest**](CreateFeatureRequest.md)|  | 
 **x_user_id** | **str**|  | [optional] 
 **x_workspace_id** | **str**|  | [optional] 

### Return type

[**Feature**](Feature.md)

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

# **deactivate_amenity**
> deactivate_amenity(amenity_id, x_user_id=x_user_id, x_workspace_id=x_workspace_id)

Deactivate Amenity

### Example


```python
import nauticalstream_workspace
from nauticalstream_workspace.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = nauticalstream_workspace.Configuration(
    host = "http://localhost"
)


# Enter a context with an instance of the API client
with nauticalstream_workspace.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = nauticalstream_workspace.WorkspacesApi(api_client)
    amenity_id = 56 # int | 
    x_user_id = 'x_user_id_example' # str |  (optional)
    x_workspace_id = 'x_workspace_id_example' # str |  (optional)

    try:
        # Deactivate Amenity
        api_instance.deactivate_amenity(amenity_id, x_user_id=x_user_id, x_workspace_id=x_workspace_id)
    except Exception as e:
        print("Exception when calling WorkspacesApi->deactivate_amenity: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **amenity_id** | **int**|  | 
 **x_user_id** | **str**|  | [optional] 
 **x_workspace_id** | **str**|  | [optional] 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**204** | Successful Response |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deactivate_category**
> deactivate_category(category_id, x_user_id=x_user_id, x_workspace_id=x_workspace_id)

Deactivate Category

### Example


```python
import nauticalstream_workspace
from nauticalstream_workspace.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = nauticalstream_workspace.Configuration(
    host = "http://localhost"
)


# Enter a context with an instance of the API client
with nauticalstream_workspace.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = nauticalstream_workspace.WorkspacesApi(api_client)
    category_id = 56 # int | 
    x_user_id = 'x_user_id_example' # str |  (optional)
    x_workspace_id = 'x_workspace_id_example' # str |  (optional)

    try:
        # Deactivate Category
        api_instance.deactivate_category(category_id, x_user_id=x_user_id, x_workspace_id=x_workspace_id)
    except Exception as e:
        print("Exception when calling WorkspacesApi->deactivate_category: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **category_id** | **int**|  | 
 **x_user_id** | **str**|  | [optional] 
 **x_workspace_id** | **str**|  | [optional] 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**204** | Successful Response |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deactivate_workspace**
> deactivate_workspace(workspace_id, x_user_id=x_user_id, x_workspace_id=x_workspace_id)

Deactivate Workspace

### Example


```python
import nauticalstream_workspace
from nauticalstream_workspace.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = nauticalstream_workspace.Configuration(
    host = "http://localhost"
)


# Enter a context with an instance of the API client
with nauticalstream_workspace.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = nauticalstream_workspace.WorkspacesApi(api_client)
    workspace_id = 56 # int | 
    x_user_id = 'x_user_id_example' # str |  (optional)
    x_workspace_id = 'x_workspace_id_example' # str |  (optional)

    try:
        # Deactivate Workspace
        api_instance.deactivate_workspace(workspace_id, x_user_id=x_user_id, x_workspace_id=x_workspace_id)
    except Exception as e:
        print("Exception when calling WorkspacesApi->deactivate_workspace: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_id** | **int**|  | 
 **x_user_id** | **str**|  | [optional] 
 **x_workspace_id** | **str**|  | [optional] 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**204** | Successful Response |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deactivate_workspace_feature**
> deactivate_workspace_feature(workspace_id, feature_id, x_user_id=x_user_id, x_workspace_id=x_workspace_id)

Deactivate Workspace Feature

Deactivate a feature within a workspace

### Example


```python
import nauticalstream_workspace
from nauticalstream_workspace.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = nauticalstream_workspace.Configuration(
    host = "http://localhost"
)


# Enter a context with an instance of the API client
with nauticalstream_workspace.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = nauticalstream_workspace.WorkspacesApi(api_client)
    workspace_id = 56 # int | 
    feature_id = 'feature_id_example' # str | 
    x_user_id = 'x_user_id_example' # str |  (optional)
    x_workspace_id = 'x_workspace_id_example' # str |  (optional)

    try:
        # Deactivate Workspace Feature
        api_instance.deactivate_workspace_feature(workspace_id, feature_id, x_user_id=x_user_id, x_workspace_id=x_workspace_id)
    except Exception as e:
        print("Exception when calling WorkspacesApi->deactivate_workspace_feature: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_id** | **int**|  | 
 **feature_id** | **str**|  | 
 **x_user_id** | **str**|  | [optional] 
 **x_workspace_id** | **str**|  | [optional] 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**204** | Successful Response |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_workspace**
> object delete_workspace(workspace_id, x_user_id=x_user_id, x_workspace_id=x_workspace_id)

Delete Workspace

### Example


```python
import nauticalstream_workspace
from nauticalstream_workspace.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = nauticalstream_workspace.Configuration(
    host = "http://localhost"
)


# Enter a context with an instance of the API client
with nauticalstream_workspace.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = nauticalstream_workspace.WorkspacesApi(api_client)
    workspace_id = 56 # int | 
    x_user_id = 'x_user_id_example' # str |  (optional)
    x_workspace_id = 'x_workspace_id_example' # str |  (optional)

    try:
        # Delete Workspace
        api_response = api_instance.delete_workspace(workspace_id, x_user_id=x_user_id, x_workspace_id=x_workspace_id)
        print("The response of WorkspacesApi->delete_workspace:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WorkspacesApi->delete_workspace: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_id** | **int**|  | 
 **x_user_id** | **str**|  | [optional] 
 **x_workspace_id** | **str**|  | [optional] 

### Return type

**object**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_workspace_feature**
> delete_workspace_feature(workspace_id, feature_id, x_user_id=x_user_id, x_workspace_id=x_workspace_id)

Delete Workspace Feature

Delete a feature from a workspace

### Example


```python
import nauticalstream_workspace
from nauticalstream_workspace.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = nauticalstream_workspace.Configuration(
    host = "http://localhost"
)


# Enter a context with an instance of the API client
with nauticalstream_workspace.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = nauticalstream_workspace.WorkspacesApi(api_client)
    workspace_id = 56 # int | 
    feature_id = 'feature_id_example' # str | 
    x_user_id = 'x_user_id_example' # str |  (optional)
    x_workspace_id = 'x_workspace_id_example' # str |  (optional)

    try:
        # Delete Workspace Feature
        api_instance.delete_workspace_feature(workspace_id, feature_id, x_user_id=x_user_id, x_workspace_id=x_workspace_id)
    except Exception as e:
        print("Exception when calling WorkspacesApi->delete_workspace_feature: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_id** | **int**|  | 
 **feature_id** | **str**|  | 
 **x_user_id** | **str**|  | [optional] 
 **x_workspace_id** | **str**|  | [optional] 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**204** | Successful Response |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deprecate_amenity**
> deprecate_amenity(amenity_id, x_user_id=x_user_id, x_workspace_id=x_workspace_id)

Deprecate Amenity

### Example


```python
import nauticalstream_workspace
from nauticalstream_workspace.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = nauticalstream_workspace.Configuration(
    host = "http://localhost"
)


# Enter a context with an instance of the API client
with nauticalstream_workspace.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = nauticalstream_workspace.WorkspacesApi(api_client)
    amenity_id = 56 # int | 
    x_user_id = 'x_user_id_example' # str |  (optional)
    x_workspace_id = 'x_workspace_id_example' # str |  (optional)

    try:
        # Deprecate Amenity
        api_instance.deprecate_amenity(amenity_id, x_user_id=x_user_id, x_workspace_id=x_workspace_id)
    except Exception as e:
        print("Exception when calling WorkspacesApi->deprecate_amenity: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **amenity_id** | **int**|  | 
 **x_user_id** | **str**|  | [optional] 
 **x_workspace_id** | **str**|  | [optional] 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**204** | Successful Response |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deprecate_category**
> deprecate_category(category_id, x_user_id=x_user_id, x_workspace_id=x_workspace_id)

Deprecate Category

### Example


```python
import nauticalstream_workspace
from nauticalstream_workspace.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = nauticalstream_workspace.Configuration(
    host = "http://localhost"
)


# Enter a context with an instance of the API client
with nauticalstream_workspace.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = nauticalstream_workspace.WorkspacesApi(api_client)
    category_id = 56 # int | 
    x_user_id = 'x_user_id_example' # str |  (optional)
    x_workspace_id = 'x_workspace_id_example' # str |  (optional)

    try:
        # Deprecate Category
        api_instance.deprecate_category(category_id, x_user_id=x_user_id, x_workspace_id=x_workspace_id)
    except Exception as e:
        print("Exception when calling WorkspacesApi->deprecate_category: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **category_id** | **int**|  | 
 **x_user_id** | **str**|  | [optional] 
 **x_workspace_id** | **str**|  | [optional] 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**204** | Successful Response |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_amenities_batch**
> GetAmenitiesBatchResponse get_amenities_batch(get_amenities_batch_request, x_user_id=x_user_id, x_workspace_id=x_workspace_id)

Get Amenities Batch

### Example


```python
import nauticalstream_workspace
from nauticalstream_workspace.models.get_amenities_batch_request import GetAmenitiesBatchRequest
from nauticalstream_workspace.models.get_amenities_batch_response import GetAmenitiesBatchResponse
from nauticalstream_workspace.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = nauticalstream_workspace.Configuration(
    host = "http://localhost"
)


# Enter a context with an instance of the API client
with nauticalstream_workspace.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = nauticalstream_workspace.WorkspacesApi(api_client)
    get_amenities_batch_request = nauticalstream_workspace.GetAmenitiesBatchRequest() # GetAmenitiesBatchRequest | 
    x_user_id = 'x_user_id_example' # str |  (optional)
    x_workspace_id = 'x_workspace_id_example' # str |  (optional)

    try:
        # Get Amenities Batch
        api_response = api_instance.get_amenities_batch(get_amenities_batch_request, x_user_id=x_user_id, x_workspace_id=x_workspace_id)
        print("The response of WorkspacesApi->get_amenities_batch:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WorkspacesApi->get_amenities_batch: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **get_amenities_batch_request** | [**GetAmenitiesBatchRequest**](GetAmenitiesBatchRequest.md)|  | 
 **x_user_id** | **str**|  | [optional] 
 **x_workspace_id** | **str**|  | [optional] 

### Return type

[**GetAmenitiesBatchResponse**](GetAmenitiesBatchResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_amenity**
> Amenity get_amenity(amenity_id, x_user_id=x_user_id, x_workspace_id=x_workspace_id)

Get Amenity

### Example


```python
import nauticalstream_workspace
from nauticalstream_workspace.models.amenity import Amenity
from nauticalstream_workspace.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = nauticalstream_workspace.Configuration(
    host = "http://localhost"
)


# Enter a context with an instance of the API client
with nauticalstream_workspace.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = nauticalstream_workspace.WorkspacesApi(api_client)
    amenity_id = 56 # int | 
    x_user_id = 'x_user_id_example' # str |  (optional)
    x_workspace_id = 'x_workspace_id_example' # str |  (optional)

    try:
        # Get Amenity
        api_response = api_instance.get_amenity(amenity_id, x_user_id=x_user_id, x_workspace_id=x_workspace_id)
        print("The response of WorkspacesApi->get_amenity:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WorkspacesApi->get_amenity: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **amenity_id** | **int**|  | 
 **x_user_id** | **str**|  | [optional] 
 **x_workspace_id** | **str**|  | [optional] 

### Return type

[**Amenity**](Amenity.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_categories_batch**
> GetCategoriesBatchResponse get_categories_batch(get_categories_batch_request, x_user_id=x_user_id, x_workspace_id=x_workspace_id)

Get Categories Batch

### Example


```python
import nauticalstream_workspace
from nauticalstream_workspace.models.get_categories_batch_request import GetCategoriesBatchRequest
from nauticalstream_workspace.models.get_categories_batch_response import GetCategoriesBatchResponse
from nauticalstream_workspace.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = nauticalstream_workspace.Configuration(
    host = "http://localhost"
)


# Enter a context with an instance of the API client
with nauticalstream_workspace.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = nauticalstream_workspace.WorkspacesApi(api_client)
    get_categories_batch_request = nauticalstream_workspace.GetCategoriesBatchRequest() # GetCategoriesBatchRequest | 
    x_user_id = 'x_user_id_example' # str |  (optional)
    x_workspace_id = 'x_workspace_id_example' # str |  (optional)

    try:
        # Get Categories Batch
        api_response = api_instance.get_categories_batch(get_categories_batch_request, x_user_id=x_user_id, x_workspace_id=x_workspace_id)
        print("The response of WorkspacesApi->get_categories_batch:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WorkspacesApi->get_categories_batch: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **get_categories_batch_request** | [**GetCategoriesBatchRequest**](GetCategoriesBatchRequest.md)|  | 
 **x_user_id** | **str**|  | [optional] 
 **x_workspace_id** | **str**|  | [optional] 

### Return type

[**GetCategoriesBatchResponse**](GetCategoriesBatchResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_category**
> Category get_category(category_id, x_user_id=x_user_id, x_workspace_id=x_workspace_id)

Get Category

### Example


```python
import nauticalstream_workspace
from nauticalstream_workspace.models.category import Category
from nauticalstream_workspace.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = nauticalstream_workspace.Configuration(
    host = "http://localhost"
)


# Enter a context with an instance of the API client
with nauticalstream_workspace.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = nauticalstream_workspace.WorkspacesApi(api_client)
    category_id = 56 # int | 
    x_user_id = 'x_user_id_example' # str |  (optional)
    x_workspace_id = 'x_workspace_id_example' # str |  (optional)

    try:
        # Get Category
        api_response = api_instance.get_category(category_id, x_user_id=x_user_id, x_workspace_id=x_workspace_id)
        print("The response of WorkspacesApi->get_category:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WorkspacesApi->get_category: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **category_id** | **int**|  | 
 **x_user_id** | **str**|  | [optional] 
 **x_workspace_id** | **str**|  | [optional] 

### Return type

[**Category**](Category.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_features_batch**
> GetFeaturesBatchResponse get_features_batch(get_features_batch_request, x_user_id=x_user_id, x_workspace_id=x_workspace_id)

Get Features Batch

### Example


```python
import nauticalstream_workspace
from nauticalstream_workspace.models.get_features_batch_request import GetFeaturesBatchRequest
from nauticalstream_workspace.models.get_features_batch_response import GetFeaturesBatchResponse
from nauticalstream_workspace.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = nauticalstream_workspace.Configuration(
    host = "http://localhost"
)


# Enter a context with an instance of the API client
with nauticalstream_workspace.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = nauticalstream_workspace.WorkspacesApi(api_client)
    get_features_batch_request = nauticalstream_workspace.GetFeaturesBatchRequest() # GetFeaturesBatchRequest | 
    x_user_id = 'x_user_id_example' # str |  (optional)
    x_workspace_id = 'x_workspace_id_example' # str |  (optional)

    try:
        # Get Features Batch
        api_response = api_instance.get_features_batch(get_features_batch_request, x_user_id=x_user_id, x_workspace_id=x_workspace_id)
        print("The response of WorkspacesApi->get_features_batch:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WorkspacesApi->get_features_batch: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **get_features_batch_request** | [**GetFeaturesBatchRequest**](GetFeaturesBatchRequest.md)|  | 
 **x_user_id** | **str**|  | [optional] 
 **x_workspace_id** | **str**|  | [optional] 

### Return type

[**GetFeaturesBatchResponse**](GetFeaturesBatchResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_workspace**
> Workspace get_workspace(id=id, handle=handle, x_user_id=x_user_id, x_workspace_id=x_workspace_id)

Get Workspace

Get workspace by ID or handle

### Example


```python
import nauticalstream_workspace
from nauticalstream_workspace.models.workspace import Workspace
from nauticalstream_workspace.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = nauticalstream_workspace.Configuration(
    host = "http://localhost"
)


# Enter a context with an instance of the API client
with nauticalstream_workspace.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = nauticalstream_workspace.WorkspacesApi(api_client)
    id = 56 # int |  (optional)
    handle = 'handle_example' # str |  (optional)
    x_user_id = 'x_user_id_example' # str |  (optional)
    x_workspace_id = 'x_workspace_id_example' # str |  (optional)

    try:
        # Get Workspace
        api_response = api_instance.get_workspace(id=id, handle=handle, x_user_id=x_user_id, x_workspace_id=x_workspace_id)
        print("The response of WorkspacesApi->get_workspace:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WorkspacesApi->get_workspace: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**|  | [optional] 
 **handle** | **str**|  | [optional] 
 **x_user_id** | **str**|  | [optional] 
 **x_workspace_id** | **str**|  | [optional] 

### Return type

[**Workspace**](Workspace.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_workspace_feature**
> Feature get_workspace_feature(workspace_id, feature_id, x_user_id=x_user_id, x_workspace_id=x_workspace_id)

Get Workspace Feature

### Example


```python
import nauticalstream_workspace
from nauticalstream_workspace.models.feature import Feature
from nauticalstream_workspace.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = nauticalstream_workspace.Configuration(
    host = "http://localhost"
)


# Enter a context with an instance of the API client
with nauticalstream_workspace.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = nauticalstream_workspace.WorkspacesApi(api_client)
    workspace_id = 56 # int | 
    feature_id = 'feature_id_example' # str | 
    x_user_id = 'x_user_id_example' # str |  (optional)
    x_workspace_id = 'x_workspace_id_example' # str |  (optional)

    try:
        # Get Workspace Feature
        api_response = api_instance.get_workspace_feature(workspace_id, feature_id, x_user_id=x_user_id, x_workspace_id=x_workspace_id)
        print("The response of WorkspacesApi->get_workspace_feature:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WorkspacesApi->get_workspace_feature: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_id** | **int**|  | 
 **feature_id** | **str**|  | 
 **x_user_id** | **str**|  | [optional] 
 **x_workspace_id** | **str**|  | [optional] 

### Return type

[**Feature**](Feature.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_workspace_features**
> List[Feature] get_workspace_features(workspace_id, x_user_id=x_user_id, x_workspace_id=x_workspace_id)

Get Workspace Features

### Example


```python
import nauticalstream_workspace
from nauticalstream_workspace.models.feature import Feature
from nauticalstream_workspace.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = nauticalstream_workspace.Configuration(
    host = "http://localhost"
)


# Enter a context with an instance of the API client
with nauticalstream_workspace.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = nauticalstream_workspace.WorkspacesApi(api_client)
    workspace_id = 56 # int | 
    x_user_id = 'x_user_id_example' # str |  (optional)
    x_workspace_id = 'x_workspace_id_example' # str |  (optional)

    try:
        # Get Workspace Features
        api_response = api_instance.get_workspace_features(workspace_id, x_user_id=x_user_id, x_workspace_id=x_workspace_id)
        print("The response of WorkspacesApi->get_workspace_features:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WorkspacesApi->get_workspace_features: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_id** | **int**|  | 
 **x_user_id** | **str**|  | [optional] 
 **x_workspace_id** | **str**|  | [optional] 

### Return type

[**List[Feature]**](Feature.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_workspaces_batch**
> GetWorkspacesBatchResponse get_workspaces_batch(get_workspaces_batch_request, x_user_id=x_user_id, x_workspace_id=x_workspace_id)

Get Workspaces Batch

### Example


```python
import nauticalstream_workspace
from nauticalstream_workspace.models.get_workspaces_batch_request import GetWorkspacesBatchRequest
from nauticalstream_workspace.models.get_workspaces_batch_response import GetWorkspacesBatchResponse
from nauticalstream_workspace.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = nauticalstream_workspace.Configuration(
    host = "http://localhost"
)


# Enter a context with an instance of the API client
with nauticalstream_workspace.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = nauticalstream_workspace.WorkspacesApi(api_client)
    get_workspaces_batch_request = nauticalstream_workspace.GetWorkspacesBatchRequest() # GetWorkspacesBatchRequest | 
    x_user_id = 'x_user_id_example' # str |  (optional)
    x_workspace_id = 'x_workspace_id_example' # str |  (optional)

    try:
        # Get Workspaces Batch
        api_response = api_instance.get_workspaces_batch(get_workspaces_batch_request, x_user_id=x_user_id, x_workspace_id=x_workspace_id)
        print("The response of WorkspacesApi->get_workspaces_batch:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WorkspacesApi->get_workspaces_batch: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **get_workspaces_batch_request** | [**GetWorkspacesBatchRequest**](GetWorkspacesBatchRequest.md)|  | 
 **x_user_id** | **str**|  | [optional] 
 **x_workspace_id** | **str**|  | [optional] 

### Return type

[**GetWorkspacesBatchResponse**](GetWorkspacesBatchResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_workspaces_by_bbox**
> List[Workspace] get_workspaces_by_bbox(workspace_b_box_query_request, x_user_id=x_user_id, x_workspace_id=x_workspace_id)

Get Workspaces By Bbox

### Example


```python
import nauticalstream_workspace
from nauticalstream_workspace.models.workspace import Workspace
from nauticalstream_workspace.models.workspace_b_box_query_request import WorkspaceBBoxQueryRequest
from nauticalstream_workspace.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = nauticalstream_workspace.Configuration(
    host = "http://localhost"
)


# Enter a context with an instance of the API client
with nauticalstream_workspace.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = nauticalstream_workspace.WorkspacesApi(api_client)
    workspace_b_box_query_request = nauticalstream_workspace.WorkspaceBBoxQueryRequest() # WorkspaceBBoxQueryRequest | 
    x_user_id = 'x_user_id_example' # str |  (optional)
    x_workspace_id = 'x_workspace_id_example' # str |  (optional)

    try:
        # Get Workspaces By Bbox
        api_response = api_instance.get_workspaces_by_bbox(workspace_b_box_query_request, x_user_id=x_user_id, x_workspace_id=x_workspace_id)
        print("The response of WorkspacesApi->get_workspaces_by_bbox:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WorkspacesApi->get_workspaces_by_bbox: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_b_box_query_request** | [**WorkspaceBBoxQueryRequest**](WorkspaceBBoxQueryRequest.md)|  | 
 **x_user_id** | **str**|  | [optional] 
 **x_workspace_id** | **str**|  | [optional] 

### Return type

[**List[Workspace]**](Workspace.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_amenities**
> ListAmenitiesResponse list_amenities(x_user_id=x_user_id, x_workspace_id=x_workspace_id, list_amenities_request=list_amenities_request)

List Amenities

### Example


```python
import nauticalstream_workspace
from nauticalstream_workspace.models.list_amenities_request import ListAmenitiesRequest
from nauticalstream_workspace.models.list_amenities_response import ListAmenitiesResponse
from nauticalstream_workspace.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = nauticalstream_workspace.Configuration(
    host = "http://localhost"
)


# Enter a context with an instance of the API client
with nauticalstream_workspace.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = nauticalstream_workspace.WorkspacesApi(api_client)
    x_user_id = 'x_user_id_example' # str |  (optional)
    x_workspace_id = 'x_workspace_id_example' # str |  (optional)
    list_amenities_request = nauticalstream_workspace.ListAmenitiesRequest() # ListAmenitiesRequest |  (optional)

    try:
        # List Amenities
        api_response = api_instance.list_amenities(x_user_id=x_user_id, x_workspace_id=x_workspace_id, list_amenities_request=list_amenities_request)
        print("The response of WorkspacesApi->list_amenities:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WorkspacesApi->list_amenities: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_user_id** | **str**|  | [optional] 
 **x_workspace_id** | **str**|  | [optional] 
 **list_amenities_request** | [**ListAmenitiesRequest**](ListAmenitiesRequest.md)|  | [optional] 

### Return type

[**ListAmenitiesResponse**](ListAmenitiesResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_categories**
> ListCategoriesResponse list_categories(x_user_id=x_user_id, x_workspace_id=x_workspace_id, list_categories_request=list_categories_request)

List Categories

### Example


```python
import nauticalstream_workspace
from nauticalstream_workspace.models.list_categories_request import ListCategoriesRequest
from nauticalstream_workspace.models.list_categories_response import ListCategoriesResponse
from nauticalstream_workspace.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = nauticalstream_workspace.Configuration(
    host = "http://localhost"
)


# Enter a context with an instance of the API client
with nauticalstream_workspace.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = nauticalstream_workspace.WorkspacesApi(api_client)
    x_user_id = 'x_user_id_example' # str |  (optional)
    x_workspace_id = 'x_workspace_id_example' # str |  (optional)
    list_categories_request = nauticalstream_workspace.ListCategoriesRequest() # ListCategoriesRequest |  (optional)

    try:
        # List Categories
        api_response = api_instance.list_categories(x_user_id=x_user_id, x_workspace_id=x_workspace_id, list_categories_request=list_categories_request)
        print("The response of WorkspacesApi->list_categories:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WorkspacesApi->list_categories: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_user_id** | **str**|  | [optional] 
 **x_workspace_id** | **str**|  | [optional] 
 **list_categories_request** | [**ListCategoriesRequest**](ListCategoriesRequest.md)|  | [optional] 

### Return type

[**ListCategoriesResponse**](ListCategoriesResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_workspaces**
> ListWorkspacesResponse list_workspaces(x_user_id=x_user_id, x_workspace_id=x_workspace_id, list_workspaces_request=list_workspaces_request)

List Workspaces

### Example


```python
import nauticalstream_workspace
from nauticalstream_workspace.models.list_workspaces_request import ListWorkspacesRequest
from nauticalstream_workspace.models.list_workspaces_response import ListWorkspacesResponse
from nauticalstream_workspace.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = nauticalstream_workspace.Configuration(
    host = "http://localhost"
)


# Enter a context with an instance of the API client
with nauticalstream_workspace.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = nauticalstream_workspace.WorkspacesApi(api_client)
    x_user_id = 'x_user_id_example' # str |  (optional)
    x_workspace_id = 'x_workspace_id_example' # str |  (optional)
    list_workspaces_request = nauticalstream_workspace.ListWorkspacesRequest() # ListWorkspacesRequest |  (optional)

    try:
        # List Workspaces
        api_response = api_instance.list_workspaces(x_user_id=x_user_id, x_workspace_id=x_workspace_id, list_workspaces_request=list_workspaces_request)
        print("The response of WorkspacesApi->list_workspaces:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WorkspacesApi->list_workspaces: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_user_id** | **str**|  | [optional] 
 **x_workspace_id** | **str**|  | [optional] 
 **list_workspaces_request** | [**ListWorkspacesRequest**](ListWorkspacesRequest.md)|  | [optional] 

### Return type

[**ListWorkspacesResponse**](ListWorkspacesResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **remove_amenity_from_category**
> remove_amenity_from_category(category_id, remove_amenity_from_category_request, x_user_id=x_user_id, x_workspace_id=x_workspace_id)

Remove Amenity From Category

### Example


```python
import nauticalstream_workspace
from nauticalstream_workspace.models.remove_amenity_from_category_request import RemoveAmenityFromCategoryRequest
from nauticalstream_workspace.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = nauticalstream_workspace.Configuration(
    host = "http://localhost"
)


# Enter a context with an instance of the API client
with nauticalstream_workspace.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = nauticalstream_workspace.WorkspacesApi(api_client)
    category_id = 56 # int | 
    remove_amenity_from_category_request = nauticalstream_workspace.RemoveAmenityFromCategoryRequest() # RemoveAmenityFromCategoryRequest | 
    x_user_id = 'x_user_id_example' # str |  (optional)
    x_workspace_id = 'x_workspace_id_example' # str |  (optional)

    try:
        # Remove Amenity From Category
        api_instance.remove_amenity_from_category(category_id, remove_amenity_from_category_request, x_user_id=x_user_id, x_workspace_id=x_workspace_id)
    except Exception as e:
        print("Exception when calling WorkspacesApi->remove_amenity_from_category: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **category_id** | **int**|  | 
 **remove_amenity_from_category_request** | [**RemoveAmenityFromCategoryRequest**](RemoveAmenityFromCategoryRequest.md)|  | 
 **x_user_id** | **str**|  | [optional] 
 **x_workspace_id** | **str**|  | [optional] 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**204** | Successful Response |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_workspace**
> Workspace update_workspace(workspace_id, update_workspace_request, x_user_id=x_user_id, x_workspace_id=x_workspace_id)

Update Workspace

### Example


```python
import nauticalstream_workspace
from nauticalstream_workspace.models.update_workspace_request import UpdateWorkspaceRequest
from nauticalstream_workspace.models.workspace import Workspace
from nauticalstream_workspace.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = nauticalstream_workspace.Configuration(
    host = "http://localhost"
)


# Enter a context with an instance of the API client
with nauticalstream_workspace.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = nauticalstream_workspace.WorkspacesApi(api_client)
    workspace_id = 56 # int | 
    update_workspace_request = nauticalstream_workspace.UpdateWorkspaceRequest() # UpdateWorkspaceRequest | 
    x_user_id = 'x_user_id_example' # str |  (optional)
    x_workspace_id = 'x_workspace_id_example' # str |  (optional)

    try:
        # Update Workspace
        api_response = api_instance.update_workspace(workspace_id, update_workspace_request, x_user_id=x_user_id, x_workspace_id=x_workspace_id)
        print("The response of WorkspacesApi->update_workspace:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WorkspacesApi->update_workspace: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_id** | **int**|  | 
 **update_workspace_request** | [**UpdateWorkspaceRequest**](UpdateWorkspaceRequest.md)|  | 
 **x_user_id** | **str**|  | [optional] 
 **x_workspace_id** | **str**|  | [optional] 

### Return type

[**Workspace**](Workspace.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_workspace_feature**
> Feature update_workspace_feature(workspace_id, feature_id, body, x_user_id=x_user_id, x_workspace_id=x_workspace_id)

Update Workspace Feature

Update a feature within a workspace

### Example


```python
import nauticalstream_workspace
from nauticalstream_workspace.models.feature import Feature
from nauticalstream_workspace.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = nauticalstream_workspace.Configuration(
    host = "http://localhost"
)


# Enter a context with an instance of the API client
with nauticalstream_workspace.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = nauticalstream_workspace.WorkspacesApi(api_client)
    workspace_id = 56 # int | 
    feature_id = 'feature_id_example' # str | 
    body = None # object | 
    x_user_id = 'x_user_id_example' # str |  (optional)
    x_workspace_id = 'x_workspace_id_example' # str |  (optional)

    try:
        # Update Workspace Feature
        api_response = api_instance.update_workspace_feature(workspace_id, feature_id, body, x_user_id=x_user_id, x_workspace_id=x_workspace_id)
        print("The response of WorkspacesApi->update_workspace_feature:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WorkspacesApi->update_workspace_feature: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_id** | **int**|  | 
 **feature_id** | **str**|  | 
 **body** | **object**|  | 
 **x_user_id** | **str**|  | [optional] 
 **x_workspace_id** | **str**|  | [optional] 

### Return type

[**Feature**](Feature.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

