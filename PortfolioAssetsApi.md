# PortfolioAssetsAPI

All URIs are relative to *https://backend.arkhon.test.arkhon.digital*

Method | HTTP request | Description
------------- | ------------- | -------------
[**portfolioAssetControllerFindCurrent**](PortfolioAssetsAPI.md#portfolioassetcontrollerfindcurrent) | **GET** /v1/accounts/{accountId}/portfolios/{portfolioId}/assets | Get all Portfolio Assets
[**portfolioAssetControllerFindCurrentForSingleSymbol**](PortfolioAssetsAPI.md#portfolioassetcontrollerfindcurrentforsinglesymbol) | **GET** /v1/accounts/{accountId}/portfolios/{portfolioId}/assets/{symbol} | Get Portfolio Asset for a given symbol
[**portfolioAssetControllerSearch**](PortfolioAssetsAPI.md#portfolioassetcontrollersearch) | **POST** /v1/accounts/{accountId}/portfolios/{portfolioId}/assets/search | Search Portfolio Assets


# **portfolioAssetControllerFindCurrent**
```swift
    open class func portfolioAssetControllerFindCurrent(accountId: Double, portfolioId: Double, completion: @escaping (_ data: [PortfolioAssetHistoryDto]?, _ error: Error?) -> Void)
```

Get all Portfolio Assets

Returns all portfolio assets.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let accountId = 987 // Double | 
let portfolioId = 987 // Double | 

// Get all Portfolio Assets
PortfolioAssetsAPI.portfolioAssetControllerFindCurrent(accountId: accountId, portfolioId: portfolioId) { (response, error) in
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
 **portfolioId** | **Double** |  | 

### Return type

[**[PortfolioAssetHistoryDto]**](PortfolioAssetHistoryDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **portfolioAssetControllerFindCurrentForSingleSymbol**
```swift
    open class func portfolioAssetControllerFindCurrentForSingleSymbol(accountId: Double, portfolioId: Double, symbol: String, completion: @escaping (_ data: PortfolioAssetHistoryDto?, _ error: Error?) -> Void)
```

Get Portfolio Asset for a given symbol

Returns current portfolio asset quantity.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let accountId = 987 // Double | 
let portfolioId = 987 // Double | 
let symbol = "symbol_example" // String | 

// Get Portfolio Asset for a given symbol
PortfolioAssetsAPI.portfolioAssetControllerFindCurrentForSingleSymbol(accountId: accountId, portfolioId: portfolioId, symbol: symbol) { (response, error) in
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
 **portfolioId** | **Double** |  | 
 **symbol** | **String** |  | 

### Return type

[**PortfolioAssetHistoryDto**](PortfolioAssetHistoryDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **portfolioAssetControllerSearch**
```swift
    open class func portfolioAssetControllerSearch(accountId: Double, portfolioId: Double, searchDto: SearchDto, completion: @escaping (_ data: [PortfolioAssetHistoryDto]?, _ error: Error?) -> Void)
```

Search Portfolio Assets

Returns matching portfolio assets.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let accountId = 987 // Double | 
let portfolioId = 987 // Double | 
let searchDto = SearchDto(orderOption: [OrderOption(field: "field_example", direction: "direction_example")], pageSize: 123, page: 123, enrichments: ["enrichments_example"], filterOptions: [FilterOptionDto(values: [FilterOptionDto_values_inner()], field: "field_example", _operator: "_operator_example", subFilters: [nil])], returnSoftDeletedEntities: false) // SearchDto | 

// Search Portfolio Assets
PortfolioAssetsAPI.portfolioAssetControllerSearch(accountId: accountId, portfolioId: portfolioId, searchDto: searchDto) { (response, error) in
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
 **portfolioId** | **Double** |  | 
 **searchDto** | [**SearchDto**](SearchDto.md) |  | 

### Return type

[**[PortfolioAssetHistoryDto]**](PortfolioAssetHistoryDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

