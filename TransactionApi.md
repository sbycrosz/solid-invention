# TransactionAPI

All URIs are relative to *https://backend.arkhon.test.arkhon.digital*

Method | HTTP request | Description
------------- | ------------- | -------------
[**transactionControllerCount**](TransactionAPI.md#transactioncontrollercount) | **POST** /v1/transactions/count | Count Transfers
[**transactionControllerGetBlockedFunds**](TransactionAPI.md#transactioncontrollergetblockedfunds) | **POST** /v1/transactions/blocked | Check for blocked funds
[**transactionControllerHasOngoingTransactions**](TransactionAPI.md#transactioncontrollerhasongoingtransactions) | **POST** /v1/transactions/ongoing | Check for ongoing transactions
[**transactionControllerSearch**](TransactionAPI.md#transactioncontrollersearch) | **POST** /v1/transactions/search | Search Transfers


# **transactionControllerCount**
```swift
    open class func transactionControllerCount(countDto: CountDto, completion: @escaping (_ data: Double?, _ error: Error?) -> Void)
```

Count Transfers

Counts matching orders & transfers to which the logged in user has access.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let countDto = CountDto(filterOptions: [FilterOptionDto(values: [FilterOptionDto_values_inner()], field: "field_example", _operator: "_operator_example", subFilters: [nil])], returnSoftDeletedEntities: false) // CountDto | 

// Count Transfers
TransactionAPI.transactionControllerCount(countDto: countDto) { (response, error) in
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
 **countDto** | [**CountDto**](CountDto.md) |  | 

### Return type

**Double**

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **transactionControllerGetBlockedFunds**
```swift
    open class func transactionControllerGetBlockedFunds(blockedFundsRequestDto: BlockedFundsRequestDto, completion: @escaping (_ data: String?, _ error: Error?) -> Void)
```

Check for blocked funds

Returns blocked funds, or 0 if no funds blocked

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let blockedFundsRequestDto = BlockedFundsRequestDto(portfolioId: 123, currency: "currency_example") // BlockedFundsRequestDto | 

// Check for blocked funds
TransactionAPI.transactionControllerGetBlockedFunds(blockedFundsRequestDto: blockedFundsRequestDto) { (response, error) in
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
 **blockedFundsRequestDto** | [**BlockedFundsRequestDto**](BlockedFundsRequestDto.md) |  | 

### Return type

**String**

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **transactionControllerHasOngoingTransactions**
```swift
    open class func transactionControllerHasOngoingTransactions(ongoingTransactionRequestDto: OngoingTransactionRequestDto, completion: @escaping (_ data: Bool?, _ error: Error?) -> Void)
```

Check for ongoing transactions

Returns true if ongoing transactions; false otherwise.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let ongoingTransactionRequestDto = OngoingTransactionRequestDto(portfolioId: 123, latestPortfolioAssetHistoryDt: Date(), currency: "currency_example") // OngoingTransactionRequestDto | 

// Check for ongoing transactions
TransactionAPI.transactionControllerHasOngoingTransactions(ongoingTransactionRequestDto: ongoingTransactionRequestDto) { (response, error) in
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
 **ongoingTransactionRequestDto** | [**OngoingTransactionRequestDto**](OngoingTransactionRequestDto.md) |  | 

### Return type

**Bool**

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **transactionControllerSearch**
```swift
    open class func transactionControllerSearch(searchDto: SearchDto, completion: @escaping (_ data: [TransactionControllerSearch200ResponseInner]?, _ error: Error?) -> Void)
```

Search Transfers

Returns matching orders & transfers to which the logged in user has access.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let searchDto = SearchDto(orderOption: [OrderOption(field: "field_example", direction: "direction_example")], pageSize: 123, page: 123, enrichments: ["enrichments_example"], filterOptions: [FilterOptionDto(values: [FilterOptionDto_values_inner()], field: "field_example", _operator: "_operator_example", subFilters: [nil])], returnSoftDeletedEntities: false) // SearchDto | 

// Search Transfers
TransactionAPI.transactionControllerSearch(searchDto: searchDto) { (response, error) in
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
 **searchDto** | [**SearchDto**](SearchDto.md) |  | 

### Return type

[**[TransactionControllerSearch200ResponseInner]**](TransactionControllerSearch200ResponseInner.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

