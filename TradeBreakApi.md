# TradeBreakAPI

All URIs are relative to *https://backend.arkhon.test.arkhon.digital*

Method | HTTP request | Description
------------- | ------------- | -------------
[**tradeBreakControllerCount**](TradeBreakAPI.md#tradebreakcontrollercount) | **POST** /v1/tradeBreaks/count | Count TradeBreaks
[**tradeBreakControllerCreate**](TradeBreakAPI.md#tradebreakcontrollercreate) | **POST** /v1/tradeBreaks | Create TradeBreak
[**tradeBreakControllerCreateBulk**](TradeBreakAPI.md#tradebreakcontrollercreatebulk) | **POST** /v1/tradeBreaks/bulk | Create multiple TradeBreaks
[**tradeBreakControllerDelete**](TradeBreakAPI.md#tradebreakcontrollerdelete) | **DELETE** /v1/tradeBreaks/{recordId} | Delete TradeBreak
[**tradeBreakControllerFindAll**](TradeBreakAPI.md#tradebreakcontrollerfindall) | **GET** /v1/tradeBreaks | Get all TradeBreaks
[**tradeBreakControllerFindOne**](TradeBreakAPI.md#tradebreakcontrollerfindone) | **GET** /v1/tradeBreaks/{recordId} | Get single TradeBreak
[**tradeBreakControllerSearch**](TradeBreakAPI.md#tradebreakcontrollersearch) | **POST** /v1/tradeBreaks/search | Search TradeBreaks
[**tradeBreakControllerStatistics**](TradeBreakAPI.md#tradebreakcontrollerstatistics) | **GET** /v1/tradeBreaks/statistics | Get Statistics across all TradeBreaks
[**tradeBreakControllerUpdate**](TradeBreakAPI.md#tradebreakcontrollerupdate) | **PATCH** /v1/tradeBreaks/{recordId} | Update single TradeBreak
[**tradeBreakControllerUpdateBulk**](TradeBreakAPI.md#tradebreakcontrollerupdatebulk) | **PATCH** /v1/tradeBreaks/bulk | Update multiple TradeBreaks


# **tradeBreakControllerCount**
```swift
    open class func tradeBreakControllerCount(countDto: CountDto, completion: @escaping (_ data: Double?, _ error: Error?) -> Void)
```

Count TradeBreaks

Counts matching trade breaks to which the logged in user has access.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let countDto = CountDto(filterOptions: [FilterOptionDto(values: [FilterOptionDto_values_inner()], field: "field_example", _operator: "_operator_example", subFilters: [nil])], returnSoftDeletedEntities: false) // CountDto | 

// Count TradeBreaks
TradeBreakAPI.tradeBreakControllerCount(countDto: countDto) { (response, error) in
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

# **tradeBreakControllerCreate**
```swift
    open class func tradeBreakControllerCreate(createTradeBreakDto: CreateTradeBreakDto, completion: @escaping (_ data: TradeBreakDto?, _ error: Error?) -> Void)
```

Create TradeBreak

Creates and returns a trade break.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let createTradeBreakDto = CreateTradeBreakDto(userId: 123, quantity: "quantity_example", platformId: 123, type: "type_example", currency: "currency_example", reason: "reason_example", version: 123, comment: "comment_example") // CreateTradeBreakDto | 

// Create TradeBreak
TradeBreakAPI.tradeBreakControllerCreate(createTradeBreakDto: createTradeBreakDto) { (response, error) in
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
 **createTradeBreakDto** | [**CreateTradeBreakDto**](CreateTradeBreakDto.md) |  | 

### Return type

[**TradeBreakDto**](TradeBreakDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **tradeBreakControllerCreateBulk**
```swift
    open class func tradeBreakControllerCreateBulk(createTradeBreakDto: [CreateTradeBreakDto], completion: @escaping (_ data: [TradeBreakDto]?, _ error: Error?) -> Void)
```

Create multiple TradeBreaks

Creates and returns multiple trade breaks.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let createTradeBreakDto = [CreateTradeBreakDto(userId: 123, quantity: "quantity_example", platformId: 123, type: "type_example", currency: "currency_example", reason: "reason_example", version: 123, comment: "comment_example")] // [CreateTradeBreakDto] | 

// Create multiple TradeBreaks
TradeBreakAPI.tradeBreakControllerCreateBulk(createTradeBreakDto: createTradeBreakDto) { (response, error) in
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
 **createTradeBreakDto** | [**[CreateTradeBreakDto]**](CreateTradeBreakDto.md) |  | 

### Return type

[**[TradeBreakDto]**](TradeBreakDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **tradeBreakControllerDelete**
```swift
    open class func tradeBreakControllerDelete(recordId: Double, completion: @escaping (_ data: String?, _ error: Error?) -> Void)
```

Delete TradeBreak

Deletes a trade break.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let recordId = 987 // Double | 

// Delete TradeBreak
TradeBreakAPI.tradeBreakControllerDelete(recordId: recordId) { (response, error) in
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

# **tradeBreakControllerFindAll**
```swift
    open class func tradeBreakControllerFindAll(page: Double, pageSize: Double, completion: @escaping (_ data: [TradeBreakDto]?, _ error: Error?) -> Void)
```

Get all TradeBreaks

Returns all trade breaks to which the logged in user has access.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let page = 987 // Double | 
let pageSize = 987 // Double | 

// Get all TradeBreaks
TradeBreakAPI.tradeBreakControllerFindAll(page: page, pageSize: pageSize) { (response, error) in
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

[**[TradeBreakDto]**](TradeBreakDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **tradeBreakControllerFindOne**
```swift
    open class func tradeBreakControllerFindOne(recordId: Double, completion: @escaping (_ data: TradeBreakDto?, _ error: Error?) -> Void)
```

Get single TradeBreak

Returns single trade break if the logged in user has access.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let recordId = 987 // Double | 

// Get single TradeBreak
TradeBreakAPI.tradeBreakControllerFindOne(recordId: recordId) { (response, error) in
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

[**TradeBreakDto**](TradeBreakDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **tradeBreakControllerSearch**
```swift
    open class func tradeBreakControllerSearch(searchDto: SearchDto, completion: @escaping (_ data: [TradeBreakDto]?, _ error: Error?) -> Void)
```

Search TradeBreaks

Returns matching trade breaks to which the logged in user has access.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let searchDto = SearchDto(orderOption: [OrderOption(field: "field_example", direction: "direction_example")], pageSize: 123, page: 123, enrichments: ["enrichments_example"], filterOptions: [FilterOptionDto(values: [FilterOptionDto_values_inner()], field: "field_example", _operator: "_operator_example", subFilters: [nil])], returnSoftDeletedEntities: false) // SearchDto | 

// Search TradeBreaks
TradeBreakAPI.tradeBreakControllerSearch(searchDto: searchDto) { (response, error) in
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

[**[TradeBreakDto]**](TradeBreakDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **tradeBreakControllerStatistics**
```swift
    open class func tradeBreakControllerStatistics(stats: [String], completion: @escaping (_ data: TradeBreakDto?, _ error: Error?) -> Void)
```

Get Statistics across all TradeBreaks

Returns desired statistic(s) across trade breaks.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let stats = ["inner_example"] // [String] | Specifies statistics to be evaluated across trade breaks.

// Get Statistics across all TradeBreaks
TradeBreakAPI.tradeBreakControllerStatistics(stats: stats) { (response, error) in
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
 **stats** | [**[String]**](String.md) | Specifies statistics to be evaluated across trade breaks. | 

### Return type

[**TradeBreakDto**](TradeBreakDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **tradeBreakControllerUpdate**
```swift
    open class func tradeBreakControllerUpdate(recordId: Double, updateTradeBreakDto: UpdateTradeBreakDto, completion: @escaping (_ data: TradeBreakDto?, _ error: Error?) -> Void)
```

Update single TradeBreak

Updates and returns single trade break.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let recordId = 987 // Double | 
let updateTradeBreakDto = UpdateTradeBreakDto(recordId: 123, userId: 123, quantity: "quantity_example", platformId: 123, version: 123, type: "type_example", currency: "currency_example", reason: "reason_example", comment: "comment_example") // UpdateTradeBreakDto | 

// Update single TradeBreak
TradeBreakAPI.tradeBreakControllerUpdate(recordId: recordId, updateTradeBreakDto: updateTradeBreakDto) { (response, error) in
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
 **updateTradeBreakDto** | [**UpdateTradeBreakDto**](UpdateTradeBreakDto.md) |  | 

### Return type

[**TradeBreakDto**](TradeBreakDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **tradeBreakControllerUpdateBulk**
```swift
    open class func tradeBreakControllerUpdateBulk(updateTradeBreakDto: [UpdateTradeBreakDto], completion: @escaping (_ data: [TradeBreakDto]?, _ error: Error?) -> Void)
```

Update multiple TradeBreaks

Updates and returns multiple trade breaks.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let updateTradeBreakDto = [UpdateTradeBreakDto(recordId: 123, userId: 123, quantity: "quantity_example", platformId: 123, version: 123, type: "type_example", currency: "currency_example", reason: "reason_example", comment: "comment_example")] // [UpdateTradeBreakDto] | 

// Update multiple TradeBreaks
TradeBreakAPI.tradeBreakControllerUpdateBulk(updateTradeBreakDto: updateTradeBreakDto) { (response, error) in
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
 **updateTradeBreakDto** | [**[UpdateTradeBreakDto]**](UpdateTradeBreakDto.md) |  | 

### Return type

[**[TradeBreakDto]**](TradeBreakDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

