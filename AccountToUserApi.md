# AccountToUserAPI

All URIs are relative to *https://backend.arkhon.test.arkhon.digital*

Method | HTTP request | Description
------------- | ------------- | -------------
[**accountUserControllerCreate**](AccountToUserAPI.md#accountusercontrollercreate) | **POST** /v1/accounts/{accountId}/users/{userIds} | Attach user(s) to account
[**accountUserControllerFindAll**](AccountToUserAPI.md#accountusercontrollerfindall) | **GET** /v1/accounts/{accountId}/users | Find all users attached to account
[**accountUserControllerFindOne**](AccountToUserAPI.md#accountusercontrollerfindone) | **GET** /v1/accounts/{accountId}/users/{userId} | Find user attached to account
[**accountUserControllerRemove**](AccountToUserAPI.md#accountusercontrollerremove) | **DELETE** /v1/accounts/{accountId}/users/{userIds} | Detaches user(s) from account
[**userAccountControllerFindAll**](AccountToUserAPI.md#useraccountcontrollerfindall) | **GET** /v1/users/{userIds}/accounts | Find all accounts attached to user(s)


# **accountUserControllerCreate**
```swift
    open class func accountUserControllerCreate(accountId: Double, userIds: AnyCodable, body: AnyCodable, completion: @escaping (_ data: [AccountUserDto]?, _ error: Error?) -> Void)
```

Attach user(s) to account

Attaches one or more users to the given account

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let accountId = 987 // Double | 
let userIds = 987 // AnyCodable | 
let body = "TODO" // AnyCodable | 

// Attach user(s) to account
AccountToUserAPI.accountUserControllerCreate(accountId: accountId, userIds: userIds, body: body) { (response, error) in
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
 **userIds** | [**AnyCodable**](.md) |  | 
 **body** | **AnyCodable** |  | 

### Return type

[**[AccountUserDto]**](AccountUserDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **accountUserControllerFindAll**
```swift
    open class func accountUserControllerFindAll(accountId: Double, completion: @escaping (_ data: [AccountUserDto]?, _ error: Error?) -> Void)
```

Find all users attached to account

Returns all account-to-user mappings for the given account.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let accountId = 987 // Double | 

// Find all users attached to account
AccountToUserAPI.accountUserControllerFindAll(accountId: accountId) { (response, error) in
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

[**[AccountUserDto]**](AccountUserDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **accountUserControllerFindOne**
```swift
    open class func accountUserControllerFindOne(accountId: Double, userId: Double, completion: @escaping (_ data: AccountUserDto?, _ error: Error?) -> Void)
```

Find user attached to account

Returns account-to-user mapping for the given account and user, if it exists.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let accountId = 987 // Double | 
let userId = 987 // Double | 

// Find user attached to account
AccountToUserAPI.accountUserControllerFindOne(accountId: accountId, userId: userId) { (response, error) in
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
 **userId** | **Double** |  | 

### Return type

[**AccountUserDto**](AccountUserDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **accountUserControllerRemove**
```swift
    open class func accountUserControllerRemove(accountId: Double, userIds: AnyCodable, completion: @escaping (_ data: Double?, _ error: Error?) -> Void)
```

Detaches user(s) from account

Detaches one or more users from the given account

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let accountId = 987 // Double | 
let userIds = 987 // AnyCodable | 

// Detaches user(s) from account
AccountToUserAPI.accountUserControllerRemove(accountId: accountId, userIds: userIds) { (response, error) in
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
 **userIds** | [**AnyCodable**](.md) |  | 

### Return type

**Double**

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **userAccountControllerFindAll**
```swift
    open class func userAccountControllerFindAll(userIds: AnyCodable, completion: @escaping (_ data: [AccountUserDto]?, _ error: Error?) -> Void)
```

Find all accounts attached to user(s)

Returns account-to-user mappings for the given user(s).

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let userIds = 987 // AnyCodable | 

// Find all accounts attached to user(s)
AccountToUserAPI.userAccountControllerFindAll(userIds: userIds) { (response, error) in
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
 **userIds** | [**AnyCodable**](.md) |  | 

### Return type

[**[AccountUserDto]**](AccountUserDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

