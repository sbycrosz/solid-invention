# LoggingAPI

All URIs are relative to *https://backend.arkhon.test.arkhon.digital*

Method | HTTP request | Description
------------- | ------------- | -------------
[**loggingControllerLogs**](LoggingAPI.md#loggingcontrollerlogs) | **POST** /v1/logs | Post Logs


# **loggingControllerLogs**
```swift
    open class func loggingControllerLogs(loggingDto: LoggingDto, completion: @escaping (_ data: Void?, _ error: Error?) -> Void)
```

Post Logs

Logs given body so it can be analyzed later using ALM tools.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let loggingDto = LoggingDto(platform: "platform_example", logEntries: [123]) // LoggingDto | 

// Post Logs
LoggingAPI.loggingControllerLogs(loggingDto: loggingDto) { (response, error) in
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

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **loggingDto** | [**LoggingDto**](LoggingDto.md) |  | 

### Return type

Void (empty response body)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

