# AccountAPI

All URIs are relative to *https://backend.arkhon.test.arkhon.digital*

Method | HTTP request | Description
------------- | ------------- | -------------
[**accountControllerComputeAggregates**](AccountAPI.md#accountcontrollercomputeaggregates) | **POST** /v1/accounts/computeAggregates | Get Aggregates across Accounts
[**accountControllerCount**](AccountAPI.md#accountcontrollercount) | **POST** /v1/accounts/count | Count all Accounts
[**accountControllerCreate**](AccountAPI.md#accountcontrollercreate) | **POST** /v1/accounts | Create a new Account
[**accountControllerCreateAndUpdate**](AccountAPI.md#accountcontrollercreateandupdate) | **POST** /v1/accounts/createAndUpdate | Create and update Accounts
[**accountControllerCreateBulk**](AccountAPI.md#accountcontrollercreatebulk) | **POST** /v1/accounts/bulk | Create multiple new Accounts
[**accountControllerDelete**](AccountAPI.md#accountcontrollerdelete) | **DELETE** /v1/accounts/{recordId} | Deletes single Account
[**accountControllerFindAll**](AccountAPI.md#accountcontrollerfindall) | **GET** /v1/accounts | Get all Accounts
[**accountControllerFindOne**](AccountAPI.md#accountcontrollerfindone) | **GET** /v1/accounts/{recordId} | Find single Accounts
[**accountControllerGetFeeTierByAccount**](AccountAPI.md#accountcontrollergetfeetierbyaccount) | **GET** /v1/accounts/{accountId}/feeTier | Fetch Fee tier of Account
[**accountControllerSearch**](AccountAPI.md#accountcontrollersearch) | **POST** /v1/accounts/search | Search all Accounts
[**accountControllerStatistics**](AccountAPI.md#accountcontrollerstatistics) | **GET** /v1/accounts/statistics | Get Statistics across all Accounts
[**accountControllerUpdate**](AccountAPI.md#accountcontrollerupdate) | **PATCH** /v1/accounts/{recordId} | Updates single Account
[**accountControllerUpdateBulk**](AccountAPI.md#accountcontrollerupdatebulk) | **PATCH** /v1/accounts/bulk | Updates multiple Accounts


# **accountControllerComputeAggregates**
```swift
    open class func accountControllerComputeAggregates(aggregates: [String], searchDto: SearchDto, completion: @escaping (_ data: [AggregateDto]?, _ error: Error?) -> Void)
```

Get Aggregates across Accounts

Returns desired aggregate(s) across accounts to which the logged in user has searched & has access.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let aggregates = ["inner_example"] // [String] | Specifies aggregates to be evaluated across accounts returned by search body.
let searchDto = SearchDto(orderOption: [OrderOption(field: "field_example", direction: "direction_example")], pageSize: 123, page: 123, enrichments: ["enrichments_example"], filterOptions: [FilterOptionDto(values: [FilterOptionDto_values_inner()], field: "field_example", _operator: "_operator_example", subFilters: [nil])], returnSoftDeletedEntities: false) // SearchDto | 

// Get Aggregates across Accounts
AccountAPI.accountControllerComputeAggregates(aggregates: aggregates, searchDto: searchDto) { (response, error) in
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
 **aggregates** | [**[String]**](String.md) | Specifies aggregates to be evaluated across accounts returned by search body. | 
 **searchDto** | [**SearchDto**](SearchDto.md) |  | 

### Return type

[**[AggregateDto]**](AggregateDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **accountControllerCount**
```swift
    open class func accountControllerCount(countDto: CountDto, completion: @escaping (_ data: Double?, _ error: Error?) -> Void)
```

Count all Accounts

Returns count of matching accounts to which the logged in user has access.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let countDto = CountDto(filterOptions: [FilterOptionDto(values: [FilterOptionDto_values_inner()], field: "field_example", _operator: "_operator_example", subFilters: [nil])], returnSoftDeletedEntities: false) // CountDto | 

// Count all Accounts
AccountAPI.accountControllerCount(countDto: countDto) { (response, error) in
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

# **accountControllerCreate**
```swift
    open class func accountControllerCreate(createAccountDto: CreateAccountDto, completion: @escaping (_ data: AccountDto?, _ error: Error?) -> Void)
```

Create a new Account

Creates and returns new account. Also adds the requesting user to the newly added account.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let createAccountDto = CreateAccountDto(tradeFeePercentageOverride: "tradeFeePercentageOverride_example", slackChannelId: "slackChannelId_example", accountType: "accountType_example", accountRefId: "accountRefId_example", status: "status_example") // CreateAccountDto | 

// Create a new Account
AccountAPI.accountControllerCreate(createAccountDto: createAccountDto) { (response, error) in
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
 **createAccountDto** | [**CreateAccountDto**](CreateAccountDto.md) |  | 

### Return type

[**AccountDto**](AccountDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **accountControllerCreateAndUpdate**
```swift
    open class func accountControllerCreateAndUpdate(createAndUpdateAccountDto: [CreateAndUpdateAccountDto], completion: @escaping (_ data: [AccountDto]?, _ error: Error?) -> Void)
```

Create and update Accounts

Creates or updates and returns multiple accounts.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let createAndUpdateAccountDto = [CreateAndUpdateAccountDto(recordId: 123, tradeFeePercentageOverride: "tradeFeePercentageOverride_example", slackChannelId: "slackChannelId_example", creationDt: Date(), updatedOn: Date(), deletionDt: Date(), accountType: "accountType_example", accountRefId: "accountRefId_example", status: "status_example", portfolios: [PortfolioDto(recordId: 123, accountId: 123, account: AccountDto(recordId: 123, tradeFeePercentageOverride: "tradeFeePercentageOverride_example", slackChannelId: "slackChannelId_example", accountType: "accountType_example", accountRefId: "accountRefId_example", status: "status_example", portfolios: [nil], accountUsers: [AccountUserDto(recordId: 123, userId: 123, accountId: 123, updatedOn: Date(), deletionDt: Date(), creationDt: Date())], enrichments: [AccountOrPortfolioEnrichmentDto(value: AccountOrPortfolioEnrichmentDto_value(gains: PortfolioAssetEnrichmentDto_gains(hour: "hour_example", hourPercentage: "hourPercentage_example", day: "day_example", dayPercentage: "dayPercentage_example", week: "week_example", weekPercentage: "weekPercentage_example", month: "month_example", monthPercentage: "monthPercentage_example", year: "year_example", yearPercentage: "yearPercentage_example", allTime: "allTime_example", allTimePercentage: "allTimePercentage_example"), marketValue: "marketValue_example", base: "base_example", assets: [PortfolioAssetEnrichmentDto_assets_inner(quantity: "quantity_example", symbol: "symbol_example", marketPrice: "marketPrice_example", marketValue: "marketValue_example", percentAllocated: "percentAllocated_example", base: "base_example", gains: [GainEntryDto(value: "value_example", type: "type_example")])], topAccounts: [MarketValueStatisticDto(marketValue: "marketValue_example", accountMarketValuePercentOfAllAccounts: "accountMarketValuePercentOfAllAccounts_example", gains: Gains(hour: "hour_example", hourPercentage: "hourPercentage_example", day: "day_example", dayPercentage: "dayPercentage_example", week: "week_example", weekPercentage: "weekPercentage_example", month: "month_example", monthPercentage: "monthPercentage_example", year: "year_example", yearPercentage: "yearPercentage_example", allTime: "allTime_example", allTimePercentage: "allTimePercentage_example"), accountGains: [nil], accountRefId: "accountRefId_example")]), type: "type_example")], statistics: [nil], updatedOn: Date(), deletionDt: Date(), creationDt: Date()), type: "type_example", orders: [OrderDto(recordId: 123, portfolioId: 123, userId: 123, executedBy: 123, pricePerUnit: "pricePerUnit_example", lpPricePerUnit: "lpPricePerUnit_example", stopPrice: "stopPrice_example", requestedQuantity: "requestedQuantity_example", filledQuantity: "filledQuantity_example", platformId: 123, platformFee: "platformFee_example", arkhonFeePercentage: "arkhonFeePercentage_example", arkhonSpreadPercentage: "arkhonSpreadPercentage_example", tierId: 123, arkhonSpread: "arkhonSpread_example", arkhonFee: "arkhonFee_example", totalFees: "totalFees_example", subtotal: "subtotal_example", totalConsideration: "totalConsideration_example", portfolio: nil, baseToken: "baseToken_example", quoteToken: "quoteToken_example", tradedToken: "tradedToken_example", side: "side_example", startTime: Date(), endTime: Date(), strategy: "strategy_example", type: "type_example", platform: PlatformDto(recordId: 123, name: "name_example", isCustody: false, isVaspCapable: false, updatedOn: Date(), deletionDt: Date(), creationDt: Date()), platformRefId: "platformRefId_example", clientRefId: "clientRefId_example", platformFeeCurrency: "platformFeeCurrency_example", status: "status_example", arkhonFeeCurrency: "arkhonFeeCurrency_example", feeStatus: "feeStatus_example", feeComment: "feeComment_example", comment: "comment_example", settlementId: 123, description: "description_example", enrichments: OrderEnrichment(fiatFxOnRequestedBaseCurrency: "fiatFxOnRequestedBaseCurrency_example"), statistics: [AssetStatistic(type: "type_example", value: [AssetStatisticEntry(quantity: "quantity_example", currency: "currency_example")])], version: 123, updatedOn: Date(), deletionDt: Date(), creationDt: Date())], transfers: [TransferDto(recordId: 123, portfolioId: 123, secondaryPortfolioId: 123, userId: 123, executedBy: 123, quantity: "quantity_example", platformId: 123, portfolio: nil, type: "type_example", currency: "currency_example", status: "status_example", platform: nil, platformRefId: "platformRefId_example", clientRefId: "clientRefId_example", receiptTime: Date(), creditTime: Date(), withdrawalTime: Date(), comment: "comment_example", version: 123, updatedOn: Date(), deletionDt: Date(), creationDt: Date())], enrichments: [nil], updatedOn: Date(), deletionDt: Date(), creationDt: Date())], accountUsers: [nil], enrichments: [nil], statistics: [nil])] // [CreateAndUpdateAccountDto] | 

// Create and update Accounts
AccountAPI.accountControllerCreateAndUpdate(createAndUpdateAccountDto: createAndUpdateAccountDto) { (response, error) in
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
 **createAndUpdateAccountDto** | [**[CreateAndUpdateAccountDto]**](CreateAndUpdateAccountDto.md) |  | 

### Return type

[**[AccountDto]**](AccountDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **accountControllerCreateBulk**
```swift
    open class func accountControllerCreateBulk(createAccountDto: [CreateAccountDto], completion: @escaping (_ data: [AccountDto]?, _ error: Error?) -> Void)
```

Create multiple new Accounts

Creates and returns new accounts.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let createAccountDto = [CreateAccountDto(tradeFeePercentageOverride: "tradeFeePercentageOverride_example", slackChannelId: "slackChannelId_example", accountType: "accountType_example", accountRefId: "accountRefId_example", status: "status_example")] // [CreateAccountDto] | 

// Create multiple new Accounts
AccountAPI.accountControllerCreateBulk(createAccountDto: createAccountDto) { (response, error) in
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
 **createAccountDto** | [**[CreateAccountDto]**](CreateAccountDto.md) |  | 

### Return type

[**[AccountDto]**](AccountDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **accountControllerDelete**
```swift
    open class func accountControllerDelete(recordId: Double, completion: @escaping (_ data: String?, _ error: Error?) -> Void)
```

Deletes single Account

Deletes account identified by :recordId, if it exists.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let recordId = 987 // Double | 

// Deletes single Account
AccountAPI.accountControllerDelete(recordId: recordId) { (response, error) in
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

# **accountControllerFindAll**
```swift
    open class func accountControllerFindAll(page: Double, pageSize: Double, withPortfolios: Bool? = nil, withAccountUserLinks: Bool? = nil, completion: @escaping (_ data: [AccountDto]?, _ error: Error?) -> Void)
```

Get all Accounts

Returns all accounts to which the logged in user has access.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let page = 987 // Double | 
let pageSize = 987 // Double | 
let withPortfolios = true // Bool |  (optional)
let withAccountUserLinks = true // Bool |  (optional)

// Get all Accounts
AccountAPI.accountControllerFindAll(page: page, pageSize: pageSize, withPortfolios: withPortfolios, withAccountUserLinks: withAccountUserLinks) { (response, error) in
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
 **withPortfolios** | **Bool** |  | [optional] 
 **withAccountUserLinks** | **Bool** |  | [optional] 

### Return type

[**[AccountDto]**](AccountDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **accountControllerFindOne**
```swift
    open class func accountControllerFindOne(recordId: Double, withPortfolios: Bool? = nil, withAccountUserLinks: Bool? = nil, enrichments: [String]? = nil, completion: @escaping (_ data: AccountDto?, _ error: Error?) -> Void)
```

Find single Accounts

Returns matching account if which the logged in user has access.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let recordId = 987 // Double | 
let withPortfolios = true // Bool |  (optional)
let withAccountUserLinks = true // Bool |  (optional)
let enrichments = ["inner_example"] // [String] | Specifies additional enrichments to be applied to the account. (optional)

// Find single Accounts
AccountAPI.accountControllerFindOne(recordId: recordId, withPortfolios: withPortfolios, withAccountUserLinks: withAccountUserLinks, enrichments: enrichments) { (response, error) in
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
 **withPortfolios** | **Bool** |  | [optional] 
 **withAccountUserLinks** | **Bool** |  | [optional] 
 **enrichments** | [**[String]**](String.md) | Specifies additional enrichments to be applied to the account. | [optional] 

### Return type

[**AccountDto**](AccountDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **accountControllerGetFeeTierByAccount**
```swift
    open class func accountControllerGetFeeTierByAccount(accountId: Double, completion: @escaping (_ data: TierDto?, _ error: Error?) -> Void)
```

Fetch Fee tier of Account

Returns the fee tier of a given account.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let accountId = 987 // Double | 

// Fetch Fee tier of Account
AccountAPI.accountControllerGetFeeTierByAccount(accountId: accountId) { (response, error) in
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

### Return type

[**TierDto**](TierDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **accountControllerSearch**
```swift
    open class func accountControllerSearch(searchDto: SearchDto, withPortfolios: Bool? = nil, withAccountUserLinks: Bool? = nil, completion: @escaping (_ data: [AccountDto]?, _ error: Error?) -> Void)
```

Search all Accounts

Returns matching accounts to which the logged in user has access.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let searchDto = SearchDto(orderOption: [OrderOption(field: "field_example", direction: "direction_example")], pageSize: 123, page: 123, enrichments: ["enrichments_example"], filterOptions: [FilterOptionDto(values: [FilterOptionDto_values_inner()], field: "field_example", _operator: "_operator_example", subFilters: [nil])], returnSoftDeletedEntities: false) // SearchDto | 
let withPortfolios = true // Bool |  (optional)
let withAccountUserLinks = true // Bool |  (optional)

// Search all Accounts
AccountAPI.accountControllerSearch(searchDto: searchDto, withPortfolios: withPortfolios, withAccountUserLinks: withAccountUserLinks) { (response, error) in
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
 **withPortfolios** | **Bool** |  | [optional] 
 **withAccountUserLinks** | **Bool** |  | [optional] 

### Return type

[**[AccountDto]**](AccountDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **accountControllerStatistics**
```swift
    open class func accountControllerStatistics(stats: [String], completion: @escaping (_ data: AccountDto?, _ error: Error?) -> Void)
```

Get Statistics across all Accounts

Returns desired statistic(s) across accounts to which the logged in user has access.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let stats = ["inner_example"] // [String] | Specifies statistics to be evaluated across accounts.

// Get Statistics across all Accounts
AccountAPI.accountControllerStatistics(stats: stats) { (response, error) in
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
 **stats** | [**[String]**](String.md) | Specifies statistics to be evaluated across accounts. | 

### Return type

[**AccountDto**](AccountDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **accountControllerUpdate**
```swift
    open class func accountControllerUpdate(recordId: Double, updateAccountDto: UpdateAccountDto, completion: @escaping (_ data: AccountDto?, _ error: Error?) -> Void)
```

Updates single Account

Updates and returns account identified by :recordId

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let recordId = 987 // Double | 
let updateAccountDto = UpdateAccountDto(recordId: 123, tradeFeePercentageOverride: "tradeFeePercentageOverride_example", slackChannelId: "slackChannelId_example", accountType: "accountType_example", accountRefId: "accountRefId_example", status: "status_example") // UpdateAccountDto | 

// Updates single Account
AccountAPI.accountControllerUpdate(recordId: recordId, updateAccountDto: updateAccountDto) { (response, error) in
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
 **updateAccountDto** | [**UpdateAccountDto**](UpdateAccountDto.md) |  | 

### Return type

[**AccountDto**](AccountDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **accountControllerUpdateBulk**
```swift
    open class func accountControllerUpdateBulk(updateAccountDto: [UpdateAccountDto], completion: @escaping (_ data: [AccountDto]?, _ error: Error?) -> Void)
```

Updates multiple Accounts

Updates and returns accounts.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let updateAccountDto = [UpdateAccountDto(recordId: 123, tradeFeePercentageOverride: "tradeFeePercentageOverride_example", slackChannelId: "slackChannelId_example", accountType: "accountType_example", accountRefId: "accountRefId_example", status: "status_example")] // [UpdateAccountDto] | 

// Updates multiple Accounts
AccountAPI.accountControllerUpdateBulk(updateAccountDto: updateAccountDto) { (response, error) in
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
 **updateAccountDto** | [**[UpdateAccountDto]**](UpdateAccountDto.md) |  | 

### Return type

[**[AccountDto]**](AccountDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

