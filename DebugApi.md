# DebugAPI

All URIs are relative to *https://backend.arkhon.test.arkhon.digital*

Method | HTTP request | Description
------------- | ------------- | -------------
[**deletedUserControllerRemoveDeletedUsers**](DebugAPI.md#deletedusercontrollerremovedeletedusers) | **DELETE** /v1/accounts/{accountId}/users/removeDeletedUsers | Remove Account-to-User links involving deleted users
[**featureFlagControllerGetAll**](DebugAPI.md#featureflagcontrollergetall) | **GET** /v1/featureFlags | Get all Feature Flags
[**featureFlagControllerGetOne**](DebugAPI.md#featureflagcontrollergetone) | **GET** /v1/featureFlags/{settingKey} | Get single Feature Flag
[**transactionListenerControllerRecalculatePlatformBalance**](DebugAPI.md#transactionlistenercontrollerrecalculateplatformbalance) | **POST** /v1/platforms/{platformId}/assets/recalculateBalance | Recalculate Platform Balance
[**transactionListenerControllerRecalculatePortfolioBalance**](DebugAPI.md#transactionlistenercontrollerrecalculateportfoliobalance) | **POST** /v1/accounts/{accountId}/portfolios/{recordId}/recalculateBalance | Recalculate Portfolio Balance
[**versionControllerGetApplicationVersion**](DebugAPI.md#versioncontrollergetapplicationversion) | **GET** /v1/version | Get Application Version


# **deletedUserControllerRemoveDeletedUsers**
```swift
    open class func deletedUserControllerRemoveDeletedUsers(accountId: Double, completion: @escaping (_ data: String?, _ error: Error?) -> Void)
```

Remove Account-to-User links involving deleted users

Removes any account to user links that involve deleted users. Calling this endpoint should not be necessary thanks to our \"Deleted Users Listener\" but is provided for debugging purposes.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let accountId = 987 // Double | 

// Remove Account-to-User links involving deleted users
DebugAPI.deletedUserControllerRemoveDeletedUsers(accountId: accountId) { (response, error) in
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

**String**

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **featureFlagControllerGetAll**
```swift
    open class func featureFlagControllerGetAll(completion: @escaping (_ data: [FeatureFlagDto]?, _ error: Error?) -> Void)
```

Get all Feature Flags

Returns all feature flags and their current values.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient


// Get all Feature Flags
DebugAPI.featureFlagControllerGetAll() { (response, error) in
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
This endpoint does not need any parameter.

### Return type

[**[FeatureFlagDto]**](FeatureFlagDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **featureFlagControllerGetOne**
```swift
    open class func featureFlagControllerGetOne(settingKey: String, completion: @escaping (_ data: FeatureFlagDto?, _ error: Error?) -> Void)
```

Get single Feature Flag

Returns single feature flags and its current value.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let settingKey = "settingKey_example" // String | 

// Get single Feature Flag
DebugAPI.featureFlagControllerGetOne(settingKey: settingKey) { (response, error) in
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
 **settingKey** | **String** |  | 

### Return type

[**FeatureFlagDto**](FeatureFlagDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **transactionListenerControllerRecalculatePlatformBalance**
```swift
    open class func transactionListenerControllerRecalculatePlatformBalance(platformId: Double, body: AnyCodable, completion: @escaping (_ data: String?, _ error: Error?) -> Void)
```

Recalculate Platform Balance

Recalculates the asset balances of a platform by walking through all transactions since the beginning of time and summing them up. This endpoint can be used if for whatever reason the platform asset cache is incorrect.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let platformId = 987 // Double | 
let body = "TODO" // AnyCodable | 

// Recalculate Platform Balance
DebugAPI.transactionListenerControllerRecalculatePlatformBalance(platformId: platformId, body: body) { (response, error) in
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
 **body** | **AnyCodable** |  | 

### Return type

**String**

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **transactionListenerControllerRecalculatePortfolioBalance**
```swift
    open class func transactionListenerControllerRecalculatePortfolioBalance(accountId: Double, recordId: Double, body: AnyCodable, completion: @escaping (_ data: String?, _ error: Error?) -> Void)
```

Recalculate Portfolio Balance

Recalculates the asset balances of a portfolio by walking through all transactions since the beginning of time and summing them up. This endpoint can be used if for whatever reason the portfolio asset cache is incorrect.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let accountId = 987 // Double | 
let recordId = 987 // Double | 
let body = "TODO" // AnyCodable | 

// Recalculate Portfolio Balance
DebugAPI.transactionListenerControllerRecalculatePortfolioBalance(accountId: accountId, recordId: recordId, body: body) { (response, error) in
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
 **recordId** | **Double** |  | 
 **body** | **AnyCodable** |  | 

### Return type

**String**

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **versionControllerGetApplicationVersion**
```swift
    open class func versionControllerGetApplicationVersion(completion: @escaping (_ data: String?, _ error: Error?) -> Void)
```

Get Application Version

Returns athe version of the application, e.g. \"1.123.45\".

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient


// Get Application Version
DebugAPI.versionControllerGetApplicationVersion() { (response, error) in
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
This endpoint does not need any parameter.

### Return type

**String**

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

