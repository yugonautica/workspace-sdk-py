# nauticalstream_workspace.HealthApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**liveness_check**](HealthApi.md#liveness_check) | **GET** /health/liveness | Liveness Check
[**readiness_check**](HealthApi.md#readiness_check) | **GET** /health/readiness | Readiness Check


# **liveness_check**
> LivenessResponse liveness_check()

Liveness Check

Liveness endpoint.
Always returns 200 if the server process is alive.

### Example


```python
import nauticalstream_workspace
from nauticalstream_workspace.models.liveness_response import LivenessResponse
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
    api_instance = nauticalstream_workspace.HealthApi(api_client)

    try:
        # Liveness Check
        api_response = api_instance.liveness_check()
        print("The response of HealthApi->liveness_check:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling HealthApi->liveness_check: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**LivenessResponse**](LivenessResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **readiness_check**
> ReadinessResponse readiness_check()

Readiness Check

Readiness endpoint.
Returns 200 if DB is reachable, 503 otherwise.

### Example


```python
import nauticalstream_workspace
from nauticalstream_workspace.models.readiness_response import ReadinessResponse
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
    api_instance = nauticalstream_workspace.HealthApi(api_client)

    try:
        # Readiness Check
        api_response = api_instance.readiness_check()
        print("The response of HealthApi->readiness_check:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling HealthApi->readiness_check: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**ReadinessResponse**](ReadinessResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |
**503** | Service Unavailable |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

