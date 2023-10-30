# MarketAPI

All URIs are relative to *https://backend.arkhon.test.arkhon.digital*

Method | HTTP request | Description
------------- | ------------- | -------------
[**marketControllerGetAssetMarketData**](MarketAPI.md#marketcontrollergetassetmarketdata) | **GET** /v1/market/{category} | Get current Market data
[**marketControllerGetAssetTimelineData**](MarketAPI.md#marketcontrollergetassettimelinedata) | **GET** /v1/market/history/asset/{symbol} | Get historical Market data
[**marketControllerGetAssetTimelineInCandleBarFormat**](MarketAPI.md#marketcontrollergetassettimelineincandlebarformat) | **GET** /v1/market/history/asset/{symbol}/candleBars | Get historical Market data (candleBars)
[**marketControllerGetMarketStat**](MarketAPI.md#marketcontrollergetmarketstat) | **GET** /v1/market/stat/{symbol} | Get Market Statistics
[**marketControllerGetPriceData**](MarketAPI.md#marketcontrollergetpricedata) | **GET** /v1/market/current/price | Get current price data
[**marketNewsControllerGetAssetPosts**](MarketAPI.md#marketnewscontrollergetassetposts) | **GET** /v1/market/news/asset/{symbol} | Get Cryptopanic Posts for symbol
[**marketNewsControllerGetPosts**](MarketAPI.md#marketnewscontrollergetposts) | **GET** /v1/market/news | Get Posts from Cryptopanic


# **marketControllerGetAssetMarketData**
```swift
    open class func marketControllerGetAssetMarketData(category: Category_marketControllerGetAssetMarketData, searchSymbolPart: String? = nil, symbol: String? = nil, symbols: String? = nil, quoteSymbol: String? = nil, completion: @escaping (_ data: [AssetMarketDataDto]?, _ error: Error?) -> Void)
```

Get current Market data

Returns current market data.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let category = "category_example" // String | Specify market category to return data for. Available values : all, top_gainers, top_losers, top_traded
let searchSymbolPart = "searchSymbolPart_example" // String | Part of cryptocurrency symbol to search cryptocurrencies for. Cannot be combined with `symbol` or `symbols` (optional)
let symbol = "symbol_example" // String | Specify cryptocurrency symbol to return data for. Cannot be combined with `searchSymbolPart` or `symbols` (optional)
let symbols = "symbols_example" // String | Specify cryptocurrency symbols to return data for. Cannot be combined with `searchSymbolPart` or `symbol` (optional)
let quoteSymbol = "quoteSymbol_example" // String | Specify quote symbol if needed. This can be fiat currency e.g. SGD (optional)

// Get current Market data
MarketAPI.marketControllerGetAssetMarketData(category: category, searchSymbolPart: searchSymbolPart, symbol: symbol, symbols: symbols, quoteSymbol: quoteSymbol) { (response, error) in
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
 **category** | **String** | Specify market category to return data for. Available values : all, top_gainers, top_losers, top_traded | 
 **searchSymbolPart** | **String** | Part of cryptocurrency symbol to search cryptocurrencies for. Cannot be combined with &#x60;symbol&#x60; or &#x60;symbols&#x60; | [optional] 
 **symbol** | **String** | Specify cryptocurrency symbol to return data for. Cannot be combined with &#x60;searchSymbolPart&#x60; or &#x60;symbols&#x60; | [optional] 
 **symbols** | **String** | Specify cryptocurrency symbols to return data for. Cannot be combined with &#x60;searchSymbolPart&#x60; or &#x60;symbol&#x60; | [optional] 
 **quoteSymbol** | **String** | Specify quote symbol if needed. This can be fiat currency e.g. SGD | [optional] 

### Return type

[**[AssetMarketDataDto]**](AssetMarketDataDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **marketControllerGetAssetTimelineData**
```swift
    open class func marketControllerGetAssetTimelineData(symbol: String, timePeriod: TimePeriod_marketControllerGetAssetTimelineData? = nil, timePeriod2: TimePeriod_marketControllerGetAssetTimelineData? = nil, quoteSymbol: String? = nil, completion: @escaping (_ data: [TimelineDataDto]?, _ error: Error?) -> Void)
```

Get historical Market data

Returns historical market data for a single symbol.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let symbol = "symbol_example" // String | Specify cryptocurrency symbol to return data for. Cannot be combined with `searchSymbolPart`
let timePeriod = "timePeriod_example" // String | Specify time periods to return data for. accept 1h,1d,7d,30d, 365d or AllTime. 1d is default (optional)
let timePeriod2 = "timePeriod2_example" // String | Specify time periods to return data for. accept 1h,1d,7d,30d, 365d or AllTime. 1d is default (optional)
let quoteSymbol = "quoteSymbol_example" // String | Specify quote symbol if needed. This can be fiat currency e.g. SGD (optional)

// Get historical Market data
MarketAPI.marketControllerGetAssetTimelineData(symbol: symbol, timePeriod: timePeriod, timePeriod2: timePeriod2, quoteSymbol: quoteSymbol) { (response, error) in
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
 **symbol** | **String** | Specify cryptocurrency symbol to return data for. Cannot be combined with &#x60;searchSymbolPart&#x60; | 
 **timePeriod** | **String** | Specify time periods to return data for. accept 1h,1d,7d,30d, 365d or AllTime. 1d is default | [optional] 
 **timePeriod2** | **String** | Specify time periods to return data for. accept 1h,1d,7d,30d, 365d or AllTime. 1d is default | [optional] 
 **quoteSymbol** | **String** | Specify quote symbol if needed. This can be fiat currency e.g. SGD | [optional] 

### Return type

[**[TimelineDataDto]**](TimelineDataDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **marketControllerGetAssetTimelineInCandleBarFormat**
```swift
    open class func marketControllerGetAssetTimelineInCandleBarFormat(symbol: String, timePeriod: TimePeriod_marketControllerGetAssetTimelineInCandleBarFormat? = nil, quoteSymbol: String? = nil, completion: @escaping (_ data: [AssetMarketPeriodDto]?, _ error: Error?) -> Void)
```

Get historical Market data (candleBars)

Returns historical market data for a single symbol for CandleBars display purposes.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let symbol = "symbol_example" // String | Specify cryptocurrency symbol to return data for. Cannot be combined with `searchSymbolPart`
let timePeriod = "timePeriod_example" // String | Specify time periods to return data for. accept 1h,1d,7d,30d, 365d or AllTime. 1d is default (optional)
let quoteSymbol = "quoteSymbol_example" // String | Specify quote symbol if needed. This can be fiat currency e.g. SGD (optional)

// Get historical Market data (candleBars)
MarketAPI.marketControllerGetAssetTimelineInCandleBarFormat(symbol: symbol, timePeriod: timePeriod, quoteSymbol: quoteSymbol) { (response, error) in
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
 **symbol** | **String** | Specify cryptocurrency symbol to return data for. Cannot be combined with &#x60;searchSymbolPart&#x60; | 
 **timePeriod** | **String** | Specify time periods to return data for. accept 1h,1d,7d,30d, 365d or AllTime. 1d is default | [optional] 
 **quoteSymbol** | **String** | Specify quote symbol if needed. This can be fiat currency e.g. SGD | [optional] 

### Return type

[**[AssetMarketPeriodDto]**](AssetMarketPeriodDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **marketControllerGetMarketStat**
```swift
    open class func marketControllerGetMarketStat(symbol: String, completion: @escaping (_ data: AssetStatDataDto?, _ error: Error?) -> Void)
```

Get Market Statistics

Returns market statistics for a single symbol.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let symbol = "symbol_example" // String | Specify cryptocurrency symbol to return data for.

// Get Market Statistics
MarketAPI.marketControllerGetMarketStat(symbol: symbol) { (response, error) in
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
 **symbol** | **String** | Specify cryptocurrency symbol to return data for. | 

### Return type

[**AssetStatDataDto**](AssetStatDataDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **marketControllerGetPriceData**
```swift
    open class func marketControllerGetPriceData(symbols: String? = nil, quoteSymbol: String? = nil, completion: @escaping (_ data: [AssetCurrentPriceDto]?, _ error: Error?) -> Void)
```

Get current price data

Returns current price data.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let symbols = "symbols_example" // String | Specify cryptocurrency symbols to return data for. Cannot be combined with `searchSymbolPart` or `symbol` (optional)
let quoteSymbol = "quoteSymbol_example" // String | Specify quote symbol if needed. This can be fiat currency e.g. SGD (optional)

// Get current price data
MarketAPI.marketControllerGetPriceData(symbols: symbols, quoteSymbol: quoteSymbol) { (response, error) in
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
 **symbols** | **String** | Specify cryptocurrency symbols to return data for. Cannot be combined with &#x60;searchSymbolPart&#x60; or &#x60;symbol&#x60; | [optional] 
 **quoteSymbol** | **String** | Specify quote symbol if needed. This can be fiat currency e.g. SGD | [optional] 

### Return type

[**[AssetCurrentPriceDto]**](AssetCurrentPriceDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **marketNewsControllerGetAssetPosts**
```swift
    open class func marketNewsControllerGetAssetPosts(symbol: String, page: Double, completion: @escaping (_ data: [CryptopanicPostDto]?, _ error: Error?) -> Void)
```

Get Cryptopanic Posts for symbol

Returns Cryptopanic Posts for symbol.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let symbol = "symbol_example" // String | 
let page = 987 // Double | 

// Get Cryptopanic Posts for symbol
MarketAPI.marketNewsControllerGetAssetPosts(symbol: symbol, page: page) { (response, error) in
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
 **symbol** | **String** |  | 
 **page** | **Double** |  | 

### Return type

[**[CryptopanicPostDto]**](CryptopanicPostDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **marketNewsControllerGetPosts**
```swift
    open class func marketNewsControllerGetPosts(page: Double, completion: @escaping (_ data: [CryptopanicPostDto]?, _ error: Error?) -> Void)
```

Get Posts from Cryptopanic

Returns Cryptopanic Posts.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let page = 987 // Double | 

// Get Posts from Cryptopanic
MarketAPI.marketNewsControllerGetPosts(page: page) { (response, error) in
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

### Return type

[**[CryptopanicPostDto]**](CryptopanicPostDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

