# PortfolioAPI

All URIs are relative to *https://backend.arkhon.test.arkhon.digital*

Method | HTTP request | Description
------------- | ------------- | -------------
[**accountPortfoliosControllerCreate**](PortfolioAPI.md#accountportfolioscontrollercreate) | **POST** /v1/accounts/{accountId}/portfolios | Create Portfolio
[**accountPortfoliosControllerDelete**](PortfolioAPI.md#accountportfolioscontrollerdelete) | **DELETE** /v1/accounts/{accountId}/portfolios/{recordId} | Delete Portfolio
[**accountPortfoliosControllerFindAll**](PortfolioAPI.md#accountportfolioscontrollerfindall) | **GET** /v1/accounts/{accountId}/portfolios | Get all Portfolios
[**accountPortfoliosControllerFindOne**](PortfolioAPI.md#accountportfolioscontrollerfindone) | **GET** /v1/accounts/{accountId}/portfolios/{recordId} | Get single Portfolio
[**accountPortfoliosControllerUpdate**](PortfolioAPI.md#accountportfolioscontrollerupdate) | **PATCH** /v1/accounts/{accountId}/portfolios/{recordId} | Update Portfolio
[**portfolioControllerFindOne**](PortfolioAPI.md#portfoliocontrollerfindone) | **GET** /v1/portfolios/{recordId} | Get single Portfolio


# **accountPortfoliosControllerCreate**
```swift
    open class func accountPortfoliosControllerCreate(accountId: Double, createPortfolioDto: CreatePortfolioDto, completion: @escaping (_ data: PortfolioDto?, _ error: Error?) -> Void)
```

Create Portfolio

Creates and returns new portfolio for an account.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let accountId = 987 // Double | 
let createPortfolioDto = CreatePortfolioDto(accountId: 123, type: "type_example") // CreatePortfolioDto | 

// Create Portfolio
PortfolioAPI.accountPortfoliosControllerCreate(accountId: accountId, createPortfolioDto: createPortfolioDto) { (response, error) in
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
 **createPortfolioDto** | [**CreatePortfolioDto**](CreatePortfolioDto.md) |  | 

### Return type

[**PortfolioDto**](PortfolioDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **accountPortfoliosControllerDelete**
```swift
    open class func accountPortfoliosControllerDelete(accountId: Double, recordId: Double, completion: @escaping (_ data: String?, _ error: Error?) -> Void)
```

Delete Portfolio

Deletes a portfolio of an account.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let accountId = 987 // Double | 
let recordId = 987 // Double | 

// Delete Portfolio
PortfolioAPI.accountPortfoliosControllerDelete(accountId: accountId, recordId: recordId) { (response, error) in
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

### Return type

**String**

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **accountPortfoliosControllerFindAll**
```swift
    open class func accountPortfoliosControllerFindAll(accountId: Double, enrichments: [String], completion: @escaping (_ data: [PortfolioDto]?, _ error: Error?) -> Void)
```

Get all Portfolios

Returns all portfolios of an account.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let accountId = 987 // Double | 
let enrichments = ["inner_example"] // [String] | 

// Get all Portfolios
PortfolioAPI.accountPortfoliosControllerFindAll(accountId: accountId, enrichments: enrichments) { (response, error) in
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
 **enrichments** | [**[String]**](String.md) |  | 

### Return type

[**[PortfolioDto]**](PortfolioDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **accountPortfoliosControllerFindOne**
```swift
    open class func accountPortfoliosControllerFindOne(recordId: Double, accountId: Double, enrichments: [String]? = nil, completion: @escaping (_ data: PortfolioDto?, _ error: Error?) -> Void)
```

Get single Portfolio

Returns single portfolio of an account.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let recordId = 987 // Double | 
let accountId = 987 // Double | 
let enrichments = ["inner_example"] // [String] | Specifies additional enrichments, these are only supported on some entities and vary from entity to entity. (optional)

// Get single Portfolio
PortfolioAPI.accountPortfoliosControllerFindOne(recordId: recordId, accountId: accountId, enrichments: enrichments) { (response, error) in
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
 **accountId** | **Double** |  | 
 **enrichments** | [**[String]**](String.md) | Specifies additional enrichments, these are only supported on some entities and vary from entity to entity. | [optional] 

### Return type

[**PortfolioDto**](PortfolioDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **accountPortfoliosControllerUpdate**
```swift
    open class func accountPortfoliosControllerUpdate(accountId: Double, recordId: Double, updatePortfolioDto: UpdatePortfolioDto, completion: @escaping (_ data: PortfolioDto?, _ error: Error?) -> Void)
```

Update Portfolio

Updates and returns a portfolio of an account.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let accountId = 987 // Double | 
let recordId = 987 // Double | 
let updatePortfolioDto = UpdatePortfolioDto(recordId: 123, accountId: 123, type: "type_example") // UpdatePortfolioDto | 

// Update Portfolio
PortfolioAPI.accountPortfoliosControllerUpdate(accountId: accountId, recordId: recordId, updatePortfolioDto: updatePortfolioDto) { (response, error) in
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
 **updatePortfolioDto** | [**UpdatePortfolioDto**](UpdatePortfolioDto.md) |  | 

### Return type

[**PortfolioDto**](PortfolioDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **portfolioControllerFindOne**
```swift
    open class func portfolioControllerFindOne(recordId: Double, completion: @escaping (_ data: PortfolioDto?, _ error: Error?) -> Void)
```

Get single Portfolio

Returns single portfolio. This is a helper method if you don't have the accountId.

### Example
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let recordId = 987 // Double | 

// Get single Portfolio
PortfolioAPI.portfolioControllerFindOne(recordId: recordId) { (response, error) in
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

[**PortfolioDto**](PortfolioDto.md)

### Authorization

[apiHeaderSec](../README.md#apiHeaderSec)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

