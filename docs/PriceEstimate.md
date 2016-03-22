# PriceEstimate

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**product_id** | **string** | Unique identifier representing a specific product for a given latitude &amp; longitude. For example, uberX in San Francisco will have a different product_id than uberX in Los Angeles | [optional] 
**currency_code** | **string** | [ISO 4217](http://en.wikipedia.org/wiki/ISO_4217) currency code. | [optional] 
**display_name** | **string** | Display name of product. | [optional] 
**estimate** | **string** | Formatted string of estimate in local currency of the start location. Estimate could be a range, a single number (flat rate) or \&quot;Metered\&quot; for TAXI. | [optional] 
**low_estimate** | [**Number**](Number.md) | Lower bound of the estimated price. | [optional] 
**high_estimate** | [**Number**](Number.md) | Upper bound of the estimated price. | [optional] 
**surge_multiplier** | [**Number**](Number.md) | Expected surge multiplier. Surge is active if surge_multiplier is greater than 1. Price estimate already factors in the surge multiplier. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


