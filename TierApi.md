# TierAPI

All URIs are relative to *https://backend.arkhon.test.arkhon.digital*

Method | HTTP request | Description
------------- | ------------- | -------------
[**tierControllerCount**](TierAPI.md#tiercontrollercount) | **POST** /v1/tiers/count | Count Tiers
[**tierControllerCreate**](TierAPI.md#tiercontrollercreate) | **POST** /v1/tiers | Create new Tier
[**tierControllerCreateAndUpdate**](TierAPI.md#tiercontrollercreateandupdate) | **POST** /v1/tiers/createAndUpdate | Create and update Tiers
[**tierControllerCreateBulk**](TierAPI.md#tiercontrollercreatebulk) | **POST** /v1/tiers/bulk | Create new Tiers
[**tierControllerDelete**](TierAPI.md#tiercontrollerdelete) | **DELETE** /v1/tiers/{recordId} | Delete a Tier
[**tierControllerFindAll**](TierAPI.md#tiercontrollerfindall) | **GET** /v1/tiers | Get all Tiers
[**tierControllerFindOne**](TierAPI.md#tiercontrollerfindone) | **GET** /v1/tiers/{recordId} | Get single Tier
[**tierControllerSearch**](TierAPI.md#tiercontrollersearch) | **POST** /v1/tiers/search | Search Tiers
[**tierControllerStatistics**](TierAPI.md#tiercontrollerstatistics) | **GET** /v1/tiers/statistics | Tier Statistics
[**tierControllerUpdate**](TierAPI.md#tiercontrollerupdate) | **PATCH** /v1/tiers/{recordId} | Update an Asset
[**tierControllerUpdateBulk**](TierAPI.md#tiercontrollerupdatebulk) | **PATCH** /v1/tiers/bulk | Update multiple Tiers


# **tierControllerCount**
```swift
    open class func tierControllerCount(countDto: CountDto, completion: @escaping (_ data: Double?, _ error: Error?) -> Void)
```

Count Tiers

Counts matching tiers.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let countDto = CountDto(filterOptions: [FilterOptionDto(values: [FilterOptionDto_values_inner()], field: "field_example", _operator: "_operator_example", subFilters: [nil])], returnSoftDeletedEntities: false) // CountDto | 

// Count Tiers
TierAPI.tierControllerCount(countDto: countDto) { (response, error) in
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

# **tierControllerCreate**
```swift
    open class func tierControllerCreate(createTierDto: CreateTierDto, completion: @escaping (_ data: TierDto?, _ error: Error?) -> Void)
```

Create new Tier

Creates and returns a new tier.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let createTierDto = CreateTierDto(fromBasisPoint: "fromBasisPoint_example", feeValue: "feeValue_example", name: "name_example", validFrom: Date(), validUntil: Date()) // CreateTierDto | 

// Create new Tier
TierAPI.tierControllerCreate(createTierDto: createTierDto) { (response, error) in
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
 **createTierDto** | [**CreateTierDto**](CreateTierDto.md) |  | 

### Return type

[**TierDto**](TierDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **tierControllerCreateAndUpdate**
```swift
    open class func tierControllerCreateAndUpdate(createAndUpdateTierDto: [CreateAndUpdateTierDto], completion: @escaping (_ data: [TierDto]?, _ error: Error?) -> Void)
```

Create and update Tiers

Creates or updates and returns multiple tiers.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let createAndUpdateTierDto = [CreateAndUpdateTierDto(recordId: 123, fromBasisPoint: "fromBasisPoint_example", feeValue: "feeValue_example", creationDt: Date(), updatedOn: Date(), deletionDt: Date(), name: "name_example", validFrom: Date(), validUntil: Date())] // [CreateAndUpdateTierDto] | 

// Create and update Tiers
TierAPI.tierControllerCreateAndUpdate(createAndUpdateTierDto: createAndUpdateTierDto) { (response, error) in
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
 **createAndUpdateTierDto** | [**[CreateAndUpdateTierDto]**](CreateAndUpdateTierDto.md) |  | 

### Return type

[**[TierDto]**](TierDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **tierControllerCreateBulk**
```swift
    open class func tierControllerCreateBulk(createTierDto: [CreateTierDto], completion: @escaping (_ data: [TierDto]?, _ error: Error?) -> Void)
```

Create new Tiers

Creates and returns multiple new tiers.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let createTierDto = [CreateTierDto(fromBasisPoint: "fromBasisPoint_example", feeValue: "feeValue_example", name: "name_example", validFrom: Date(), validUntil: Date())] // [CreateTierDto] | 

// Create new Tiers
TierAPI.tierControllerCreateBulk(createTierDto: createTierDto) { (response, error) in
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
 **createTierDto** | [**[CreateTierDto]**](CreateTierDto.md) |  | 

### Return type

[**[TierDto]**](TierDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **tierControllerDelete**
```swift
    open class func tierControllerDelete(recordId: Double, completion: @escaping (_ data: String?, _ error: Error?) -> Void)
```

Delete a Tier

UNSUPPORTED; Deleting tiers is not possible. Once an tier has been created it could have been used in various transactions, and deleting it after the fact would not be safe. You can update a tier to no longer be applicable, which we suggest to do instead of deleting it. Please contact Arkhon support if you wish to delete a tier.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let recordId = 987 // Double | 

// Delete a Tier
TierAPI.tierControllerDelete(recordId: recordId) { (response, error) in
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

# **tierControllerFindAll**
```swift
    open class func tierControllerFindAll(page: Double, pageSize: Double, completion: @escaping (_ data: [TierDto]?, _ error: Error?) -> Void)
```

Get all Tiers

Returns all tiers.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let page = 987 // Double | 
let pageSize = 987 // Double | 

// Get all Tiers
TierAPI.tierControllerFindAll(page: page, pageSize: pageSize) { (response, error) in
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

[**[TierDto]**](TierDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **tierControllerFindOne**
```swift
    open class func tierControllerFindOne(recordId: Double, completion: @escaping (_ data: TierDto?, _ error: Error?) -> Void)
```

Get single Tier

Returns single tier.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let recordId = 987 // Double | 

// Get single Tier
TierAPI.tierControllerFindOne(recordId: recordId) { (response, error) in
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

[**TierDto**](TierDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **tierControllerSearch**
```swift
    open class func tierControllerSearch(searchDto: SearchDto, completion: @escaping (_ data: [TierDto]?, _ error: Error?) -> Void)
```

Search Tiers

Returns matching tiers.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let searchDto = SearchDto(orderOption: [OrderOption(field: "field_example", direction: "direction_example")], pageSize: 123, page: 123, enrichments: ["enrichments_example"], filterOptions: [FilterOptionDto(values: [FilterOptionDto_values_inner()], field: "field_example", _operator: "_operator_example", subFilters: [nil])], returnSoftDeletedEntities: false) // SearchDto | 

// Search Tiers
TierAPI.tierControllerSearch(searchDto: searchDto) { (response, error) in
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

[**[TierDto]**](TierDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **tierControllerStatistics**
```swift
    open class func tierControllerStatistics(stats: [String], completion: @escaping (_ data: TierDto?, _ error: Error?) -> Void)
```

Tier Statistics

Not supported.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let stats = ["inner_example"] // [String] | 

// Tier Statistics
TierAPI.tierControllerStatistics(stats: stats) { (response, error) in
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

[**TierDto**](TierDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **tierControllerUpdate**
```swift
    open class func tierControllerUpdate(recordId: Double, updateTierDto: UpdateTierDto, completion: @escaping (_ data: TierDto?, _ error: Error?) -> Void)
```

Update an Asset

Updates and returns a single asset.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let recordId = 987 // Double | 
let updateTierDto = UpdateTierDto(recordId: 123, fromBasisPoint: "fromBasisPoint_example", feeValue: "feeValue_example", name: "name_example", validFrom: Date(), validUntil: Date()) // UpdateTierDto | 

// Update an Asset
TierAPI.tierControllerUpdate(recordId: recordId, updateTierDto: updateTierDto) { (response, error) in
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
 **updateTierDto** | [**UpdateTierDto**](UpdateTierDto.md) |  | 

### Return type

[**TierDto**](TierDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **tierControllerUpdateBulk**
```swift
    open class func tierControllerUpdateBulk(updateTierDto: [UpdateTierDto], completion: @escaping (_ data: [TierDto]?, _ error: Error?) -> Void)
```

Update multiple Tiers

Updates and returns multiple tiers.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let updateTierDto = [UpdateTierDto(recordId: 123, fromBasisPoint: "fromBasisPoint_example", feeValue: "feeValue_example", name: "name_example", validFrom: Date(), validUntil: Date())] // [UpdateTierDto] | 

// Update multiple Tiers
TierAPI.tierControllerUpdateBulk(updateTierDto: updateTierDto) { (response, error) in
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
 **updateTierDto** | [**[UpdateTierDto]**](UpdateTierDto.md) |  | 

### Return type

[**[TierDto]**](TierDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

