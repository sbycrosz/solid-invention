# ComplianceCheckAPI

All URIs are relative to *https://backend.arkhon.test.arkhon.digital*

Method | HTTP request | Description
------------- | ------------- | -------------
[**complianceCheckControllerCount**](ComplianceCheckAPI.md#compliancecheckcontrollercount) | **POST** /v1/compliancecheck/count | Count Compliance Checks
[**complianceCheckControllerCreate**](ComplianceCheckAPI.md#compliancecheckcontrollercreate) | **POST** /v1/compliancecheck | Create Compliance Check
[**complianceCheckControllerCreateAndUpdate**](ComplianceCheckAPI.md#compliancecheckcontrollercreateandupdate) | **POST** /v1/compliancecheck/createAndUpdate | Create and update Asset Pairs
[**complianceCheckControllerCreateBulk**](ComplianceCheckAPI.md#compliancecheckcontrollercreatebulk) | **POST** /v1/compliancecheck/bulk | Create Compliance Checks
[**complianceCheckControllerDelete**](ComplianceCheckAPI.md#compliancecheckcontrollerdelete) | **DELETE** /v1/compliancecheck/{recordId} | Delete Compliance Check
[**complianceCheckControllerFindAll**](ComplianceCheckAPI.md#compliancecheckcontrollerfindall) | **GET** /v1/compliancecheck | Get all Compliance Checks
[**complianceCheckControllerFindOne**](ComplianceCheckAPI.md#compliancecheckcontrollerfindone) | **GET** /v1/compliancecheck/{recordId} | Get single Compliance Check
[**complianceCheckControllerSearch**](ComplianceCheckAPI.md#compliancecheckcontrollersearch) | **POST** /v1/compliancecheck/search | Search Compliance Checks
[**complianceCheckControllerStatistics**](ComplianceCheckAPI.md#compliancecheckcontrollerstatistics) | **GET** /v1/compliancecheck/statistics | Compliance check Statistics
[**complianceCheckControllerUpdate**](ComplianceCheckAPI.md#compliancecheckcontrollerupdate) | **PATCH** /v1/compliancecheck/{recordId} | Update Compliance Check
[**complianceCheckControllerUpdateBulk**](ComplianceCheckAPI.md#compliancecheckcontrollerupdatebulk) | **PATCH** /v1/compliancecheck/bulk | Update Compliance Checks


# **complianceCheckControllerCount**
```swift
    open class func complianceCheckControllerCount(countDto: CountDto, completion: @escaping (_ data: Double?, _ error: Error?) -> Void)
```

Count Compliance Checks

Counts matching Compliance Checks.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let countDto = CountDto(filterOptions: [FilterOptionDto(values: [FilterOptionDto_values_inner()], field: "field_example", _operator: "_operator_example", subFilters: [nil])], returnSoftDeletedEntities: false) // CountDto | 

// Count Compliance Checks
ComplianceCheckAPI.complianceCheckControllerCount(countDto: countDto) { (response, error) in
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

# **complianceCheckControllerCreate**
```swift
    open class func complianceCheckControllerCreate(createComplianceCheckDto: CreateComplianceCheckDto, completion: @escaping (_ data: ComplianceCheckDto?, _ error: Error?) -> Void)
```

Create Compliance Check

Creates and returns a new Compliance Check.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let createComplianceCheckDto = CreateComplianceCheckDto(currency: "currency_example", blockchain: "blockchain_example", walletAddress: "walletAddress_example", isVASP: false, assetTier: "assetTier_example", riskRating: "riskRating_example", riskTriggerSourceRiskScore: "riskTriggerSourceRiskScore_example", riskTriggerSourceCategory: "riskTriggerSourceCategory_example", riskTriggerSourceIsSanctioned: false, riskTriggerDestinationRiskScore: "riskTriggerDestinationRiskScore_example", riskTriggerDestinationCategory: "riskTriggerDestinationCategory_example", riskTriggerDestinationIsSanctioned: false, accountId: 123, transferId: 123, platformId: 123) // CreateComplianceCheckDto | 

// Create Compliance Check
ComplianceCheckAPI.complianceCheckControllerCreate(createComplianceCheckDto: createComplianceCheckDto) { (response, error) in
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
 **createComplianceCheckDto** | [**CreateComplianceCheckDto**](CreateComplianceCheckDto.md) |  | 

### Return type

[**ComplianceCheckDto**](ComplianceCheckDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **complianceCheckControllerCreateAndUpdate**
```swift
    open class func complianceCheckControllerCreateAndUpdate(createAndUpdateComplianceCheckDto: [CreateAndUpdateComplianceCheckDto], completion: @escaping (_ data: [ComplianceCheckDto]?, _ error: Error?) -> Void)
```

Create and update Asset Pairs

Creates or updates and returns multiple asset pairs.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let createAndUpdateComplianceCheckDto = [CreateAndUpdateComplianceCheckDto(recordId: 123, currency: "currency_example", blockchain: "blockchain_example", walletAddress: "walletAddress_example", isVASP: false, assetTier: "assetTier_example", riskRating: "riskRating_example", riskTriggerSourceRiskScore: "riskTriggerSourceRiskScore_example", riskTriggerSourceCategory: "riskTriggerSourceCategory_example", riskTriggerSourceIsSanctioned: false, riskTriggerDestinationRiskScore: "riskTriggerDestinationRiskScore_example", riskTriggerDestinationCategory: "riskTriggerDestinationCategory_example", riskTriggerDestinationIsSanctioned: false, accountId: 123, transferId: 123, platformId: 123, creationDt: Date(), updatedOn: Date(), deletionDt: Date())] // [CreateAndUpdateComplianceCheckDto] | 

// Create and update Asset Pairs
ComplianceCheckAPI.complianceCheckControllerCreateAndUpdate(createAndUpdateComplianceCheckDto: createAndUpdateComplianceCheckDto) { (response, error) in
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
 **createAndUpdateComplianceCheckDto** | [**[CreateAndUpdateComplianceCheckDto]**](CreateAndUpdateComplianceCheckDto.md) |  | 

### Return type

[**[ComplianceCheckDto]**](ComplianceCheckDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **complianceCheckControllerCreateBulk**
```swift
    open class func complianceCheckControllerCreateBulk(createComplianceCheckDto: [CreateComplianceCheckDto], completion: @escaping (_ data: [ComplianceCheckDto]?, _ error: Error?) -> Void)
```

Create Compliance Checks

Creates and returns multiple new Compliance Checks.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let createComplianceCheckDto = [CreateComplianceCheckDto(currency: "currency_example", blockchain: "blockchain_example", walletAddress: "walletAddress_example", isVASP: false, assetTier: "assetTier_example", riskRating: "riskRating_example", riskTriggerSourceRiskScore: "riskTriggerSourceRiskScore_example", riskTriggerSourceCategory: "riskTriggerSourceCategory_example", riskTriggerSourceIsSanctioned: false, riskTriggerDestinationRiskScore: "riskTriggerDestinationRiskScore_example", riskTriggerDestinationCategory: "riskTriggerDestinationCategory_example", riskTriggerDestinationIsSanctioned: false, accountId: 123, transferId: 123, platformId: 123)] // [CreateComplianceCheckDto] | 

// Create Compliance Checks
ComplianceCheckAPI.complianceCheckControllerCreateBulk(createComplianceCheckDto: createComplianceCheckDto) { (response, error) in
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
 **createComplianceCheckDto** | [**[CreateComplianceCheckDto]**](CreateComplianceCheckDto.md) |  | 

### Return type

[**[ComplianceCheckDto]**](ComplianceCheckDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **complianceCheckControllerDelete**
```swift
    open class func complianceCheckControllerDelete(recordId: Double, completion: @escaping (_ data: String?, _ error: Error?) -> Void)
```

Delete Compliance Check

Deletes single Compliance Check.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let recordId = 987 // Double | 

// Delete Compliance Check
ComplianceCheckAPI.complianceCheckControllerDelete(recordId: recordId) { (response, error) in
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

# **complianceCheckControllerFindAll**
```swift
    open class func complianceCheckControllerFindAll(page: Double, pageSize: Double, completion: @escaping (_ data: [ComplianceCheckDto]?, _ error: Error?) -> Void)
```

Get all Compliance Checks

Returns all Compliance Checks.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let page = 987 // Double | 
let pageSize = 987 // Double | 

// Get all Compliance Checks
ComplianceCheckAPI.complianceCheckControllerFindAll(page: page, pageSize: pageSize) { (response, error) in
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

[**[ComplianceCheckDto]**](ComplianceCheckDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **complianceCheckControllerFindOne**
```swift
    open class func complianceCheckControllerFindOne(recordId: Double, completion: @escaping (_ data: ComplianceCheckDto?, _ error: Error?) -> Void)
```

Get single Compliance Check

Returns single Compliance Check.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let recordId = 987 // Double | 

// Get single Compliance Check
ComplianceCheckAPI.complianceCheckControllerFindOne(recordId: recordId) { (response, error) in
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

[**ComplianceCheckDto**](ComplianceCheckDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **complianceCheckControllerSearch**
```swift
    open class func complianceCheckControllerSearch(searchDto: SearchDto, completion: @escaping (_ data: [ComplianceCheckDto]?, _ error: Error?) -> Void)
```

Search Compliance Checks

Returns all matching Compliance Checks.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let searchDto = SearchDto(orderOption: [OrderOption(field: "field_example", direction: "direction_example")], pageSize: 123, page: 123, enrichments: ["enrichments_example"], filterOptions: [FilterOptionDto(values: [FilterOptionDto_values_inner()], field: "field_example", _operator: "_operator_example", subFilters: [nil])], returnSoftDeletedEntities: false) // SearchDto | 

// Search Compliance Checks
ComplianceCheckAPI.complianceCheckControllerSearch(searchDto: searchDto) { (response, error) in
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

[**[ComplianceCheckDto]**](ComplianceCheckDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **complianceCheckControllerStatistics**
```swift
    open class func complianceCheckControllerStatistics(stats: [String], completion: @escaping (_ data: ComplianceCheckDto?, _ error: Error?) -> Void)
```

Compliance check Statistics

Not supported.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let stats = ["inner_example"] // [String] | 

// Compliance check Statistics
ComplianceCheckAPI.complianceCheckControllerStatistics(stats: stats) { (response, error) in
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

[**ComplianceCheckDto**](ComplianceCheckDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **complianceCheckControllerUpdate**
```swift
    open class func complianceCheckControllerUpdate(recordId: Double, updateComplianceCheckDto: UpdateComplianceCheckDto, completion: @escaping (_ data: ComplianceCheckDto?, _ error: Error?) -> Void)
```

Update Compliance Check

Updates and returns single Compliance Check.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let recordId = 987 // Double | 
let updateComplianceCheckDto = UpdateComplianceCheckDto(recordId: 123, currency: "currency_example", blockchain: "blockchain_example", walletAddress: "walletAddress_example", isVASP: false, assetTier: "assetTier_example", riskRating: "riskRating_example", riskTriggerSourceRiskScore: "riskTriggerSourceRiskScore_example", riskTriggerSourceCategory: "riskTriggerSourceCategory_example", riskTriggerSourceIsSanctioned: false, riskTriggerDestinationRiskScore: "riskTriggerDestinationRiskScore_example", riskTriggerDestinationCategory: "riskTriggerDestinationCategory_example", riskTriggerDestinationIsSanctioned: false, accountId: 123, transferId: 123, platformId: 123) // UpdateComplianceCheckDto | 

// Update Compliance Check
ComplianceCheckAPI.complianceCheckControllerUpdate(recordId: recordId, updateComplianceCheckDto: updateComplianceCheckDto) { (response, error) in
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
 **updateComplianceCheckDto** | [**UpdateComplianceCheckDto**](UpdateComplianceCheckDto.md) |  | 

### Return type

[**ComplianceCheckDto**](ComplianceCheckDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **complianceCheckControllerUpdateBulk**
```swift
    open class func complianceCheckControllerUpdateBulk(updateComplianceCheckDto: [UpdateComplianceCheckDto], completion: @escaping (_ data: [ComplianceCheckDto]?, _ error: Error?) -> Void)
```

Update Compliance Checks

Updates and returns multiple Compliance Checks.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let updateComplianceCheckDto = [UpdateComplianceCheckDto(recordId: 123, currency: "currency_example", blockchain: "blockchain_example", walletAddress: "walletAddress_example", isVASP: false, assetTier: "assetTier_example", riskRating: "riskRating_example", riskTriggerSourceRiskScore: "riskTriggerSourceRiskScore_example", riskTriggerSourceCategory: "riskTriggerSourceCategory_example", riskTriggerSourceIsSanctioned: false, riskTriggerDestinationRiskScore: "riskTriggerDestinationRiskScore_example", riskTriggerDestinationCategory: "riskTriggerDestinationCategory_example", riskTriggerDestinationIsSanctioned: false, accountId: 123, transferId: 123, platformId: 123)] // [UpdateComplianceCheckDto] | 

// Update Compliance Checks
ComplianceCheckAPI.complianceCheckControllerUpdateBulk(updateComplianceCheckDto: updateComplianceCheckDto) { (response, error) in
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
 **updateComplianceCheckDto** | [**[UpdateComplianceCheckDto]**](UpdateComplianceCheckDto.md) |  | 

### Return type

[**[ComplianceCheckDto]**](ComplianceCheckDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

