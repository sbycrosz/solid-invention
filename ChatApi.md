# ChatAPI

All URIs are relative to *https://backend.arkhon.test.arkhon.digital*

Method | HTTP request | Description
------------- | ------------- | -------------
[**chatControllerGetChatHistories**](ChatAPI.md#chatcontrollergetchathistories) | **GET** /v1/accounts/{accountId}/chat | Get Chat History
[**chatControllerPostMessage**](ChatAPI.md#chatcontrollerpostmessage) | **POST** /v1/accounts/{accountId}/chat | Post Chat Message


# **chatControllerGetChatHistories**
```swift
    open class func chatControllerGetChatHistories(accountId: Double, completion: @escaping (_ data: SlackHistoryResponseDto?, _ error: Error?) -> Void)
```

Get Chat History

Returns chat history.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let accountId = 987 // Double | 

// Get Chat History
ChatAPI.chatControllerGetChatHistories(accountId: accountId) { (response, error) in
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
 **accountId** | **Double** |  | 

### Return type

[**SlackHistoryResponseDto**](SlackHistoryResponseDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **chatControllerPostMessage**
```swift
    open class func chatControllerPostMessage(accountId: Double, slackMessageRequestDto: SlackMessageRequestDto, completion: @escaping (_ data: SlackMessageResponseDto?, _ error: Error?) -> Void)
```

Post Chat Message

Posts a new message in chat.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let accountId = 987 // Double | 
let slackMessageRequestDto = SlackMessageRequestDto(message: "message_example") // SlackMessageRequestDto | 

// Post Chat Message
ChatAPI.chatControllerPostMessage(accountId: accountId, slackMessageRequestDto: slackMessageRequestDto) { (response, error) in
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
 **accountId** | **Double** |  | 
 **slackMessageRequestDto** | [**SlackMessageRequestDto**](SlackMessageRequestDto.md) |  | 

### Return type

[**SlackMessageResponseDto**](SlackMessageResponseDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

