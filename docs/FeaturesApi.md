# nauticalstream_workspace.FeaturesApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**are_features_active**](FeaturesApi.md#are_features_active) | **POST** /workspaces/features/batch/is-active | Are Features Active
[**get_features_batch**](FeaturesApi.md#get_features_batch) | **POST** /workspaces/features/batch | Get Features Batch


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
    api_instance = nauticalstream_workspace.FeaturesApi(api_client)
    batch_workspace_amenity_check_request = nauticalstream_workspace.BatchWorkspaceAmenityCheckRequest() # BatchWorkspaceAmenityCheckRequest | 
    x_user_id = 'x_user_id_example' # str |  (optional)
    x_workspace_id = 'x_workspace_id_example' # str |  (optional)

    try:
        # Are Features Active
        api_response = api_instance.are_features_active(batch_workspace_amenity_check_request, x_user_id=x_user_id, x_workspace_id=x_workspace_id)
        print("The response of FeaturesApi->are_features_active:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FeaturesApi->are_features_active: %s\n" % e)
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
    api_instance = nauticalstream_workspace.FeaturesApi(api_client)
    get_features_batch_request = nauticalstream_workspace.GetFeaturesBatchRequest() # GetFeaturesBatchRequest | 
    x_user_id = 'x_user_id_example' # str |  (optional)
    x_workspace_id = 'x_workspace_id_example' # str |  (optional)

    try:
        # Get Features Batch
        api_response = api_instance.get_features_batch(get_features_batch_request, x_user_id=x_user_id, x_workspace_id=x_workspace_id)
        print("The response of FeaturesApi->get_features_batch:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FeaturesApi->get_features_batch: %s\n" % e)
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

