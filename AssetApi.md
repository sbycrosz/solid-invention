# AssetAPI

All URIs are relative to *https://backend.arkhon.test.arkhon.digital*

Method | HTTP request | Description
------------- | ------------- | -------------
[**assetControllerCount**](AssetAPI.md#assetcontrollercount) | **POST** /v1/assets/count | Count Assets
[**assetControllerCreate**](AssetAPI.md#assetcontrollercreate) | **POST** /v1/assets | Create new Asset
[**assetControllerCreateAndUpdate**](AssetAPI.md#assetcontrollercreateandupdate) | **POST** /v1/assets/createAndUpdate | Create and update Assets
[**assetControllerCreateBulk**](AssetAPI.md#assetcontrollercreatebulk) | **POST** /v1/assets/bulk | Create new Assets
[**assetControllerDelete**](AssetAPI.md#assetcontrollerdelete) | **DELETE** /v1/assets/{recordId} | Delete an Asset
[**assetControllerFindAll**](AssetAPI.md#assetcontrollerfindall) | **GET** /v1/assets | Get all Assets
[**assetControllerFindOne**](AssetAPI.md#assetcontrollerfindone) | **GET** /v1/assets/{recordId} | Get Asset
[**assetControllerSearch**](AssetAPI.md#assetcontrollersearch) | **POST** /v1/assets/search | Search Assets
[**assetControllerStatistics**](AssetAPI.md#assetcontrollerstatistics) | **GET** /v1/assets/statistics | Asset Statistics
[**assetControllerUpdate**](AssetAPI.md#assetcontrollerupdate) | **PATCH** /v1/assets/{recordId} | Update an Asset
[**assetControllerUpdateBulk**](AssetAPI.md#assetcontrollerupdatebulk) | **PATCH** /v1/assets/bulk | Update multiple Assets


# **assetControllerCount**
```swift
    open class func assetControllerCount(countDto: CountDto, completion: @escaping (_ data: Double?, _ error: Error?) -> Void)
```

Count Assets

Counts matching assets.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let countDto = CountDto(filterOptions: [FilterOptionDto(values: [FilterOptionDto_values_inner()], field: "field_example", _operator: "_operator_example", subFilters: [nil])], returnSoftDeletedEntities: false) // CountDto | 

// Count Assets
AssetAPI.assetControllerCount(countDto: countDto) { (response, error) in
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

# **assetControllerCreate**
```swift
    open class func assetControllerCreate(createAssetDto: CreateAssetDto, completion: @escaping (_ data: AssetDto?, _ error: Error?) -> Void)
```

Create new Asset

Creates and returns a new asset.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let createAssetDto = CreateAssetDto(symbol: "symbol_example", type: "type_example", iconUrl: "iconUrl_example", stable: false, fiat: false, format: "format_example", color: "color_example") // CreateAssetDto | 

// Create new Asset
AssetAPI.assetControllerCreate(createAssetDto: createAssetDto) { (response, error) in
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
 **createAssetDto** | [**CreateAssetDto**](CreateAssetDto.md) |  | 

### Return type

[**AssetDto**](AssetDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **assetControllerCreateAndUpdate**
```swift
    open class func assetControllerCreateAndUpdate(createAndUpdateAssetDto: [CreateAndUpdateAssetDto], completion: @escaping (_ data: [AssetDto]?, _ error: Error?) -> Void)
```

Create and update Assets

Creates or updates and returns multiple assets.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let createAndUpdateAssetDto = [CreateAndUpdateAssetDto(recordId: 123, creationDt: Date(), updatedOn: Date(), deletionDt: Date(), symbol: "symbol_example", type: "type_example", iconUrl: "iconUrl_example", stable: false, fiat: false, format: "format_example", color: "color_example")] // [CreateAndUpdateAssetDto] | 

// Create and update Assets
AssetAPI.assetControllerCreateAndUpdate(createAndUpdateAssetDto: createAndUpdateAssetDto) { (response, error) in
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
 **createAndUpdateAssetDto** | [**[CreateAndUpdateAssetDto]**](CreateAndUpdateAssetDto.md) |  | 

### Return type

[**[AssetDto]**](AssetDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **assetControllerCreateBulk**
```swift
    open class func assetControllerCreateBulk(createAssetDto: [CreateAssetDto], completion: @escaping (_ data: [AssetDto]?, _ error: Error?) -> Void)
```

Create new Assets

Creates and returns multiple new assets.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let createAssetDto = [CreateAssetDto(symbol: "symbol_example", type: "type_example", iconUrl: "iconUrl_example", stable: false, fiat: false, format: "format_example", color: "color_example")] // [CreateAssetDto] | 

// Create new Assets
AssetAPI.assetControllerCreateBulk(createAssetDto: createAssetDto) { (response, error) in
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
 **createAssetDto** | [**[CreateAssetDto]**](CreateAssetDto.md) |  | 

### Return type

[**[AssetDto]**](AssetDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **assetControllerDelete**
```swift
    open class func assetControllerDelete(recordId: Double, completion: @escaping (_ data: String?, _ error: Error?) -> Void)
```

Delete an Asset

UNSUPPORTED; Deleting assets is not possible. Once an asset has been created it could have been used in various transactions, and deleting it after the fact would not be safe. Please contact Arkhon support if you wish to delete an asset.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let recordId = 987 // Double | 

// Delete an Asset
AssetAPI.assetControllerDelete(recordId: recordId) { (response, error) in
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

# **assetControllerFindAll**
```swift
    open class func assetControllerFindAll(page: Double, pageSize: Double, completion: @escaping (_ data: [AssetDto]?, _ error: Error?) -> Void)
```

Get all Assets

Returns all supported assets.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let page = 987 // Double | 
let pageSize = 987 // Double | 

// Get all Assets
AssetAPI.assetControllerFindAll(page: page, pageSize: pageSize) { (response, error) in
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

[**[AssetDto]**](AssetDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **assetControllerFindOne**
```swift
    open class func assetControllerFindOne(recordId: Double, completion: @escaping (_ data: AssetDto?, _ error: Error?) -> Void)
```

Get Asset

Returns single asset.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let recordId = 987 // Double | 

// Get Asset
AssetAPI.assetControllerFindOne(recordId: recordId) { (response, error) in
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

[**AssetDto**](AssetDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **assetControllerSearch**
```swift
    open class func assetControllerSearch(searchDto: SearchDto, completion: @escaping (_ data: [AssetDto]?, _ error: Error?) -> Void)
```

Search Assets

Returns all matching assets.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let searchDto = SearchDto(orderOption: [OrderOption(field: "field_example", direction: "direction_example")], pageSize: 123, page: 123, enrichments: ["enrichments_example"], filterOptions: [FilterOptionDto(values: [FilterOptionDto_values_inner()], field: "field_example", _operator: "_operator_example", subFilters: [nil])], returnSoftDeletedEntities: false) // SearchDto | 

// Search Assets
AssetAPI.assetControllerSearch(searchDto: searchDto) { (response, error) in
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

[**[AssetDto]**](AssetDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **assetControllerStatistics**
```swift
    open class func assetControllerStatistics(stats: [String], completion: @escaping (_ data: AssetDto?, _ error: Error?) -> Void)
```

Asset Statistics

Not supported.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let stats = ["inner_example"] // [String] | 

// Asset Statistics
AssetAPI.assetControllerStatistics(stats: stats) { (response, error) in
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

[**AssetDto**](AssetDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **assetControllerUpdate**
```swift
    open class func assetControllerUpdate(recordId: Double, updateAssetDto: UpdateAssetDto, completion: @escaping (_ data: AssetDto?, _ error: Error?) -> Void)
```

Update an Asset

Updates and returns a single asset.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let recordId = 987 // Double | 
let updateAssetDto = UpdateAssetDto(recordId: 123, symbol: "symbol_example", type: "type_example", iconUrl: "iconUrl_example", stable: false, fiat: false, format: "format_example", color: "color_example") // UpdateAssetDto | 

// Update an Asset
AssetAPI.assetControllerUpdate(recordId: recordId, updateAssetDto: updateAssetDto) { (response, error) in
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
 **updateAssetDto** | [**UpdateAssetDto**](UpdateAssetDto.md) |  | 

### Return type

[**AssetDto**](AssetDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **assetControllerUpdateBulk**
```swift
    open class func assetControllerUpdateBulk(updateAssetDto: [UpdateAssetDto], completion: @escaping (_ data: [AssetDto]?, _ error: Error?) -> Void)
```

Update multiple Assets

Updates and returns multiple assets.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let updateAssetDto = [UpdateAssetDto(recordId: 123, symbol: "symbol_example", type: "type_example", iconUrl: "iconUrl_example", stable: false, fiat: false, format: "format_example", color: "color_example")] // [UpdateAssetDto] | 

// Update multiple Assets
AssetAPI.assetControllerUpdateBulk(updateAssetDto: updateAssetDto) { (response, error) in
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
 **updateAssetDto** | [**[UpdateAssetDto]**](UpdateAssetDto.md) |  | 

### Return type

[**[AssetDto]**](AssetDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

