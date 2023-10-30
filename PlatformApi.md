# PlatformAPI

All URIs are relative to *https://backend.arkhon.test.arkhon.digital*

Method | HTTP request | Description
------------- | ------------- | -------------
[**platformAssetsControllerFindAllPlatformAssets**](PlatformAPI.md#platformassetscontrollerfindallplatformassets) | **GET** /v1/platforms/{platformId}/assets | Get Platform Assets
[**platformAssetsControllerFindSinglePlatformAsset**](PlatformAPI.md#platformassetscontrollerfindsingleplatformasset) | **GET** /v1/platforms/{platformId}/assets/{symbol} | Get single Platform Asset
[**platformControllerCount**](PlatformAPI.md#platformcontrollercount) | **POST** /v1/platforms/count | Count Platforms
[**platformControllerCreate**](PlatformAPI.md#platformcontrollercreate) | **POST** /v1/platforms | Create a new Platform
[**platformControllerCreateAndUpdate**](PlatformAPI.md#platformcontrollercreateandupdate) | **POST** /v1/platforms/createAndUpdate | Create and update Asset Pairs
[**platformControllerCreateBulk**](PlatformAPI.md#platformcontrollercreatebulk) | **POST** /v1/platforms/bulk | Create multiple new Platforms
[**platformControllerDelete**](PlatformAPI.md#platformcontrollerdelete) | **DELETE** /v1/platforms/{recordId} | Delete a Platform
[**platformControllerFindAll**](PlatformAPI.md#platformcontrollerfindall) | **GET** /v1/platforms | Get all Platforms
[**platformControllerFindOne**](PlatformAPI.md#platformcontrollerfindone) | **GET** /v1/platforms/{recordId} | Get single Platform
[**platformControllerSearch**](PlatformAPI.md#platformcontrollersearch) | **POST** /v1/platforms/search | Search Platforms
[**platformControllerStatistics**](PlatformAPI.md#platformcontrollerstatistics) | **GET** /v1/platforms/statistics | Platform Statistics
[**platformControllerUpdate**](PlatformAPI.md#platformcontrollerupdate) | **PATCH** /v1/platforms/{recordId} | Updates single Platform
[**platformControllerUpdateBulk**](PlatformAPI.md#platformcontrollerupdatebulk) | **PATCH** /v1/platforms/bulk | Updates multiple Platforms
[**settlementControllerCount**](PlatformAPI.md#settlementcontrollercount) | **POST** /v1/platforms/{platformId}/settlements/count | Count Settlements
[**settlementControllerCreate**](PlatformAPI.md#settlementcontrollercreate) | **POST** /v1/platforms/{platformId}/settlements | Create Settlement
[**settlementControllerCreateAndUpdate**](PlatformAPI.md#settlementcontrollercreateandupdate) | **POST** /v1/platforms/{platformId}/settlements/createAndUpdate | Create and update Asset Pairs
[**settlementControllerCreateBulk**](PlatformAPI.md#settlementcontrollercreatebulk) | **POST** /v1/platforms/{platformId}/settlements/bulk | Create multiple Settlements
[**settlementControllerDelete**](PlatformAPI.md#settlementcontrollerdelete) | **DELETE** /v1/platforms/{platformId}/settlements/{recordId} | Delete Settlement
[**settlementControllerFindAll**](PlatformAPI.md#settlementcontrollerfindall) | **GET** /v1/platforms/{platformId}/settlements | Get all Settlements
[**settlementControllerFindOne**](PlatformAPI.md#settlementcontrollerfindone) | **GET** /v1/platforms/{platformId}/settlements/{recordId} | Get single Settlement
[**settlementControllerSearch**](PlatformAPI.md#settlementcontrollersearch) | **POST** /v1/platforms/{platformId}/settlements/search | Search Settlements
[**settlementControllerStatistics**](PlatformAPI.md#settlementcontrollerstatistics) | **GET** /v1/platforms/{platformId}/settlements/statistics | Settlement Statistics
[**settlementControllerUpdate**](PlatformAPI.md#settlementcontrollerupdate) | **PATCH** /v1/platforms/{platformId}/settlements/{recordId} | Update single Settlement
[**settlementControllerUpdateBulk**](PlatformAPI.md#settlementcontrollerupdatebulk) | **PATCH** /v1/platforms/{platformId}/settlements/bulk | Update multiple Settlements


# **platformAssetsControllerFindAllPlatformAssets**
```swift
    open class func platformAssetsControllerFindAllPlatformAssets(platformId: Double, completion: @escaping (_ data: [PlatformAssetDto]?, _ error: Error?) -> Void)
```

Get Platform Assets

Returns all assets on a platform.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let platformId = 987 // Double | 

// Get Platform Assets
PlatformAPI.platformAssetsControllerFindAllPlatformAssets(platformId: platformId) { (response, error) in
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
 **platformId** | **Double** |  | 

### Return type

[**[PlatformAssetDto]**](PlatformAssetDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **platformAssetsControllerFindSinglePlatformAsset**
```swift
    open class func platformAssetsControllerFindSinglePlatformAsset(platformId: Double, symbol: String, completion: @escaping (_ data: String?, _ error: Error?) -> Void)
```

Get single Platform Asset

Returns single asset of a platform.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let platformId = 987 // Double | 
let symbol = "symbol_example" // String | 

// Get single Platform Asset
PlatformAPI.platformAssetsControllerFindSinglePlatformAsset(platformId: platformId, symbol: symbol) { (response, error) in
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
 **platformId** | **Double** |  | 
 **symbol** | **String** |  | 

### Return type

**String**

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **platformControllerCount**
```swift
    open class func platformControllerCount(countDto: CountDto, completion: @escaping (_ data: Double?, _ error: Error?) -> Void)
```

Count Platforms

Counts matching platforms.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let countDto = CountDto(filterOptions: [FilterOptionDto(values: [FilterOptionDto_values_inner()], field: "field_example", _operator: "_operator_example", subFilters: [nil])], returnSoftDeletedEntities: false) // CountDto | 

// Count Platforms
PlatformAPI.platformControllerCount(countDto: countDto) { (response, error) in
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

# **platformControllerCreate**
```swift
    open class func platformControllerCreate(createPlatformDto: CreatePlatformDto, completion: @escaping (_ data: PlatformDto?, _ error: Error?) -> Void)
```

Create a new Platform

Creates and returns new platform.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let createPlatformDto = CreatePlatformDto(name: "name_example", isCustody: false, isVaspCapable: false) // CreatePlatformDto | 

// Create a new Platform
PlatformAPI.platformControllerCreate(createPlatformDto: createPlatformDto) { (response, error) in
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
 **createPlatformDto** | [**CreatePlatformDto**](CreatePlatformDto.md) |  | 

### Return type

[**PlatformDto**](PlatformDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **platformControllerCreateAndUpdate**
```swift
    open class func platformControllerCreateAndUpdate(createAndUpdatePlatformDto: [CreateAndUpdatePlatformDto], completion: @escaping (_ data: [PlatformDto]?, _ error: Error?) -> Void)
```

Create and update Asset Pairs

Creates or updates and returns multiple asset pairs.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let createAndUpdatePlatformDto = [CreateAndUpdatePlatformDto(recordId: 123, creationDt: Date(), updatedOn: Date(), deletionDt: Date(), name: "name_example", isCustody: false, isVaspCapable: false)] // [CreateAndUpdatePlatformDto] | 

// Create and update Asset Pairs
PlatformAPI.platformControllerCreateAndUpdate(createAndUpdatePlatformDto: createAndUpdatePlatformDto) { (response, error) in
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
 **createAndUpdatePlatformDto** | [**[CreateAndUpdatePlatformDto]**](CreateAndUpdatePlatformDto.md) |  | 

### Return type

[**[PlatformDto]**](PlatformDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **platformControllerCreateBulk**
```swift
    open class func platformControllerCreateBulk(createPlatformDto: [CreatePlatformDto], completion: @escaping (_ data: [PlatformDto]?, _ error: Error?) -> Void)
```

Create multiple new Platforms

Creates and returns new platforms.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let createPlatformDto = [CreatePlatformDto(name: "name_example", isCustody: false, isVaspCapable: false)] // [CreatePlatformDto] | 

// Create multiple new Platforms
PlatformAPI.platformControllerCreateBulk(createPlatformDto: createPlatformDto) { (response, error) in
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
 **createPlatformDto** | [**[CreatePlatformDto]**](CreatePlatformDto.md) |  | 

### Return type

[**[PlatformDto]**](PlatformDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **platformControllerDelete**
```swift
    open class func platformControllerDelete(recordId: Double, completion: @escaping (_ data: String?, _ error: Error?) -> Void)
```

Delete a Platform

UNSUPPORTED; Deleting platforms is not possible. Once a platform has been created it could have been used in various transactions, and deleting it after the fact would not be safe. Please contact Arkhon support if you wish to delete a platform.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let recordId = 987 // Double | 

// Delete a Platform
PlatformAPI.platformControllerDelete(recordId: recordId) { (response, error) in
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

# **platformControllerFindAll**
```swift
    open class func platformControllerFindAll(page: Double, pageSize: Double, completion: @escaping (_ data: [PlatformDto]?, _ error: Error?) -> Void)
```

Get all Platforms

Returns all platforms.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let page = 987 // Double | 
let pageSize = 987 // Double | 

// Get all Platforms
PlatformAPI.platformControllerFindAll(page: page, pageSize: pageSize) { (response, error) in
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

[**[PlatformDto]**](PlatformDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **platformControllerFindOne**
```swift
    open class func platformControllerFindOne(recordId: Double, completion: @escaping (_ data: PlatformDto?, _ error: Error?) -> Void)
```

Get single Platform

Returns single platform.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let recordId = 987 // Double | 

// Get single Platform
PlatformAPI.platformControllerFindOne(recordId: recordId) { (response, error) in
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

[**PlatformDto**](PlatformDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **platformControllerSearch**
```swift
    open class func platformControllerSearch(searchDto: SearchDto, completion: @escaping (_ data: [PlatformDto]?, _ error: Error?) -> Void)
```

Search Platforms

Returns matching platforms.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let searchDto = SearchDto(orderOption: [OrderOption(field: "field_example", direction: "direction_example")], pageSize: 123, page: 123, enrichments: ["enrichments_example"], filterOptions: [FilterOptionDto(values: [FilterOptionDto_values_inner()], field: "field_example", _operator: "_operator_example", subFilters: [nil])], returnSoftDeletedEntities: false) // SearchDto | 

// Search Platforms
PlatformAPI.platformControllerSearch(searchDto: searchDto) { (response, error) in
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

[**[PlatformDto]**](PlatformDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **platformControllerStatistics**
```swift
    open class func platformControllerStatistics(stats: [String], completion: @escaping (_ data: PlatformDto?, _ error: Error?) -> Void)
```

Platform Statistics

Not supported.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let stats = ["inner_example"] // [String] | 

// Platform Statistics
PlatformAPI.platformControllerStatistics(stats: stats) { (response, error) in
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

[**PlatformDto**](PlatformDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **platformControllerUpdate**
```swift
    open class func platformControllerUpdate(recordId: Double, updatePlatformDto: UpdatePlatformDto, completion: @escaping (_ data: PlatformDto?, _ error: Error?) -> Void)
```

Updates single Platform

Updates and returns platform identified by :recordId

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let recordId = 987 // Double | 
let updatePlatformDto = UpdatePlatformDto(recordId: 123, name: "name_example", isCustody: false, isVaspCapable: false) // UpdatePlatformDto | 

// Updates single Platform
PlatformAPI.platformControllerUpdate(recordId: recordId, updatePlatformDto: updatePlatformDto) { (response, error) in
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
 **updatePlatformDto** | [**UpdatePlatformDto**](UpdatePlatformDto.md) |  | 

### Return type

[**PlatformDto**](PlatformDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **platformControllerUpdateBulk**
```swift
    open class func platformControllerUpdateBulk(updatePlatformDto: [UpdatePlatformDto], completion: @escaping (_ data: [PlatformDto]?, _ error: Error?) -> Void)
```

Updates multiple Platforms

Updates and returns platforms.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let updatePlatformDto = [UpdatePlatformDto(recordId: 123, name: "name_example", isCustody: false, isVaspCapable: false)] // [UpdatePlatformDto] | 

// Updates multiple Platforms
PlatformAPI.platformControllerUpdateBulk(updatePlatformDto: updatePlatformDto) { (response, error) in
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
 **updatePlatformDto** | [**[UpdatePlatformDto]**](UpdatePlatformDto.md) |  | 

### Return type

[**[PlatformDto]**](PlatformDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **settlementControllerCount**
```swift
    open class func settlementControllerCount(platformId: Double, countDto: CountDto, completion: @escaping (_ data: Double?, _ error: Error?) -> Void)
```

Count Settlements

Counts matching settlements to which the logged in user has access.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let platformId = 987 // Double | 
let countDto = CountDto(filterOptions: [FilterOptionDto(values: [FilterOptionDto_values_inner()], field: "field_example", _operator: "_operator_example", subFilters: [nil])], returnSoftDeletedEntities: false) // CountDto | 

// Count Settlements
PlatformAPI.settlementControllerCount(platformId: platformId, countDto: countDto) { (response, error) in
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
 **platformId** | **Double** |  | 
 **countDto** | [**CountDto**](CountDto.md) |  | 

### Return type

**Double**

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **settlementControllerCreate**
```swift
    open class func settlementControllerCreate(platformId: Double, createSettlementDto: CreateSettlementDto, completion: @escaping (_ data: SettlementDto?, _ error: Error?) -> Void)
```

Create Settlement

Creates and returns a settlement.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let platformId = 987 // Double | 
let createSettlementDto = CreateSettlementDto(sourcePlatformId: 123, targetPlatformId: 123, orders: [OrderDto(recordId: 123, portfolioId: 123, userId: 123, executedBy: 123, pricePerUnit: "pricePerUnit_example", lpPricePerUnit: "lpPricePerUnit_example", stopPrice: "stopPrice_example", requestedQuantity: "requestedQuantity_example", filledQuantity: "filledQuantity_example", platformId: 123, platformFee: "platformFee_example", arkhonFeePercentage: "arkhonFeePercentage_example", arkhonSpreadPercentage: "arkhonSpreadPercentage_example", tierId: 123, arkhonSpread: "arkhonSpread_example", arkhonFee: "arkhonFee_example", totalFees: "totalFees_example", subtotal: "subtotal_example", totalConsideration: "totalConsideration_example", portfolio: PortfolioDto(recordId: 123, accountId: 123, account: AccountDto(recordId: 123, tradeFeePercentageOverride: "tradeFeePercentageOverride_example", slackChannelId: "slackChannelId_example", accountType: "accountType_example", accountRefId: "accountRefId_example", status: "status_example", portfolios: [nil], accountUsers: [AccountUserDto(recordId: 123, userId: 123, accountId: 123, updatedOn: Date(), deletionDt: Date(), creationDt: Date())], enrichments: [AccountOrPortfolioEnrichmentDto(value: AccountOrPortfolioEnrichmentDto_value(gains: PortfolioAssetEnrichmentDto_gains(hour: "hour_example", hourPercentage: "hourPercentage_example", day: "day_example", dayPercentage: "dayPercentage_example", week: "week_example", weekPercentage: "weekPercentage_example", month: "month_example", monthPercentage: "monthPercentage_example", year: "year_example", yearPercentage: "yearPercentage_example", allTime: "allTime_example", allTimePercentage: "allTimePercentage_example"), marketValue: "marketValue_example", base: "base_example", assets: [PortfolioAssetEnrichmentDto_assets_inner(quantity: "quantity_example", symbol: "symbol_example", marketPrice: "marketPrice_example", marketValue: "marketValue_example", percentAllocated: "percentAllocated_example", base: "base_example", gains: [GainEntryDto(value: "value_example", type: "type_example")])], topAccounts: [MarketValueStatisticDto(marketValue: "marketValue_example", accountMarketValuePercentOfAllAccounts: "accountMarketValuePercentOfAllAccounts_example", gains: Gains(hour: "hour_example", hourPercentage: "hourPercentage_example", day: "day_example", dayPercentage: "dayPercentage_example", week: "week_example", weekPercentage: "weekPercentage_example", month: "month_example", monthPercentage: "monthPercentage_example", year: "year_example", yearPercentage: "yearPercentage_example", allTime: "allTime_example", allTimePercentage: "allTimePercentage_example"), accountGains: [nil], accountRefId: "accountRefId_example")]), type: "type_example")], statistics: [nil], updatedOn: Date(), deletionDt: Date(), creationDt: Date()), type: "type_example", orders: [nil], transfers: [TransferDto(recordId: 123, portfolioId: 123, secondaryPortfolioId: 123, userId: 123, executedBy: 123, quantity: "quantity_example", platformId: 123, portfolio: nil, type: "type_example", currency: "currency_example", status: "status_example", platform: PlatformDto(recordId: 123, name: "name_example", isCustody: false, isVaspCapable: false, updatedOn: Date(), deletionDt: Date(), creationDt: Date()), platformRefId: "platformRefId_example", clientRefId: "clientRefId_example", receiptTime: Date(), creditTime: Date(), withdrawalTime: Date(), comment: "comment_example", version: 123, updatedOn: Date(), deletionDt: Date(), creationDt: Date())], enrichments: [nil], updatedOn: Date(), deletionDt: Date(), creationDt: Date()), baseToken: "baseToken_example", quoteToken: "quoteToken_example", tradedToken: "tradedToken_example", side: "side_example", startTime: Date(), endTime: Date(), strategy: "strategy_example", type: "type_example", platform: nil, platformRefId: "platformRefId_example", clientRefId: "clientRefId_example", platformFeeCurrency: "platformFeeCurrency_example", status: "status_example", arkhonFeeCurrency: "arkhonFeeCurrency_example", feeStatus: "feeStatus_example", feeComment: "feeComment_example", comment: "comment_example", settlementId: 123, description: "description_example", enrichments: OrderEnrichment(fiatFxOnRequestedBaseCurrency: "fiatFxOnRequestedBaseCurrency_example"), statistics: [AssetStatistic(type: "type_example", value: [AssetStatisticEntry(quantity: "quantity_example", currency: "currency_example")])], version: 123, updatedOn: Date(), deletionDt: Date(), creationDt: Date())], status: "status_example") // CreateSettlementDto | 

// Create Settlement
PlatformAPI.settlementControllerCreate(platformId: platformId, createSettlementDto: createSettlementDto) { (response, error) in
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
 **platformId** | **Double** |  | 
 **createSettlementDto** | [**CreateSettlementDto**](CreateSettlementDto.md) |  | 

### Return type

[**SettlementDto**](SettlementDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **settlementControllerCreateAndUpdate**
```swift
    open class func settlementControllerCreateAndUpdate(createAndUpdateSettlementDto: [CreateAndUpdateSettlementDto], completion: @escaping (_ data: [SettlementDto]?, _ error: Error?) -> Void)
```

Create and update Asset Pairs

Creates or updates and returns multiple asset pairs.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let createAndUpdateSettlementDto = [CreateAndUpdateSettlementDto(recordId: 123, sourcePlatformId: 123, targetPlatformId: 123, creationDt: Date(), updatedOn: Date(), deletionDt: Date(), status: "status_example", orders: [OrderDto(recordId: 123, portfolioId: 123, userId: 123, executedBy: 123, pricePerUnit: "pricePerUnit_example", lpPricePerUnit: "lpPricePerUnit_example", stopPrice: "stopPrice_example", requestedQuantity: "requestedQuantity_example", filledQuantity: "filledQuantity_example", platformId: 123, platformFee: "platformFee_example", arkhonFeePercentage: "arkhonFeePercentage_example", arkhonSpreadPercentage: "arkhonSpreadPercentage_example", tierId: 123, arkhonSpread: "arkhonSpread_example", arkhonFee: "arkhonFee_example", totalFees: "totalFees_example", subtotal: "subtotal_example", totalConsideration: "totalConsideration_example", portfolio: PortfolioDto(recordId: 123, accountId: 123, account: AccountDto(recordId: 123, tradeFeePercentageOverride: "tradeFeePercentageOverride_example", slackChannelId: "slackChannelId_example", accountType: "accountType_example", accountRefId: "accountRefId_example", status: "status_example", portfolios: [nil], accountUsers: [AccountUserDto(recordId: 123, userId: 123, accountId: 123, updatedOn: Date(), deletionDt: Date(), creationDt: Date())], enrichments: [AccountOrPortfolioEnrichmentDto(value: AccountOrPortfolioEnrichmentDto_value(gains: PortfolioAssetEnrichmentDto_gains(hour: "hour_example", hourPercentage: "hourPercentage_example", day: "day_example", dayPercentage: "dayPercentage_example", week: "week_example", weekPercentage: "weekPercentage_example", month: "month_example", monthPercentage: "monthPercentage_example", year: "year_example", yearPercentage: "yearPercentage_example", allTime: "allTime_example", allTimePercentage: "allTimePercentage_example"), marketValue: "marketValue_example", base: "base_example", assets: [PortfolioAssetEnrichmentDto_assets_inner(quantity: "quantity_example", symbol: "symbol_example", marketPrice: "marketPrice_example", marketValue: "marketValue_example", percentAllocated: "percentAllocated_example", base: "base_example", gains: [GainEntryDto(value: "value_example", type: "type_example")])], topAccounts: [MarketValueStatisticDto(marketValue: "marketValue_example", accountMarketValuePercentOfAllAccounts: "accountMarketValuePercentOfAllAccounts_example", gains: Gains(hour: "hour_example", hourPercentage: "hourPercentage_example", day: "day_example", dayPercentage: "dayPercentage_example", week: "week_example", weekPercentage: "weekPercentage_example", month: "month_example", monthPercentage: "monthPercentage_example", year: "year_example", yearPercentage: "yearPercentage_example", allTime: "allTime_example", allTimePercentage: "allTimePercentage_example"), accountGains: [nil], accountRefId: "accountRefId_example")]), type: "type_example")], statistics: [nil], updatedOn: Date(), deletionDt: Date(), creationDt: Date()), type: "type_example", orders: [nil], transfers: [TransferDto(recordId: 123, portfolioId: 123, secondaryPortfolioId: 123, userId: 123, executedBy: 123, quantity: "quantity_example", platformId: 123, portfolio: nil, type: "type_example", currency: "currency_example", status: "status_example", platform: PlatformDto(recordId: 123, name: "name_example", isCustody: false, isVaspCapable: false, updatedOn: Date(), deletionDt: Date(), creationDt: Date()), platformRefId: "platformRefId_example", clientRefId: "clientRefId_example", receiptTime: Date(), creditTime: Date(), withdrawalTime: Date(), comment: "comment_example", version: 123, updatedOn: Date(), deletionDt: Date(), creationDt: Date())], enrichments: [nil], updatedOn: Date(), deletionDt: Date(), creationDt: Date()), baseToken: "baseToken_example", quoteToken: "quoteToken_example", tradedToken: "tradedToken_example", side: "side_example", startTime: Date(), endTime: Date(), strategy: "strategy_example", type: "type_example", platform: nil, platformRefId: "platformRefId_example", clientRefId: "clientRefId_example", platformFeeCurrency: "platformFeeCurrency_example", status: "status_example", arkhonFeeCurrency: "arkhonFeeCurrency_example", feeStatus: "feeStatus_example", feeComment: "feeComment_example", comment: "comment_example", settlementId: 123, description: "description_example", enrichments: OrderEnrichment(fiatFxOnRequestedBaseCurrency: "fiatFxOnRequestedBaseCurrency_example"), statistics: [AssetStatistic(type: "type_example", value: [AssetStatisticEntry(quantity: "quantity_example", currency: "currency_example")])], version: 123, updatedOn: Date(), deletionDt: Date(), creationDt: Date())])] // [CreateAndUpdateSettlementDto] | 

// Create and update Asset Pairs
PlatformAPI.settlementControllerCreateAndUpdate(createAndUpdateSettlementDto: createAndUpdateSettlementDto) { (response, error) in
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
 **createAndUpdateSettlementDto** | [**[CreateAndUpdateSettlementDto]**](CreateAndUpdateSettlementDto.md) |  | 

### Return type

[**[SettlementDto]**](SettlementDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **settlementControllerCreateBulk**
```swift
    open class func settlementControllerCreateBulk(platformId: Double, createSettlementDto: [CreateSettlementDto], completion: @escaping (_ data: [SettlementDto]?, _ error: Error?) -> Void)
```

Create multiple Settlements

Creates and returns multiple settlements.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let platformId = 987 // Double | 
let createSettlementDto = [CreateSettlementDto(sourcePlatformId: 123, targetPlatformId: 123, orders: [OrderDto(recordId: 123, portfolioId: 123, userId: 123, executedBy: 123, pricePerUnit: "pricePerUnit_example", lpPricePerUnit: "lpPricePerUnit_example", stopPrice: "stopPrice_example", requestedQuantity: "requestedQuantity_example", filledQuantity: "filledQuantity_example", platformId: 123, platformFee: "platformFee_example", arkhonFeePercentage: "arkhonFeePercentage_example", arkhonSpreadPercentage: "arkhonSpreadPercentage_example", tierId: 123, arkhonSpread: "arkhonSpread_example", arkhonFee: "arkhonFee_example", totalFees: "totalFees_example", subtotal: "subtotal_example", totalConsideration: "totalConsideration_example", portfolio: PortfolioDto(recordId: 123, accountId: 123, account: AccountDto(recordId: 123, tradeFeePercentageOverride: "tradeFeePercentageOverride_example", slackChannelId: "slackChannelId_example", accountType: "accountType_example", accountRefId: "accountRefId_example", status: "status_example", portfolios: [nil], accountUsers: [AccountUserDto(recordId: 123, userId: 123, accountId: 123, updatedOn: Date(), deletionDt: Date(), creationDt: Date())], enrichments: [AccountOrPortfolioEnrichmentDto(value: AccountOrPortfolioEnrichmentDto_value(gains: PortfolioAssetEnrichmentDto_gains(hour: "hour_example", hourPercentage: "hourPercentage_example", day: "day_example", dayPercentage: "dayPercentage_example", week: "week_example", weekPercentage: "weekPercentage_example", month: "month_example", monthPercentage: "monthPercentage_example", year: "year_example", yearPercentage: "yearPercentage_example", allTime: "allTime_example", allTimePercentage: "allTimePercentage_example"), marketValue: "marketValue_example", base: "base_example", assets: [PortfolioAssetEnrichmentDto_assets_inner(quantity: "quantity_example", symbol: "symbol_example", marketPrice: "marketPrice_example", marketValue: "marketValue_example", percentAllocated: "percentAllocated_example", base: "base_example", gains: [GainEntryDto(value: "value_example", type: "type_example")])], topAccounts: [MarketValueStatisticDto(marketValue: "marketValue_example", accountMarketValuePercentOfAllAccounts: "accountMarketValuePercentOfAllAccounts_example", gains: Gains(hour: "hour_example", hourPercentage: "hourPercentage_example", day: "day_example", dayPercentage: "dayPercentage_example", week: "week_example", weekPercentage: "weekPercentage_example", month: "month_example", monthPercentage: "monthPercentage_example", year: "year_example", yearPercentage: "yearPercentage_example", allTime: "allTime_example", allTimePercentage: "allTimePercentage_example"), accountGains: [nil], accountRefId: "accountRefId_example")]), type: "type_example")], statistics: [nil], updatedOn: Date(), deletionDt: Date(), creationDt: Date()), type: "type_example", orders: [nil], transfers: [TransferDto(recordId: 123, portfolioId: 123, secondaryPortfolioId: 123, userId: 123, executedBy: 123, quantity: "quantity_example", platformId: 123, portfolio: nil, type: "type_example", currency: "currency_example", status: "status_example", platform: PlatformDto(recordId: 123, name: "name_example", isCustody: false, isVaspCapable: false, updatedOn: Date(), deletionDt: Date(), creationDt: Date()), platformRefId: "platformRefId_example", clientRefId: "clientRefId_example", receiptTime: Date(), creditTime: Date(), withdrawalTime: Date(), comment: "comment_example", version: 123, updatedOn: Date(), deletionDt: Date(), creationDt: Date())], enrichments: [nil], updatedOn: Date(), deletionDt: Date(), creationDt: Date()), baseToken: "baseToken_example", quoteToken: "quoteToken_example", tradedToken: "tradedToken_example", side: "side_example", startTime: Date(), endTime: Date(), strategy: "strategy_example", type: "type_example", platform: nil, platformRefId: "platformRefId_example", clientRefId: "clientRefId_example", platformFeeCurrency: "platformFeeCurrency_example", status: "status_example", arkhonFeeCurrency: "arkhonFeeCurrency_example", feeStatus: "feeStatus_example", feeComment: "feeComment_example", comment: "comment_example", settlementId: 123, description: "description_example", enrichments: OrderEnrichment(fiatFxOnRequestedBaseCurrency: "fiatFxOnRequestedBaseCurrency_example"), statistics: [AssetStatistic(type: "type_example", value: [AssetStatisticEntry(quantity: "quantity_example", currency: "currency_example")])], version: 123, updatedOn: Date(), deletionDt: Date(), creationDt: Date())], status: "status_example")] // [CreateSettlementDto] | 

// Create multiple Settlements
PlatformAPI.settlementControllerCreateBulk(platformId: platformId, createSettlementDto: createSettlementDto) { (response, error) in
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
 **platformId** | **Double** |  | 
 **createSettlementDto** | [**[CreateSettlementDto]**](CreateSettlementDto.md) |  | 

### Return type

[**[SettlementDto]**](SettlementDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **settlementControllerDelete**
```swift
    open class func settlementControllerDelete(platformId: Double, recordId: Double, completion: @escaping (_ data: String?, _ error: Error?) -> Void)
```

Delete Settlement

Deletes single settlement.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let platformId = 987 // Double | 
let recordId = 987 // Double | 

// Delete Settlement
PlatformAPI.settlementControllerDelete(platformId: platformId, recordId: recordId) { (response, error) in
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
 **platformId** | **Double** |  | 
 **recordId** | **Double** |  | 

### Return type

**String**

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **settlementControllerFindAll**
```swift
    open class func settlementControllerFindAll(platformId: Double, page: Double, pageSize: Double, completion: @escaping (_ data: [SettlementDto]?, _ error: Error?) -> Void)
```

Get all Settlements

Returns all settlements to which the logged in user has access.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let platformId = 987 // Double | 
let page = 987 // Double | 
let pageSize = 987 // Double | 

// Get all Settlements
PlatformAPI.settlementControllerFindAll(platformId: platformId, page: page, pageSize: pageSize) { (response, error) in
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
 **platformId** | **Double** |  | 
 **page** | **Double** |  | 
 **pageSize** | **Double** |  | 

### Return type

[**[SettlementDto]**](SettlementDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **settlementControllerFindOne**
```swift
    open class func settlementControllerFindOne(platformId: Double, recordId: Double, completion: @escaping (_ data: SettlementDto?, _ error: Error?) -> Void)
```

Get single Settlement

Returns single settlement if the logged in user has access.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let platformId = 987 // Double | 
let recordId = 987 // Double | 

// Get single Settlement
PlatformAPI.settlementControllerFindOne(platformId: platformId, recordId: recordId) { (response, error) in
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
 **platformId** | **Double** |  | 
 **recordId** | **Double** |  | 

### Return type

[**SettlementDto**](SettlementDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **settlementControllerSearch**
```swift
    open class func settlementControllerSearch(platformId: Double, searchDto: SearchDto, completion: @escaping (_ data: [SettlementDto]?, _ error: Error?) -> Void)
```

Search Settlements

Returns matching settlements to which the logged in user has access.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let platformId = 987 // Double | 
let searchDto = SearchDto(orderOption: [OrderOption(field: "field_example", direction: "direction_example")], pageSize: 123, page: 123, enrichments: ["enrichments_example"], filterOptions: [FilterOptionDto(values: [FilterOptionDto_values_inner()], field: "field_example", _operator: "_operator_example", subFilters: [nil])], returnSoftDeletedEntities: false) // SearchDto | 

// Search Settlements
PlatformAPI.settlementControllerSearch(platformId: platformId, searchDto: searchDto) { (response, error) in
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
 **platformId** | **Double** |  | 
 **searchDto** | [**SearchDto**](SearchDto.md) |  | 

### Return type

[**[SettlementDto]**](SettlementDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **settlementControllerStatistics**
```swift
    open class func settlementControllerStatistics(platformId: Double, stats: [String], completion: @escaping (_ data: SettlementDto?, _ error: Error?) -> Void)
```

Settlement Statistics

Not supported.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let platformId = 987 // Double | 
let stats = ["inner_example"] // [String] | 

// Settlement Statistics
PlatformAPI.settlementControllerStatistics(platformId: platformId, stats: stats) { (response, error) in
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
 **platformId** | **Double** |  | 
 **stats** | [**[String]**](String.md) |  | 

### Return type

[**SettlementDto**](SettlementDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **settlementControllerUpdate**
```swift
    open class func settlementControllerUpdate(platformId: Double, recordId: Double, updateSettlementDto: UpdateSettlementDto, completion: @escaping (_ data: SettlementDto?, _ error: Error?) -> Void)
```

Update single Settlement

Updates and returns single settlement.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let platformId = 987 // Double | 
let recordId = 987 // Double | 
let updateSettlementDto = UpdateSettlementDto(recordId: 123, sourcePlatformId: 123, targetPlatformId: 123, status: "status_example", orders: [OrderDto(recordId: 123, portfolioId: 123, userId: 123, executedBy: 123, pricePerUnit: "pricePerUnit_example", lpPricePerUnit: "lpPricePerUnit_example", stopPrice: "stopPrice_example", requestedQuantity: "requestedQuantity_example", filledQuantity: "filledQuantity_example", platformId: 123, platformFee: "platformFee_example", arkhonFeePercentage: "arkhonFeePercentage_example", arkhonSpreadPercentage: "arkhonSpreadPercentage_example", tierId: 123, arkhonSpread: "arkhonSpread_example", arkhonFee: "arkhonFee_example", totalFees: "totalFees_example", subtotal: "subtotal_example", totalConsideration: "totalConsideration_example", portfolio: PortfolioDto(recordId: 123, accountId: 123, account: AccountDto(recordId: 123, tradeFeePercentageOverride: "tradeFeePercentageOverride_example", slackChannelId: "slackChannelId_example", accountType: "accountType_example", accountRefId: "accountRefId_example", status: "status_example", portfolios: [nil], accountUsers: [AccountUserDto(recordId: 123, userId: 123, accountId: 123, updatedOn: Date(), deletionDt: Date(), creationDt: Date())], enrichments: [AccountOrPortfolioEnrichmentDto(value: AccountOrPortfolioEnrichmentDto_value(gains: PortfolioAssetEnrichmentDto_gains(hour: "hour_example", hourPercentage: "hourPercentage_example", day: "day_example", dayPercentage: "dayPercentage_example", week: "week_example", weekPercentage: "weekPercentage_example", month: "month_example", monthPercentage: "monthPercentage_example", year: "year_example", yearPercentage: "yearPercentage_example", allTime: "allTime_example", allTimePercentage: "allTimePercentage_example"), marketValue: "marketValue_example", base: "base_example", assets: [PortfolioAssetEnrichmentDto_assets_inner(quantity: "quantity_example", symbol: "symbol_example", marketPrice: "marketPrice_example", marketValue: "marketValue_example", percentAllocated: "percentAllocated_example", base: "base_example", gains: [GainEntryDto(value: "value_example", type: "type_example")])], topAccounts: [MarketValueStatisticDto(marketValue: "marketValue_example", accountMarketValuePercentOfAllAccounts: "accountMarketValuePercentOfAllAccounts_example", gains: Gains(hour: "hour_example", hourPercentage: "hourPercentage_example", day: "day_example", dayPercentage: "dayPercentage_example", week: "week_example", weekPercentage: "weekPercentage_example", month: "month_example", monthPercentage: "monthPercentage_example", year: "year_example", yearPercentage: "yearPercentage_example", allTime: "allTime_example", allTimePercentage: "allTimePercentage_example"), accountGains: [nil], accountRefId: "accountRefId_example")]), type: "type_example")], statistics: [nil], updatedOn: Date(), deletionDt: Date(), creationDt: Date()), type: "type_example", orders: [nil], transfers: [TransferDto(recordId: 123, portfolioId: 123, secondaryPortfolioId: 123, userId: 123, executedBy: 123, quantity: "quantity_example", platformId: 123, portfolio: nil, type: "type_example", currency: "currency_example", status: "status_example", platform: PlatformDto(recordId: 123, name: "name_example", isCustody: false, isVaspCapable: false, updatedOn: Date(), deletionDt: Date(), creationDt: Date()), platformRefId: "platformRefId_example", clientRefId: "clientRefId_example", receiptTime: Date(), creditTime: Date(), withdrawalTime: Date(), comment: "comment_example", version: 123, updatedOn: Date(), deletionDt: Date(), creationDt: Date())], enrichments: [nil], updatedOn: Date(), deletionDt: Date(), creationDt: Date()), baseToken: "baseToken_example", quoteToken: "quoteToken_example", tradedToken: "tradedToken_example", side: "side_example", startTime: Date(), endTime: Date(), strategy: "strategy_example", type: "type_example", platform: nil, platformRefId: "platformRefId_example", clientRefId: "clientRefId_example", platformFeeCurrency: "platformFeeCurrency_example", status: "status_example", arkhonFeeCurrency: "arkhonFeeCurrency_example", feeStatus: "feeStatus_example", feeComment: "feeComment_example", comment: "comment_example", settlementId: 123, description: "description_example", enrichments: OrderEnrichment(fiatFxOnRequestedBaseCurrency: "fiatFxOnRequestedBaseCurrency_example"), statistics: [AssetStatistic(type: "type_example", value: [AssetStatisticEntry(quantity: "quantity_example", currency: "currency_example")])], version: 123, updatedOn: Date(), deletionDt: Date(), creationDt: Date())]) // UpdateSettlementDto | 

// Update single Settlement
PlatformAPI.settlementControllerUpdate(platformId: platformId, recordId: recordId, updateSettlementDto: updateSettlementDto) { (response, error) in
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
 **platformId** | **Double** |  | 
 **recordId** | **Double** |  | 
 **updateSettlementDto** | [**UpdateSettlementDto**](UpdateSettlementDto.md) |  | 

### Return type

[**SettlementDto**](SettlementDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **settlementControllerUpdateBulk**
```swift
    open class func settlementControllerUpdateBulk(platformId: Double, updateSettlementDto: [UpdateSettlementDto], completion: @escaping (_ data: [SettlementDto]?, _ error: Error?) -> Void)
```

Update multiple Settlements

Updates and returns multiple settlements.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let platformId = 987 // Double | 
let updateSettlementDto = [UpdateSettlementDto(recordId: 123, sourcePlatformId: 123, targetPlatformId: 123, status: "status_example", orders: [OrderDto(recordId: 123, portfolioId: 123, userId: 123, executedBy: 123, pricePerUnit: "pricePerUnit_example", lpPricePerUnit: "lpPricePerUnit_example", stopPrice: "stopPrice_example", requestedQuantity: "requestedQuantity_example", filledQuantity: "filledQuantity_example", platformId: 123, platformFee: "platformFee_example", arkhonFeePercentage: "arkhonFeePercentage_example", arkhonSpreadPercentage: "arkhonSpreadPercentage_example", tierId: 123, arkhonSpread: "arkhonSpread_example", arkhonFee: "arkhonFee_example", totalFees: "totalFees_example", subtotal: "subtotal_example", totalConsideration: "totalConsideration_example", portfolio: PortfolioDto(recordId: 123, accountId: 123, account: AccountDto(recordId: 123, tradeFeePercentageOverride: "tradeFeePercentageOverride_example", slackChannelId: "slackChannelId_example", accountType: "accountType_example", accountRefId: "accountRefId_example", status: "status_example", portfolios: [nil], accountUsers: [AccountUserDto(recordId: 123, userId: 123, accountId: 123, updatedOn: Date(), deletionDt: Date(), creationDt: Date())], enrichments: [AccountOrPortfolioEnrichmentDto(value: AccountOrPortfolioEnrichmentDto_value(gains: PortfolioAssetEnrichmentDto_gains(hour: "hour_example", hourPercentage: "hourPercentage_example", day: "day_example", dayPercentage: "dayPercentage_example", week: "week_example", weekPercentage: "weekPercentage_example", month: "month_example", monthPercentage: "monthPercentage_example", year: "year_example", yearPercentage: "yearPercentage_example", allTime: "allTime_example", allTimePercentage: "allTimePercentage_example"), marketValue: "marketValue_example", base: "base_example", assets: [PortfolioAssetEnrichmentDto_assets_inner(quantity: "quantity_example", symbol: "symbol_example", marketPrice: "marketPrice_example", marketValue: "marketValue_example", percentAllocated: "percentAllocated_example", base: "base_example", gains: [GainEntryDto(value: "value_example", type: "type_example")])], topAccounts: [MarketValueStatisticDto(marketValue: "marketValue_example", accountMarketValuePercentOfAllAccounts: "accountMarketValuePercentOfAllAccounts_example", gains: Gains(hour: "hour_example", hourPercentage: "hourPercentage_example", day: "day_example", dayPercentage: "dayPercentage_example", week: "week_example", weekPercentage: "weekPercentage_example", month: "month_example", monthPercentage: "monthPercentage_example", year: "year_example", yearPercentage: "yearPercentage_example", allTime: "allTime_example", allTimePercentage: "allTimePercentage_example"), accountGains: [nil], accountRefId: "accountRefId_example")]), type: "type_example")], statistics: [nil], updatedOn: Date(), deletionDt: Date(), creationDt: Date()), type: "type_example", orders: [nil], transfers: [TransferDto(recordId: 123, portfolioId: 123, secondaryPortfolioId: 123, userId: 123, executedBy: 123, quantity: "quantity_example", platformId: 123, portfolio: nil, type: "type_example", currency: "currency_example", status: "status_example", platform: PlatformDto(recordId: 123, name: "name_example", isCustody: false, isVaspCapable: false, updatedOn: Date(), deletionDt: Date(), creationDt: Date()), platformRefId: "platformRefId_example", clientRefId: "clientRefId_example", receiptTime: Date(), creditTime: Date(), withdrawalTime: Date(), comment: "comment_example", version: 123, updatedOn: Date(), deletionDt: Date(), creationDt: Date())], enrichments: [nil], updatedOn: Date(), deletionDt: Date(), creationDt: Date()), baseToken: "baseToken_example", quoteToken: "quoteToken_example", tradedToken: "tradedToken_example", side: "side_example", startTime: Date(), endTime: Date(), strategy: "strategy_example", type: "type_example", platform: nil, platformRefId: "platformRefId_example", clientRefId: "clientRefId_example", platformFeeCurrency: "platformFeeCurrency_example", status: "status_example", arkhonFeeCurrency: "arkhonFeeCurrency_example", feeStatus: "feeStatus_example", feeComment: "feeComment_example", comment: "comment_example", settlementId: 123, description: "description_example", enrichments: OrderEnrichment(fiatFxOnRequestedBaseCurrency: "fiatFxOnRequestedBaseCurrency_example"), statistics: [AssetStatistic(type: "type_example", value: [AssetStatisticEntry(quantity: "quantity_example", currency: "currency_example")])], version: 123, updatedOn: Date(), deletionDt: Date(), creationDt: Date())])] // [UpdateSettlementDto] | 

// Update multiple Settlements
PlatformAPI.settlementControllerUpdateBulk(platformId: platformId, updateSettlementDto: updateSettlementDto) { (response, error) in
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
 **platformId** | **Double** |  | 
 **updateSettlementDto** | [**[UpdateSettlementDto]**](UpdateSettlementDto.md) |  | 

### Return type

[**[SettlementDto]**](SettlementDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

