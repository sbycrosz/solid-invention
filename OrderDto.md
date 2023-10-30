# OrderDto

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**recordId** | **Int** |  | 
**portfolioId** | **Int** |  | 
**userId** | **Int** |  | 
**executedBy** | **Int** |  | 
**pricePerUnit** | **String** |  | 
**lpPricePerUnit** | **String** |  | [optional] 
**stopPrice** | **String** | StopPrice is mandatory for limit orders. For all create &amp; update calls involving limit orders this price must be specified as well. | [optional] 
**requestedQuantity** | **String** |  | 
**filledQuantity** | **String** |  | 
**platformId** | **Int** |  | 
**platformFee** | **String** |  | 
**arkhonFeePercentage** | **String** |  | 
**arkhonSpreadPercentage** | **String** |  | [optional] 
**tierId** | **Int** |  | 
**arkhonSpread** | **String** |  | [optional] 
**arkhonFee** | **String** |  | 
**totalFees** | **String** |  | 
**subtotal** | **String** |  | 
**totalConsideration** | **String** |  | 
**portfolio** | [**PortfolioDto**](PortfolioDto.md) |  | [optional] 
**baseToken** | **String** |  | 
**quoteToken** | **String** |  | 
**tradedToken** | **String** |  | 
**side** | **String** |  | 
**startTime** | **Date** |  | 
**endTime** | **Date** |  | [optional] 
**strategy** | **String** |  | 
**type** | **String** |  | 
**platform** | [**PlatformDto**](PlatformDto.md) |  | [optional] 
**platformRefId** | **String** |  | 
**clientRefId** | **String** |  | [optional] 
**platformFeeCurrency** | **String** |  | 
**status** | **String** |  | 
**arkhonFeeCurrency** | **String** |  | 
**feeStatus** | **String** |  | 
**feeComment** | **String** |  | 
**comment** | **String** |  | 
**settlementId** | **Double** |  | [optional] 
**description** | **String** |  | 
**enrichments** | [**OrderEnrichment**](OrderEnrichment.md) |  | [optional] 
**statistics** | [AssetStatistic] |  | [optional] 
**version** | **Double** |  | 
**updatedOn** | **Date** |  | 
**deletionDt** | **Date** |  | [optional] 
**creationDt** | **Date** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


