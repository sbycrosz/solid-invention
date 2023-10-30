# OrderAPI

All URIs are relative to *https://backend.arkhon.test.arkhon.digital*

Method | HTTP request | Description
------------- | ------------- | -------------
[**orderControllerBulkDelete**](OrderAPI.md#ordercontrollerbulkdelete) | **DELETE** /v1/orders/bulkDelete | Delete multiple Orders
[**orderControllerCount**](OrderAPI.md#ordercontrollercount) | **POST** /v1/orders/count | Count Orders
[**orderControllerCreate**](OrderAPI.md#ordercontrollercreate) | **POST** /v1/orders | Create single Order
[**orderControllerCreateBulk**](OrderAPI.md#ordercontrollercreatebulk) | **POST** /v1/orders/bulk | Create multiple Orders
[**orderControllerDelete**](OrderAPI.md#ordercontrollerdelete) | **DELETE** /v1/orders/{recordId} | Delete single Order
[**orderControllerFindAll**](OrderAPI.md#ordercontrollerfindall) | **GET** /v1/orders | Get all Orders
[**orderControllerFindOne**](OrderAPI.md#ordercontrollerfindone) | **GET** /v1/orders/{recordId} | Get single Order
[**orderControllerSearch**](OrderAPI.md#ordercontrollersearch) | **POST** /v1/orders/search | Search all Orders
[**orderControllerSearchWithAggregates**](OrderAPI.md#ordercontrollersearchwithaggregates) | **POST** /v1/orders/searchWithAggregates | Search all Orders with Aggregates
[**orderControllerStatistics**](OrderAPI.md#ordercontrollerstatistics) | **GET** /v1/orders/statistics | Get Statistics across all Orders
[**orderControllerUpdate**](OrderAPI.md#ordercontrollerupdate) | **PATCH** /v1/orders/{recordId} | Update single Order
[**orderControllerUpdateBulk**](OrderAPI.md#ordercontrollerupdatebulk) | **PATCH** /v1/orders/bulk | Update multiple Orders


# **orderControllerBulkDelete**
```swift
    open class func orderControllerBulkDelete(deleteOrderDto: DeleteOrderDto, completion: @escaping (_ data: String?, _ error: Error?) -> Void)
```

Delete multiple Orders

Deletes multiple orders.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let deleteOrderDto = DeleteOrderDto(reason: "reason_example", recordIds: [123]) // DeleteOrderDto | 

// Delete multiple Orders
OrderAPI.orderControllerBulkDelete(deleteOrderDto: deleteOrderDto) { (response, error) in
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
 **deleteOrderDto** | [**DeleteOrderDto**](DeleteOrderDto.md) |  | 

### Return type

**String**

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **orderControllerCount**
```swift
    open class func orderControllerCount(countDto: CountDto, completion: @escaping (_ data: Double?, _ error: Error?) -> Void)
```

Count Orders

Counts all matching orders.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let countDto = CountDto(filterOptions: [FilterOptionDto(values: [FilterOptionDto_values_inner()], field: "field_example", _operator: "_operator_example", subFilters: [nil])], returnSoftDeletedEntities: false) // CountDto | 

// Count Orders
OrderAPI.orderControllerCount(countDto: countDto) { (response, error) in
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

# **orderControllerCreate**
```swift
    open class func orderControllerCreate(createOrderDto: CreateOrderDto, completion: @escaping (_ data: OrderDto?, _ error: Error?) -> Void)
```

Create single Order

Creates and returns single order.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let createOrderDto = CreateOrderDto(portfolioId: 123, userId: 123, executedBy: 123, pricePerUnit: "pricePerUnit_example", lpPricePerUnit: "lpPricePerUnit_example", stopPrice: "stopPrice_example", requestedQuantity: "requestedQuantity_example", filledQuantity: "filledQuantity_example", platformId: 123, platformFee: "platformFee_example", arkhonFeePercentage: "arkhonFeePercentage_example", arkhonSpreadPercentage: "arkhonSpreadPercentage_example", tierId: 123, baseToken: "baseToken_example", quoteToken: "quoteToken_example", tradedToken: "tradedToken_example", side: "side_example", strategy: "strategy_example", type: "type_example", platformRefId: "platformRefId_example", status: "status_example", version: 123, startTime: Date(), endTime: Date(), clientRefId: "clientRefId_example", platformFeeCurrency: "platformFeeCurrency_example", arkhonFeeCurrency: "arkhonFeeCurrency_example", feeStatus: "feeStatus_example", feeComment: "feeComment_example", comment: "comment_example", settlementId: 123) // CreateOrderDto | 

// Create single Order
OrderAPI.orderControllerCreate(createOrderDto: createOrderDto) { (response, error) in
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
 **createOrderDto** | [**CreateOrderDto**](CreateOrderDto.md) |  | 

### Return type

[**OrderDto**](OrderDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **orderControllerCreateBulk**
```swift
    open class func orderControllerCreateBulk(createOrderDto: [CreateOrderDto], completion: @escaping (_ data: [OrderDto]?, _ error: Error?) -> Void)
```

Create multiple Orders

Creates and returns multiple orders.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let createOrderDto = [CreateOrderDto(portfolioId: 123, userId: 123, executedBy: 123, pricePerUnit: "pricePerUnit_example", lpPricePerUnit: "lpPricePerUnit_example", stopPrice: "stopPrice_example", requestedQuantity: "requestedQuantity_example", filledQuantity: "filledQuantity_example", platformId: 123, platformFee: "platformFee_example", arkhonFeePercentage: "arkhonFeePercentage_example", arkhonSpreadPercentage: "arkhonSpreadPercentage_example", tierId: 123, baseToken: "baseToken_example", quoteToken: "quoteToken_example", tradedToken: "tradedToken_example", side: "side_example", strategy: "strategy_example", type: "type_example", platformRefId: "platformRefId_example", status: "status_example", version: 123, startTime: Date(), endTime: Date(), clientRefId: "clientRefId_example", platformFeeCurrency: "platformFeeCurrency_example", arkhonFeeCurrency: "arkhonFeeCurrency_example", feeStatus: "feeStatus_example", feeComment: "feeComment_example", comment: "comment_example", settlementId: 123)] // [CreateOrderDto] | 

// Create multiple Orders
OrderAPI.orderControllerCreateBulk(createOrderDto: createOrderDto) { (response, error) in
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
 **createOrderDto** | [**[CreateOrderDto]**](CreateOrderDto.md) |  | 

### Return type

[**[OrderDto]**](OrderDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **orderControllerDelete**
```swift
    open class func orderControllerDelete(recordId: Double, deleteOrderDto: DeleteOrderDto, completion: @escaping (_ data: String?, _ error: Error?) -> Void)
```

Delete single Order

Deletes single order.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let recordId = 987 // Double | 
let deleteOrderDto = DeleteOrderDto(reason: "reason_example", recordIds: [123]) // DeleteOrderDto | 

// Delete single Order
OrderAPI.orderControllerDelete(recordId: recordId, deleteOrderDto: deleteOrderDto) { (response, error) in
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
 **deleteOrderDto** | [**DeleteOrderDto**](DeleteOrderDto.md) |  | 

### Return type

**String**

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **orderControllerFindAll**
```swift
    open class func orderControllerFindAll(page: Double, pageSize: Double, completion: @escaping (_ data: [OrderDto]?, _ error: Error?) -> Void)
```

Get all Orders

Returns all orders to which the logged in user has access.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let page = 987 // Double | 
let pageSize = 987 // Double | 

// Get all Orders
OrderAPI.orderControllerFindAll(page: page, pageSize: pageSize) { (response, error) in
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

[**[OrderDto]**](OrderDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **orderControllerFindOne**
```swift
    open class func orderControllerFindOne(recordId: Double, withPortfolio: Bool? = nil, completion: @escaping (_ data: OrderDto?, _ error: Error?) -> Void)
```

Get single Order

Returns single order if which the logged in user has access.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let recordId = 987 // Double | 
let withPortfolio = true // Bool | Return order with portfolio object attached. (optional)

// Get single Order
OrderAPI.orderControllerFindOne(recordId: recordId, withPortfolio: withPortfolio) { (response, error) in
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
 **withPortfolio** | **Bool** | Return order with portfolio object attached. | [optional] 

### Return type

[**OrderDto**](OrderDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **orderControllerSearch**
```swift
    open class func orderControllerSearch(searchDto: SearchDto, completion: @escaping (_ data: [OrderDto]?, _ error: Error?) -> Void)
```

Search all Orders

Returns all matching orders to which the logged in user has access.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let searchDto = SearchDto(orderOption: [OrderOption(field: "field_example", direction: "direction_example")], pageSize: 123, page: 123, enrichments: ["enrichments_example"], filterOptions: [FilterOptionDto(values: [FilterOptionDto_values_inner()], field: "field_example", _operator: "_operator_example", subFilters: [nil])], returnSoftDeletedEntities: false) // SearchDto | 

// Search all Orders
OrderAPI.orderControllerSearch(searchDto: searchDto) { (response, error) in
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

[**[OrderDto]**](OrderDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **orderControllerSearchWithAggregates**
```swift
    open class func orderControllerSearchWithAggregates(aggregates: [String], searchDto: SearchDto, completion: @escaping (_ data: OrdersWithAggregate?, _ error: Error?) -> Void)
```

Search all Orders with Aggregates

Returns all matching orders plus computes aggregates on top.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let aggregates = ["inner_example"] // [String] | 
let searchDto = SearchDto(orderOption: [OrderOption(field: "field_example", direction: "direction_example")], pageSize: 123, page: 123, enrichments: ["enrichments_example"], filterOptions: [FilterOptionDto(values: [FilterOptionDto_values_inner()], field: "field_example", _operator: "_operator_example", subFilters: [nil])], returnSoftDeletedEntities: false) // SearchDto | 

// Search all Orders with Aggregates
OrderAPI.orderControllerSearchWithAggregates(aggregates: aggregates, searchDto: searchDto) { (response, error) in
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
 **searchDto** | [**SearchDto**](SearchDto.md) |  | 

### Return type

[**OrdersWithAggregate**](OrdersWithAggregate.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **orderControllerStatistics**
```swift
    open class func orderControllerStatistics(stats: [String], completion: @escaping (_ data: OrderDto?, _ error: Error?) -> Void)
```

Get Statistics across all Orders

Returns desired statistic(s) across orders.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let stats = ["inner_example"] // [String] | Specifies statistics to be evaluated across orders.

// Get Statistics across all Orders
OrderAPI.orderControllerStatistics(stats: stats) { (response, error) in
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
 **stats** | [**[String]**](String.md) | Specifies statistics to be evaluated across orders. | 

### Return type

[**OrderDto**](OrderDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **orderControllerUpdate**
```swift
    open class func orderControllerUpdate(recordId: Double, updateOrderDto: UpdateOrderDto, completion: @escaping (_ data: OrderDto?, _ error: Error?) -> Void)
```

Update single Order

Updates and returns single order.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let recordId = 987 // Double | 
let updateOrderDto = UpdateOrderDto(recordId: 123, portfolioId: 123, userId: 123, executedBy: 123, pricePerUnit: "pricePerUnit_example", lpPricePerUnit: "lpPricePerUnit_example", stopPrice: "stopPrice_example", requestedQuantity: "requestedQuantity_example", filledQuantity: "filledQuantity_example", platformId: 123, platformFee: "platformFee_example", arkhonFeePercentage: "arkhonFeePercentage_example", arkhonSpreadPercentage: "arkhonSpreadPercentage_example", tierId: 123, version: 123, baseToken: "baseToken_example", quoteToken: "quoteToken_example", tradedToken: "tradedToken_example", side: "side_example", startTime: Date(), endTime: Date(), strategy: "strategy_example", type: "type_example", platformRefId: "platformRefId_example", clientRefId: "clientRefId_example", platformFeeCurrency: "platformFeeCurrency_example", status: "status_example", arkhonFeeCurrency: "arkhonFeeCurrency_example", feeStatus: "feeStatus_example", feeComment: "feeComment_example", comment: "comment_example", settlementId: 123) // UpdateOrderDto | 

// Update single Order
OrderAPI.orderControllerUpdate(recordId: recordId, updateOrderDto: updateOrderDto) { (response, error) in
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
 **updateOrderDto** | [**UpdateOrderDto**](UpdateOrderDto.md) |  | 

### Return type

[**OrderDto**](OrderDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **orderControllerUpdateBulk**
```swift
    open class func orderControllerUpdateBulk(updateOrderDto: [UpdateOrderDto], completion: @escaping (_ data: [OrderDto]?, _ error: Error?) -> Void)
```

Update multiple Orders

Updates and returns multiple orders.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let updateOrderDto = [UpdateOrderDto(recordId: 123, portfolioId: 123, userId: 123, executedBy: 123, pricePerUnit: "pricePerUnit_example", lpPricePerUnit: "lpPricePerUnit_example", stopPrice: "stopPrice_example", requestedQuantity: "requestedQuantity_example", filledQuantity: "filledQuantity_example", platformId: 123, platformFee: "platformFee_example", arkhonFeePercentage: "arkhonFeePercentage_example", arkhonSpreadPercentage: "arkhonSpreadPercentage_example", tierId: 123, version: 123, baseToken: "baseToken_example", quoteToken: "quoteToken_example", tradedToken: "tradedToken_example", side: "side_example", startTime: Date(), endTime: Date(), strategy: "strategy_example", type: "type_example", platformRefId: "platformRefId_example", clientRefId: "clientRefId_example", platformFeeCurrency: "platformFeeCurrency_example", status: "status_example", arkhonFeeCurrency: "arkhonFeeCurrency_example", feeStatus: "feeStatus_example", feeComment: "feeComment_example", comment: "comment_example", settlementId: 123)] // [UpdateOrderDto] | 

// Update multiple Orders
OrderAPI.orderControllerUpdateBulk(updateOrderDto: updateOrderDto) { (response, error) in
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
 **updateOrderDto** | [**[UpdateOrderDto]**](UpdateOrderDto.md) |  | 

### Return type

[**[OrderDto]**](OrderDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

