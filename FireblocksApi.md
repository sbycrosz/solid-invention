# FireblocksAPI

All URIs are relative to *https://backend.arkhon.test.arkhon.digital*

Method | HTTP request | Description
------------- | ------------- | -------------
[**fireblocksControllerBalance**](FireblocksAPI.md#fireblockscontrollerbalance) | **GET** /v1/fireblocks/balance | Get FireBlocks balance
[**fireblocksControllerCustodyMovements**](FireblocksAPI.md#fireblockscontrollercustodymovements) | **GET** /v1/fireblocks/custodyMovements | Retrieve FireBlocks transaction data
[**fireblocksControllerStatistics**](FireblocksAPI.md#fireblockscontrollerstatistics) | **GET** /v1/fireblocks/statistics | Get Statistics across all fees from individual custody movements


# **fireblocksControllerBalance**
```swift
    open class func fireblocksControllerBalance(completion: @escaping (_ data: [AssetResponseDto]?, _ error: Error?) -> Void)
```

Get FireBlocks balance

Get FireBlocks balance.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient


// Get FireBlocks balance
FireblocksAPI.fireblocksControllerBalance() { (response, error) in
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

[**[AssetResponseDto]**](AssetResponseDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **fireblocksControllerCustodyMovements**
```swift
    open class func fireblocksControllerCustodyMovements(completion: @escaping (_ data: [CustodyTransactionDto]?, _ error: Error?) -> Void)
```

Retrieve FireBlocks transaction data

Retrieves FireBlocks transaction data from Redis.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient


// Retrieve FireBlocks transaction data
FireblocksAPI.fireblocksControllerCustodyMovements() { (response, error) in
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

[**[CustodyTransactionDto]**](CustodyTransactionDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **fireblocksControllerStatistics**
```swift
    open class func fireblocksControllerStatistics(stats: [String], completion: @escaping (_ data: [CustodyStatisticDto]?, _ error: Error?) -> Void)
```

Get Statistics across all fees from individual custody movements

Returns desired statistic(s) across all transactions.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let stats = ["inner_example"] // [String] | Specifies statistics to be evaluated across transactions.

// Get Statistics across all fees from individual custody movements
FireblocksAPI.fireblocksControllerStatistics(stats: stats) { (response, error) in
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
 **stats** | [**[String]**](String.md) | Specifies statistics to be evaluated across transactions. | 

### Return type

[**[CustodyStatisticDto]**](CustodyStatisticDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

