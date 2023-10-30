# MetricsAPI

All URIs are relative to *https://backend.arkhon.test.arkhon.digital*

Method | HTTP request | Description
------------- | ------------- | -------------
[**metricsControllerMetrics**](MetricsAPI.md#metricscontrollermetrics) | **GET** /v1/metrics | Get Metrics


# **metricsControllerMetrics**
```swift
    open class func metricsControllerMetrics(completion: @escaping (_ data: String?, _ error: Error?) -> Void)
```

Get Metrics

Returns all Prometheus metrics which the instance provides.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient


// Get Metrics
MetricsAPI.metricsControllerMetrics() { (response, error) in
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

**String**

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

