# Swagger\Client\ProductsApi

All URIs are relative to *https://api.uber.com/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**productsGet**](ProductsApi.md#productsGet) | **GET** /products | Product Types


# **productsGet**
> \Swagger\Client\Model\Product[] productsGet($latitude, $longitude)

Product Types

The Products endpoint returns information about the *Uber* products\noffered at a given location. The response includes the display name\nand other details about each product, and lists the products in the\nproper display order.

### Example 
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$api_instance = new Swagger\Client\Api\ProductsApi();
$latitude = 1.2; // double | Latitude component of location.
$longitude = 1.2; // double | Longitude component of location.

try { 
    $result = $api_instance->productsGet($latitude, $longitude);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductsApi->productsGet: ', $e->getMessage(), "\n";
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **latitude** | **double**| Latitude component of location. | 
 **longitude** | **double**| Longitude component of location. | 

### Return type

[**\Swagger\Client\Model\Product[]**](Product.md)

### Authorization

No authorization required

### HTTP reuqest headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

