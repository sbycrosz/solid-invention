# SpreadAPI

All URIs are relative to *https://backend.arkhon.test.arkhon.digital*

Method | HTTP request | Description
------------- | ------------- | -------------
[**spreadControllerCount**](SpreadAPI.md#spreadcontrollercount) | **POST** /v1/spreads/count | Count Spreads
[**spreadControllerCreate**](SpreadAPI.md#spreadcontrollercreate) | **POST** /v1/spreads | Create new Spread
[**spreadControllerCreateAndUpdate**](SpreadAPI.md#spreadcontrollercreateandupdate) | **POST** /v1/spreads/createAndUpdate | Create and update Spreads
[**spreadControllerCreateBulk**](SpreadAPI.md#spreadcontrollercreatebulk) | **POST** /v1/spreads/bulk | Create new Spreads
[**spreadControllerDelete**](SpreadAPI.md#spreadcontrollerdelete) | **DELETE** /v1/spreads/{recordId} | Delete a Spread
[**spreadControllerFindAll**](SpreadAPI.md#spreadcontrollerfindall) | **GET** /v1/spreads | Get all Spreads
[**spreadControllerFindOne**](SpreadAPI.md#spreadcontrollerfindone) | **GET** /v1/spreads/{recordId} | Get single Spread
[**spreadControllerSearch**](SpreadAPI.md#spreadcontrollersearch) | **POST** /v1/spreads/search | Search Spreads
[**spreadControllerStatistics**](SpreadAPI.md#spreadcontrollerstatistics) | **GET** /v1/spreads/statistics | Spread Statistics
[**spreadControllerUpdate**](SpreadAPI.md#spreadcontrollerupdate) | **PATCH** /v1/spreads/{recordId} | Update spreads
[**spreadControllerUpdateBulk**](SpreadAPI.md#spreadcontrollerupdatebulk) | **PATCH** /v1/spreads/bulk | Update multiple Spreads


# **spreadControllerCount**
```swift
    open class func spreadControllerCount(countDto: CountDto, completion: @escaping (_ data: Double?, _ error: Error?) -> Void)
```

Count Spreads

Counts matching spreads.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let countDto = CountDto(filterOptions: [FilterOptionDto(values: [FilterOptionDto_values_inner()], field: "field_example", _operator: "_operator_example", subFilters: [nil])], returnSoftDeletedEntities: false) // CountDto | 

// Count Spreads
SpreadAPI.spreadControllerCount(countDto: countDto) { (response, error) in
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

# **spreadControllerCreate**
```swift
    open class func spreadControllerCreate(spreadDto: SpreadDto, completion: @escaping (_ data: SpreadDto?, _ error: Error?) -> Void)
```

Create new Spread

Creates and returns a new spread.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let spreadDto = SpreadDto(recordId: 123, spreadValue: "spreadValue_example", validFrom: Date(), validUntil: Date(), updatedOn: Date(), deletionDt: Date(), creationDt: Date()) // SpreadDto | 

// Create new Spread
SpreadAPI.spreadControllerCreate(spreadDto: spreadDto) { (response, error) in
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
 **spreadDto** | [**SpreadDto**](SpreadDto.md) |  | 

### Return type

[**SpreadDto**](SpreadDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **spreadControllerCreateAndUpdate**
```swift
    open class func spreadControllerCreateAndUpdate(createAndUpdateSpreadDto: [CreateAndUpdateSpreadDto], completion: @escaping (_ data: [SpreadDto]?, _ error: Error?) -> Void)
```

Create and update Spreads

Creates or updates and returns multiple spreads.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let createAndUpdateSpreadDto = [CreateAndUpdateSpreadDto(recordId: 123, spreadValue: "spreadValue_example", creationDt: Date(), updatedOn: Date(), deletionDt: Date(), validFrom: Date(), validUntil: Date())] // [CreateAndUpdateSpreadDto] | 

// Create and update Spreads
SpreadAPI.spreadControllerCreateAndUpdate(createAndUpdateSpreadDto: createAndUpdateSpreadDto) { (response, error) in
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
 **createAndUpdateSpreadDto** | [**[CreateAndUpdateSpreadDto]**](CreateAndUpdateSpreadDto.md) |  | 

### Return type

[**[SpreadDto]**](SpreadDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **spreadControllerCreateBulk**
```swift
    open class func spreadControllerCreateBulk(spreadDto: [SpreadDto], completion: @escaping (_ data: [SpreadDto]?, _ error: Error?) -> Void)
```

Create new Spreads

Creates and returns multiple new spreads.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let spreadDto = [SpreadDto(recordId: 123, spreadValue: "spreadValue_example", validFrom: Date(), validUntil: Date(), updatedOn: Date(), deletionDt: Date(), creationDt: Date())] // [SpreadDto] | 

// Create new Spreads
SpreadAPI.spreadControllerCreateBulk(spreadDto: spreadDto) { (response, error) in
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
 **spreadDto** | [**[SpreadDto]**](SpreadDto.md) |  | 

### Return type

[**[SpreadDto]**](SpreadDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **spreadControllerDelete**
```swift
    open class func spreadControllerDelete(recordId: Double, completion: @escaping (_ data: String?, _ error: Error?) -> Void)
```

Delete a Spread

UNSUPPORTED; Deleting spreads is not possible. Once an spread has been created it could have been used in various transactions, and deleting it after the fact would not be safe. You can update a spread to no longer be applicable, which we suggest to do instead of deleting it. Please contact Arkhon support if you wish to delete a spread.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let recordId = 987 // Double | 

// Delete a Spread
SpreadAPI.spreadControllerDelete(recordId: recordId) { (response, error) in
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

# **spreadControllerFindAll**
```swift
    open class func spreadControllerFindAll(page: Double, pageSize: Double, completion: @escaping (_ data: [SpreadDto]?, _ error: Error?) -> Void)
```

Get all Spreads

Returns all spreads.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let page = 987 // Double | 
let pageSize = 987 // Double | 

// Get all Spreads
SpreadAPI.spreadControllerFindAll(page: page, pageSize: pageSize) { (response, error) in
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

[**[SpreadDto]**](SpreadDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **spreadControllerFindOne**
```swift
    open class func spreadControllerFindOne(recordId: Double, completion: @escaping (_ data: SpreadDto?, _ error: Error?) -> Void)
```

Get single Spread

Returns single spread.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let recordId = 987 // Double | 

// Get single Spread
SpreadAPI.spreadControllerFindOne(recordId: recordId) { (response, error) in
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

[**SpreadDto**](SpreadDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **spreadControllerSearch**
```swift
    open class func spreadControllerSearch(searchDto: SearchDto, completion: @escaping (_ data: [SpreadDto]?, _ error: Error?) -> Void)
```

Search Spreads

Returns matching spreads.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let searchDto = SearchDto(orderOption: [OrderOption(field: "field_example", direction: "direction_example")], pageSize: 123, page: 123, enrichments: ["enrichments_example"], filterOptions: [FilterOptionDto(values: [FilterOptionDto_values_inner()], field: "field_example", _operator: "_operator_example", subFilters: [nil])], returnSoftDeletedEntities: false) // SearchDto | 

// Search Spreads
SpreadAPI.spreadControllerSearch(searchDto: searchDto) { (response, error) in
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

[**[SpreadDto]**](SpreadDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **spreadControllerStatistics**
```swift
    open class func spreadControllerStatistics(stats: [String], completion: @escaping (_ data: SpreadDto?, _ error: Error?) -> Void)
```

Spread Statistics

Not supported.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let stats = ["inner_example"] // [String] | 

// Spread Statistics
SpreadAPI.spreadControllerStatistics(stats: stats) { (response, error) in
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

[**SpreadDto**](SpreadDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **spreadControllerUpdate**
```swift
    open class func spreadControllerUpdate(recordId: Double, updateSpreadDto: UpdateSpreadDto, completion: @escaping (_ data: SpreadDto?, _ error: Error?) -> Void)
```

Update spreads

Updates and returns a single spread.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let recordId = 987 // Double | 
let updateSpreadDto = UpdateSpreadDto(recordId: 123, spreadValue: "spreadValue_example", validFrom: Date(), validUntil: Date()) // UpdateSpreadDto | 

// Update spreads
SpreadAPI.spreadControllerUpdate(recordId: recordId, updateSpreadDto: updateSpreadDto) { (response, error) in
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
 **updateSpreadDto** | [**UpdateSpreadDto**](UpdateSpreadDto.md) |  | 

### Return type

[**SpreadDto**](SpreadDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **spreadControllerUpdateBulk**
```swift
    open class func spreadControllerUpdateBulk(spreadDto: [SpreadDto], completion: @escaping (_ data: [SpreadDto]?, _ error: Error?) -> Void)
```

Update multiple Spreads

Updates and returns multiple spreads.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let spreadDto = [SpreadDto(recordId: 123, spreadValue: "spreadValue_example", validFrom: Date(), validUntil: Date(), updatedOn: Date(), deletionDt: Date(), creationDt: Date())] // [SpreadDto] | 

// Update multiple Spreads
SpreadAPI.spreadControllerUpdateBulk(spreadDto: spreadDto) { (response, error) in
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
 **spreadDto** | [**[SpreadDto]**](SpreadDto.md) |  | 

### Return type

[**[SpreadDto]**](SpreadDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

