# HealthAPI

All URIs are relative to *https://backend.arkhon.test.arkhon.digital*

Method | HTTP request | Description
------------- | ------------- | -------------
[**backendHealthControllerCheckLiveness**](HealthAPI.md#backendhealthcontrollercheckliveness) | **GET** /v1/health/liveness | Check if the component is alive
[**backendHealthControllerCheckReadiness**](HealthAPI.md#backendhealthcontrollercheckreadiness) | **GET** /v1/health/readiness | Check if the component is ready to work


# **backendHealthControllerCheckLiveness**
```swift
    open class func backendHealthControllerCheckLiveness(completion: @escaping (_ data: BackendHealthControllerCheckLiveness200Response?, _ error: Error?) -> Void)
```

Check if the component is alive

Returns true if the most basic needs of the component are met, in our case database connectivity.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient


// Check if the component is alive
HealthAPI.backendHealthControllerCheckLiveness() { (response, error) in
    guard error == nil else {
        print(error)
        return
    }

    if (response) {
        dump(response)
    }
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**BackendHealthControllerCheckLiveness200Response**](BackendHealthControllerCheckLiveness200Response.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **backendHealthControllerCheckReadiness**
```swift
    open class func backendHealthControllerCheckReadiness(completion: @escaping (_ data: BackendHealthControllerCheckLiveness200Response?, _ error: Error?) -> Void)
```

Check if the component is ready to work

Returns true if the component is ready to serve client requests.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient


// Check if the component is ready to work
HealthAPI.backendHealthControllerCheckReadiness() { (response, error) in
    guard error == nil else {
        print(error)
        return
    }

    if (response) {
        dump(response)
    }
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**BackendHealthControllerCheckLiveness200Response**](BackendHealthControllerCheckLiveness200Response.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

