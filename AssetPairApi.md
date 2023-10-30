# AssetPairAPI

All URIs are relative to *https://backend.arkhon.test.arkhon.digital*

Method | HTTP request | Description
------------- | ------------- | -------------
[**assetPairControllerCount**](AssetPairAPI.md#assetpaircontrollercount) | **POST** /v1/assetPair/count | Count Asset Pairs
[**assetPairControllerCreate**](AssetPairAPI.md#assetpaircontrollercreate) | **POST** /v1/assetPair | Create Asset Pair
[**assetPairControllerCreateAndUpdate**](AssetPairAPI.md#assetpaircontrollercreateandupdate) | **POST** /v1/assetPair/createAndUpdate | Create and update Asset Pairs
[**assetPairControllerCreateBulk**](AssetPairAPI.md#assetpaircontrollercreatebulk) | **POST** /v1/assetPair/bulk | Create Asset Pairs
[**assetPairControllerDelete**](AssetPairAPI.md#assetpaircontrollerdelete) | **DELETE** /v1/assetPair/{recordId} | Delete Asset Pair
[**assetPairControllerFindAll**](AssetPairAPI.md#assetpaircontrollerfindall) | **GET** /v1/assetPair | Get all Asset Pairs
[**assetPairControllerFindOne**](AssetPairAPI.md#assetpaircontrollerfindone) | **GET** /v1/assetPair/{recordId} | Get single Asset Pair
[**assetPairControllerSearch**](AssetPairAPI.md#assetpaircontrollersearch) | **POST** /v1/assetPair/search | Search Asset Pairs
[**assetPairControllerStatistics**](AssetPairAPI.md#assetpaircontrollerstatistics) | **GET** /v1/assetPair/statistics | Asset Pair Statistics
[**assetPairControllerUpdate**](AssetPairAPI.md#assetpaircontrollerupdate) | **PATCH** /v1/assetPair/{recordId} | Update Asset Pair
[**assetPairControllerUpdateBulk**](AssetPairAPI.md#assetpaircontrollerupdatebulk) | **PATCH** /v1/assetPair/bulk | Update Asset Pairs


# **assetPairControllerCount**
```swift
    open class func assetPairControllerCount(countDto: CountDto, completion: @escaping (_ data: Double?, _ error: Error?) -> Void)
```

Count Asset Pairs

Counts matching asset pairs.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let countDto = CountDto(filterOptions: [FilterOptionDto(values: [FilterOptionDto_values_inner()], field: "field_example", _operator: "_operator_example", subFilters: [nil])], returnSoftDeletedEntities: false) // CountDto | 

// Count Asset Pairs
AssetPairAPI.assetPairControllerCount(countDto: countDto) { (response, error) in
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

# **assetPairControllerCreate**
```swift
    open class func assetPairControllerCreate(createAssetPairDto: CreateAssetPairDto, completion: @escaping (_ data: AssetPairDto?, _ error: Error?) -> Void)
```

Create Asset Pair

Creates and returns a new asset pair.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let createAssetPairDto = CreateAssetPairDto(base: "base_example", quote: "quote_example", tradeable: false) // CreateAssetPairDto | 

// Create Asset Pair
AssetPairAPI.assetPairControllerCreate(createAssetPairDto: createAssetPairDto) { (response, error) in
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
 **createAssetPairDto** | [**CreateAssetPairDto**](CreateAssetPairDto.md) |  | 

### Return type

[**AssetPairDto**](AssetPairDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **assetPairControllerCreateAndUpdate**
```swift
    open class func assetPairControllerCreateAndUpdate(createAndUpdateAssetPairDto: [CreateAndUpdateAssetPairDto], completion: @escaping (_ data: [AssetPairDto]?, _ error: Error?) -> Void)
```

Create and update Asset Pairs

Creates or updates and returns multiple asset pairs.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let createAndUpdateAssetPairDto = [CreateAndUpdateAssetPairDto(recordId: 123, creationDt: Date(), updatedOn: Date(), deletionDt: Date(), base: "base_example", quote: "quote_example", tradeable: false)] // [CreateAndUpdateAssetPairDto] | 

// Create and update Asset Pairs
AssetPairAPI.assetPairControllerCreateAndUpdate(createAndUpdateAssetPairDto: createAndUpdateAssetPairDto) { (response, error) in
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
 **createAndUpdateAssetPairDto** | [**[CreateAndUpdateAssetPairDto]**](CreateAndUpdateAssetPairDto.md) |  | 

### Return type

[**[AssetPairDto]**](AssetPairDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **assetPairControllerCreateBulk**
```swift
    open class func assetPairControllerCreateBulk(createAssetPairDto: [CreateAssetPairDto], completion: @escaping (_ data: [AssetPairDto]?, _ error: Error?) -> Void)
```

Create Asset Pairs

Creates and returns multiple new asset pairs.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let createAssetPairDto = [CreateAssetPairDto(base: "base_example", quote: "quote_example", tradeable: false)] // [CreateAssetPairDto] | 

// Create Asset Pairs
AssetPairAPI.assetPairControllerCreateBulk(createAssetPairDto: createAssetPairDto) { (response, error) in
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
 **createAssetPairDto** | [**[CreateAssetPairDto]**](CreateAssetPairDto.md) |  | 

### Return type

[**[AssetPairDto]**](AssetPairDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **assetPairControllerDelete**
```swift
    open class func assetPairControllerDelete(recordId: Double, completion: @escaping (_ data: String?, _ error: Error?) -> Void)
```

Delete Asset Pair

Deletes single asset pair.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let recordId = 987 // Double | 

// Delete Asset Pair
AssetPairAPI.assetPairControllerDelete(recordId: recordId) { (response, error) in
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

# **assetPairControllerFindAll**
```swift
    open class func assetPairControllerFindAll(page: Double, pageSize: Double, completion: @escaping (_ data: [AssetPairDto]?, _ error: Error?) -> Void)
```

Get all Asset Pairs

Returns all asset pairs.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let page = 987 // Double | 
let pageSize = 987 // Double | 

// Get all Asset Pairs
AssetPairAPI.assetPairControllerFindAll(page: page, pageSize: pageSize) { (response, error) in
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

[**[AssetPairDto]**](AssetPairDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **assetPairControllerFindOne**
```swift
    open class func assetPairControllerFindOne(recordId: Double, completion: @escaping (_ data: AssetPairDto?, _ error: Error?) -> Void)
```

Get single Asset Pair

Returns single asset pair.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let recordId = 987 // Double | 

// Get single Asset Pair
AssetPairAPI.assetPairControllerFindOne(recordId: recordId) { (response, error) in
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

[**AssetPairDto**](AssetPairDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **assetPairControllerSearch**
```swift
    open class func assetPairControllerSearch(searchDto: SearchDto, completion: @escaping (_ data: [AssetPairDto]?, _ error: Error?) -> Void)
```

Search Asset Pairs

Returns all matching asset pairs.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let searchDto = SearchDto(orderOption: [OrderOption(field: "field_example", direction: "direction_example")], pageSize: 123, page: 123, enrichments: ["enrichments_example"], filterOptions: [FilterOptionDto(values: [FilterOptionDto_values_inner()], field: "field_example", _operator: "_operator_example", subFilters: [nil])], returnSoftDeletedEntities: false) // SearchDto | 

// Search Asset Pairs
AssetPairAPI.assetPairControllerSearch(searchDto: searchDto) { (response, error) in
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

[**[AssetPairDto]**](AssetPairDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **assetPairControllerStatistics**
```swift
    open class func assetPairControllerStatistics(stats: [String], completion: @escaping (_ data: AssetPairDto?, _ error: Error?) -> Void)
```

Asset Pair Statistics

Not supported.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let stats = ["inner_example"] // [String] | 

// Asset Pair Statistics
AssetPairAPI.assetPairControllerStatistics(stats: stats) { (response, error) in
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

[**AssetPairDto**](AssetPairDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **assetPairControllerUpdate**
```swift
    open class func assetPairControllerUpdate(recordId: Double, updateAssetPairDto: UpdateAssetPairDto, completion: @escaping (_ data: AssetPairDto?, _ error: Error?) -> Void)
```

Update Asset Pair

Updates and returns single asset pair.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let recordId = 987 // Double | 
let updateAssetPairDto = UpdateAssetPairDto(recordId: 123, base: "base_example", quote: "quote_example", tradeable: false) // UpdateAssetPairDto | 

// Update Asset Pair
AssetPairAPI.assetPairControllerUpdate(recordId: recordId, updateAssetPairDto: updateAssetPairDto) { (response, error) in
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
 **updateAssetPairDto** | [**UpdateAssetPairDto**](UpdateAssetPairDto.md) |  | 

### Return type

[**AssetPairDto**](AssetPairDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **assetPairControllerUpdateBulk**
```swift
    open class func assetPairControllerUpdateBulk(updateAssetPairDto: [UpdateAssetPairDto], completion: @escaping (_ data: [AssetPairDto]?, _ error: Error?) -> Void)
```

Update Asset Pairs

Updates and returns multiple asset pairs.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let updateAssetPairDto = [UpdateAssetPairDto(recordId: 123, base: "base_example", quote: "quote_example", tradeable: false)] // [UpdateAssetPairDto] | 

// Update Asset Pairs
AssetPairAPI.assetPairControllerUpdateBulk(updateAssetPairDto: updateAssetPairDto) { (response, error) in
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
 **updateAssetPairDto** | [**[UpdateAssetPairDto]**](UpdateAssetPairDto.md) |  | 

### Return type

[**[AssetPairDto]**](AssetPairDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

