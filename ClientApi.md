# ClientAPI

All URIs are relative to *https://backend.arkhon.test.arkhon.digital*

Method | HTTP request | Description
------------- | ------------- | -------------
[**clientControllerFind**](ClientAPI.md#clientcontrollerfind) | **GET** /v1/client | Get Client
[**clientControllerUpdate**](ClientAPI.md#clientcontrollerupdate) | **PATCH** /v1/client | Update Client


# **clientControllerFind**
```swift
    open class func clientControllerFind(completion: @escaping (_ data: ClientDto?, _ error: Error?) -> Void)
```

Get Client

Returns the client.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient


// Get Client
ClientAPI.clientControllerFind() { (response, error) in
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

[**ClientDto**](ClientDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **clientControllerUpdate**
```swift
    open class func clientControllerUpdate(updateClientDto: UpdateClientDto, completion: @escaping (_ data: ClientDto?, _ error: Error?) -> Void)
```

Update Client

Updates and returns the client

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let updateClientDto = UpdateClientDto(recordId: 123, name: "name_example", defaultNotificationEmail: "defaultNotificationEmail_example") // UpdateClientDto | 

// Update Client
ClientAPI.clientControllerUpdate(updateClientDto: updateClientDto) { (response, error) in
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
 **updateClientDto** | [**UpdateClientDto**](UpdateClientDto.md) |  | 

### Return type

[**ClientDto**](ClientDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

