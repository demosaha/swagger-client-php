# Swagger\Client\EstimatesApi

All URIs are relative to *https://api.uber.com/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**estimatesPriceGet**](EstimatesApi.md#estimatesPriceGet) | **GET** /estimates/price | Price Estimates
[**estimatesTimeGet**](EstimatesApi.md#estimatesTimeGet) | **GET** /estimates/time | Time Estimates


# **estimatesPriceGet**
> \Swagger\Client\Model\PriceEstimate[] estimatesPriceGet($start_latitude, $start_longitude, $end_latitude, $end_longitude)

Price Estimates

The Price Estimates endpoint returns an estimated price range\nfor each product offered at a given location. The price estimate is\nprovided as a formatted string with the full price range and the localized\ncurrency symbol.<br><br>The response also includes low and high estimates,\nand the [ISO 4217](http://en.wikipedia.org/wiki/ISO_4217) currency code for\nsituations requiring currency conversion. When surge is active for a particular\nproduct, its surge_multiplier will be greater than 1, but the price estimate\nalready factors in this multiplier.

### Example 
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$api_instance = new Swagger\Client\Api\EstimatesApi();
$start_latitude = 1.2; // double | Latitude component of start location.
$start_longitude = 1.2; // double | Longitude component of start location.
$end_latitude = 1.2; // double | Latitude component of end location.
$end_longitude = 1.2; // double | Longitude component of end location.

try { 
    $result = $api_instance->estimatesPriceGet($start_latitude, $start_longitude, $end_latitude, $end_longitude);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EstimatesApi->estimatesPriceGet: ', $e->getMessage(), "\n";
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **start_latitude** | **double**| Latitude component of start location. | 
 **start_longitude** | **double**| Longitude component of start location. | 
 **end_latitude** | **double**| Latitude component of end location. | 
 **end_longitude** | **double**| Longitude component of end location. | 

### Return type

[**\Swagger\Client\Model\PriceEstimate[]**](PriceEstimate.md)

### Authorization

No authorization required

### HTTP reuqest headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **estimatesTimeGet**
> \Swagger\Client\Model\Product[] estimatesTimeGet($start_latitude, $start_longitude, $customer_uuid, $product_id)

Time Estimates

The Time Estimates endpoint returns ETAs for all products offered at a given location, with the responses expressed as integers in seconds. We recommend that this endpoint be called every minute to provide the most accurate, up-to-date ETAs.

### Example 
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$api_instance = new Swagger\Client\Api\EstimatesApi();
$start_latitude = 1.2; // double | Latitude component of start location.
$start_longitude = 1.2; // double | Longitude component of start location.
$customer_uuid = new UUID(); // UUID | Unique customer identifier to be used for experience customization.
$product_id = "product_id_example"; // string | Unique identifier representing a specific product for a given latitude & longitude.

try { 
    $result = $api_instance->estimatesTimeGet($start_latitude, $start_longitude, $customer_uuid, $product_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EstimatesApi->estimatesTimeGet: ', $e->getMessage(), "\n";
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **start_latitude** | **double**| Latitude component of start location. | 
 **start_longitude** | **double**| Longitude component of start location. | 
 **customer_uuid** | [**UUID**](.md)| Unique customer identifier to be used for experience customization. | [optional] 
 **product_id** | **string**| Unique identifier representing a specific product for a given latitude &amp; longitude. | [optional] 

### Return type

[**\Swagger\Client\Model\Product[]**](Product.md)

### Authorization

No authorization required

### HTTP reuqest headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

