# TransferAPI

All URIs are relative to *https://backend.arkhon.test.arkhon.digital*

Method | HTTP request | Description
------------- | ------------- | -------------
[**clientTransferControllerCreateClientDeposit**](TransferAPI.md#clienttransfercontrollercreateclientdeposit) | **POST** /v1/transfers/clientDeposit | Create Client Deposit (External into Arkhon)
[**clientTransferControllerCreateClientWithdrawal**](TransferAPI.md#clienttransfercontrollercreateclientwithdrawal) | **POST** /v1/transfers/clientWithdrawal | Create Client Withdrawal (External into Arkhon)
[**transferControllerAggregates**](TransferAPI.md#transfercontrolleraggregates) | **POST** /v1/transfers/aggregates | Get Aggregates Transfers
[**transferControllerCount**](TransferAPI.md#transfercontrollercount) | **POST** /v1/transfers/count | Count Transfers
[**transferControllerCreate**](TransferAPI.md#transfercontrollercreate) | **POST** /v1/transfers | Create Transfer
[**transferControllerCreateBulk**](TransferAPI.md#transfercontrollercreatebulk) | **POST** /v1/transfers/bulk | Create multiple Transfers
[**transferControllerCreateClientPortfolioToPortfolioTransfer**](TransferAPI.md#transfercontrollercreateclientportfoliotoportfoliotransfer) | **POST** /v1/transfers/client | Create Client Transfer
[**transferControllerCreateClientPortfolioToPortfolioTransfer_0**](TransferAPI.md#transfercontrollercreateclientportfoliotoportfoliotransfer_0) | **POST** /v1/transfers/clientPortfolioToPortfolioTransfer | Create Client Transfer
[**transferControllerDelete**](TransferAPI.md#transfercontrollerdelete) | **DELETE** /v1/transfers/{recordId} | Delete Transfer
[**transferControllerFindAll**](TransferAPI.md#transfercontrollerfindall) | **GET** /v1/transfers | Get all Transfers
[**transferControllerFindOne**](TransferAPI.md#transfercontrollerfindone) | **GET** /v1/transfers/{recordId} | Get single Transfer
[**transferControllerSearch**](TransferAPI.md#transfercontrollersearch) | **POST** /v1/transfers/search | Search Transfers
[**transferControllerStatistics**](TransferAPI.md#transfercontrollerstatistics) | **GET** /v1/transfers/statistics | 
[**transferControllerUpdate**](TransferAPI.md#transfercontrollerupdate) | **PATCH** /v1/transfers/{recordId} | Update single Transfer
[**transferControllerUpdateBulk**](TransferAPI.md#transfercontrollerupdatebulk) | **PATCH** /v1/transfers/bulk | Update multiple Transfers


# **clientTransferControllerCreateClientDeposit**
```swift
    open class func clientTransferControllerCreateClientDeposit(createClientDepositDto: CreateClientDepositDto, completion: @escaping (_ data: TransferDto?, _ error: Error?) -> Void)
```

Create Client Deposit (External into Arkhon)

Creates and returns a Deposit transfer. Triggers compliance check for said transfer in the background and notifies operations of the request.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let createClientDepositDto = CreateClientDepositDto(portfolioId: 123, quantity: "quantity_example", platformId: 123, currency: "currency_example", blockchain: "blockchain_example", walletAddress: "walletAddress_example", isVASP: false) // CreateClientDepositDto | 

// Create Client Deposit (External into Arkhon)
TransferAPI.clientTransferControllerCreateClientDeposit(createClientDepositDto: createClientDepositDto) { (response, error) in
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
 **createClientDepositDto** | [**CreateClientDepositDto**](CreateClientDepositDto.md) |  | 

### Return type

[**TransferDto**](TransferDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **clientTransferControllerCreateClientWithdrawal**
```swift
    open class func clientTransferControllerCreateClientWithdrawal(createClientWithdrawalDto: CreateClientWithdrawalDto, completion: @escaping (_ data: TransferDto?, _ error: Error?) -> Void)
```

Create Client Withdrawal (External into Arkhon)

Creates and returns a Withdrawal transfer and otifies operations of the request.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let createClientWithdrawalDto = CreateClientWithdrawalDto(portfolioId: 123, quantity: "quantity_example", platformId: 123, isVASP: false, walletAddress: "walletAddress_example", blockchain: "blockchain_example", memo: "memo_example", accountNumber: "accountNumber_example", accountName: "accountName_example", bankName: "bankName_example", swift: "swift_example", accountHolderAddress: "accountHolderAddress_example", intermediaryBankAccountNumber: "intermediaryBankAccountNumber_example", intermediaryBankName: "intermediaryBankName_example", intermediaryBankAddress: "intermediaryBankAddress_example", intermediaryBankABA: "intermediaryBankABA_example", intermediaryBankSwift: "intermediaryBankSwift_example", currency: "currency_example") // CreateClientWithdrawalDto | 

// Create Client Withdrawal (External into Arkhon)
TransferAPI.clientTransferControllerCreateClientWithdrawal(createClientWithdrawalDto: createClientWithdrawalDto) { (response, error) in
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
 **createClientWithdrawalDto** | [**CreateClientWithdrawalDto**](CreateClientWithdrawalDto.md) |  | 

### Return type

[**TransferDto**](TransferDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **transferControllerAggregates**
```swift
    open class func transferControllerAggregates(aggregates: [String], body: AnyCodable, completion: @escaping (_ data: [TransferAggregatedData]?, _ error: Error?) -> Void)
```

Get Aggregates Transfers

Get aggregates for deposits & withdrawals only based on time period.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let aggregates = ["inner_example"] // [String] | 
let body = "TODO" // AnyCodable | 

// Get Aggregates Transfers
TransferAPI.transferControllerAggregates(aggregates: aggregates, body: body) { (response, error) in
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
 **aggregates** | [**[String]**](String.md) |  | 
 **body** | **AnyCodable** |  | 

### Return type

[**[TransferAggregatedData]**](TransferAggregatedData.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **transferControllerCount**
```swift
    open class func transferControllerCount(countDto: CountDto, completion: @escaping (_ data: Double?, _ error: Error?) -> Void)
```

Count Transfers

Counts matching transfers to which the logged in user has access.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let countDto = CountDto(filterOptions: [FilterOptionDto(values: [FilterOptionDto_values_inner()], field: "field_example", _operator: "_operator_example", subFilters: [nil])], returnSoftDeletedEntities: false) // CountDto | 

// Count Transfers
TransferAPI.transferControllerCount(countDto: countDto) { (response, error) in
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

# **transferControllerCreate**
```swift
    open class func transferControllerCreate(createTransferDto: CreateTransferDto, completion: @escaping (_ data: TransferDto?, _ error: Error?) -> Void)
```

Create Transfer

Creates and returns a transfer. All transfers are always made from the viewpoint of the main portfolio. Either secondaryPortfolioId or platformId is not NULL, but not both

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let createTransferDto = CreateTransferDto(portfolioId: 123, secondaryPortfolioId: 123, userId: 123, executedBy: 123, quantity: "quantity_example", platformId: 123, type: "type_example", currency: "currency_example", status: "status_example", platformRefId: "platformRefId_example", clientRefId: "clientRefId_example", receiptTime: Date(), creditTime: Date(), withdrawalTime: Date(), comment: "comment_example") // CreateTransferDto | 

// Create Transfer
TransferAPI.transferControllerCreate(createTransferDto: createTransferDto) { (response, error) in
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
 **createTransferDto** | [**CreateTransferDto**](CreateTransferDto.md) |  | 

### Return type

[**TransferDto**](TransferDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **transferControllerCreateBulk**
```swift
    open class func transferControllerCreateBulk(createTransferDto: [CreateTransferDto], completion: @escaping (_ data: [TransferDto]?, _ error: Error?) -> Void)
```

Create multiple Transfers

Creates and returns multiple transfers.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let createTransferDto = [CreateTransferDto(portfolioId: 123, secondaryPortfolioId: 123, userId: 123, executedBy: 123, quantity: "quantity_example", platformId: 123, type: "type_example", currency: "currency_example", status: "status_example", platformRefId: "platformRefId_example", clientRefId: "clientRefId_example", receiptTime: Date(), creditTime: Date(), withdrawalTime: Date(), comment: "comment_example")] // [CreateTransferDto] | 

// Create multiple Transfers
TransferAPI.transferControllerCreateBulk(createTransferDto: createTransferDto) { (response, error) in
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
 **createTransferDto** | [**[CreateTransferDto]**](CreateTransferDto.md) |  | 

### Return type

[**[TransferDto]**](TransferDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **transferControllerCreateClientPortfolioToPortfolioTransfer**
```swift
    open class func transferControllerCreateClientPortfolioToPortfolioTransfer(createClientTransferDto: CreateClientTransferDto, completion: @escaping (_ data: TransferDto?, _ error: Error?) -> Void)
```

Create Client Transfer

Creates and returns a transfer. All transfers are always made from the viewpoint of the main portfolio. Either secondaryPortfolioId or platformId is not NULL, but not both.This is similar to the /create endpoint, but it is meant to be used by the client.Only require {portfolioId, secondaryPortfolioId, currency, type, quantity} for Client Transfer

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let createClientTransferDto = CreateClientTransferDto(portfolioId: 123, secondaryPortfolioId: 123, quantity: "quantity_example", type: "type_example", currency: "currency_example") // CreateClientTransferDto | 

// Create Client Transfer
TransferAPI.transferControllerCreateClientPortfolioToPortfolioTransfer(createClientTransferDto: createClientTransferDto) { (response, error) in
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
 **createClientTransferDto** | [**CreateClientTransferDto**](CreateClientTransferDto.md) |  | 

### Return type

[**TransferDto**](TransferDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **transferControllerCreateClientPortfolioToPortfolioTransfer_0**
```swift
    open class func transferControllerCreateClientPortfolioToPortfolioTransfer_0(createClientTransferDto: CreateClientTransferDto, completion: @escaping (_ data: TransferDto?, _ error: Error?) -> Void)
```

Create Client Transfer

Creates and returns a transfer. All transfers are always made from the viewpoint of the main portfolio. Either secondaryPortfolioId or platformId is not NULL, but not both.This is similar to the /create endpoint, but it is meant to be used by the client.Only require {portfolioId, secondaryPortfolioId, currency, type, quantity} for Client Transfer

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let createClientTransferDto = CreateClientTransferDto(portfolioId: 123, secondaryPortfolioId: 123, quantity: "quantity_example", type: "type_example", currency: "currency_example") // CreateClientTransferDto | 

// Create Client Transfer
TransferAPI.transferControllerCreateClientPortfolioToPortfolioTransfer_0(createClientTransferDto: createClientTransferDto) { (response, error) in
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
 **createClientTransferDto** | [**CreateClientTransferDto**](CreateClientTransferDto.md) |  | 

### Return type

[**TransferDto**](TransferDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **transferControllerDelete**
```swift
    open class func transferControllerDelete(recordId: Double, completion: @escaping (_ data: String?, _ error: Error?) -> Void)
```

Delete Transfer

Deletes a transfer.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let recordId = 987 // Double | 

// Delete Transfer
TransferAPI.transferControllerDelete(recordId: recordId) { (response, error) in
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
 **recordId** | **Double** |  | 

### Return type

**String**

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **transferControllerFindAll**
```swift
    open class func transferControllerFindAll(page: Double, pageSize: Double, completion: @escaping (_ data: [TransferDto]?, _ error: Error?) -> Void)
```

Get all Transfers

Returns all transfers to which the logged in user has access.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let page = 987 // Double | 
let pageSize = 987 // Double | 

// Get all Transfers
TransferAPI.transferControllerFindAll(page: page, pageSize: pageSize) { (response, error) in
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
 **page** | **Double** |  | 
 **pageSize** | **Double** |  | 

### Return type

[**[TransferDto]**](TransferDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **transferControllerFindOne**
```swift
    open class func transferControllerFindOne(recordId: Double, withPortfolio: Bool? = nil, completion: @escaping (_ data: TransferDto?, _ error: Error?) -> Void)
```

Get single Transfer

Returns single transfer if the logged in user has access.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let recordId = 987 // Double | 
let withPortfolio = true // Bool | Return transfer with portfolio object attached. (optional)

// Get single Transfer
TransferAPI.transferControllerFindOne(recordId: recordId, withPortfolio: withPortfolio) { (response, error) in
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
 **recordId** | **Double** |  | 
 **withPortfolio** | **Bool** | Return transfer with portfolio object attached. | [optional] 

### Return type

[**TransferDto**](TransferDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **transferControllerSearch**
```swift
    open class func transferControllerSearch(searchDto: SearchDto, completion: @escaping (_ data: [TransferDto]?, _ error: Error?) -> Void)
```

Search Transfers

Returns matching transfers to which the logged in user has access.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let searchDto = SearchDto(orderOption: [OrderOption(field: "field_example", direction: "direction_example")], pageSize: 123, page: 123, enrichments: ["enrichments_example"], filterOptions: [FilterOptionDto(values: [FilterOptionDto_values_inner()], field: "field_example", _operator: "_operator_example", subFilters: [nil])], returnSoftDeletedEntities: false) // SearchDto | 

// Search Transfers
TransferAPI.transferControllerSearch(searchDto: searchDto) { (response, error) in
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

[**[TransferDto]**](TransferDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **transferControllerStatistics**
```swift
    open class func transferControllerStatistics(stats: [String], completion: @escaping (_ data: TransferDto?, _ error: Error?) -> Void)
```



### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let stats = ["inner_example"] // [String] | 

TransferAPI.transferControllerStatistics(stats: stats) { (response, error) in
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
 **stats** | [**[String]**](String.md) |  | 

### Return type

[**TransferDto**](TransferDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **transferControllerUpdate**
```swift
    open class func transferControllerUpdate(recordId: Double, updateTransferDto: UpdateTransferDto, completion: @escaping (_ data: TransferDto?, _ error: Error?) -> Void)
```

Update single Transfer

Updates and returns single transfer.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let recordId = 987 // Double | 
let updateTransferDto = UpdateTransferDto(recordId: 123, portfolioId: 123, secondaryPortfolioId: 123, userId: 123, executedBy: 123, quantity: "quantity_example", platformId: 123, version: 123, type: "type_example", currency: "currency_example", status: "status_example", platformRefId: "platformRefId_example", clientRefId: "clientRefId_example", receiptTime: Date(), creditTime: Date(), withdrawalTime: Date(), comment: "comment_example") // UpdateTransferDto | 

// Update single Transfer
TransferAPI.transferControllerUpdate(recordId: recordId, updateTransferDto: updateTransferDto) { (response, error) in
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
 **recordId** | **Double** |  | 
 **updateTransferDto** | [**UpdateTransferDto**](UpdateTransferDto.md) |  | 

### Return type

[**TransferDto**](TransferDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **transferControllerUpdateBulk**
```swift
    open class func transferControllerUpdateBulk(updateTransferDto: [UpdateTransferDto], completion: @escaping (_ data: [TransferDto]?, _ error: Error?) -> Void)
```

Update multiple Transfers

Updates and returns multiple transfers.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let updateTransferDto = [UpdateTransferDto(recordId: 123, portfolioId: 123, secondaryPortfolioId: 123, userId: 123, executedBy: 123, quantity: "quantity_example", platformId: 123, version: 123, type: "type_example", currency: "currency_example", status: "status_example", platformRefId: "platformRefId_example", clientRefId: "clientRefId_example", receiptTime: Date(), creditTime: Date(), withdrawalTime: Date(), comment: "comment_example")] // [UpdateTransferDto] | 

// Update multiple Transfers
TransferAPI.transferControllerUpdateBulk(updateTransferDto: updateTransferDto) { (response, error) in
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
 **updateTransferDto** | [**[UpdateTransferDto]**](UpdateTransferDto.md) |  | 

### Return type

[**[TransferDto]**](TransferDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

