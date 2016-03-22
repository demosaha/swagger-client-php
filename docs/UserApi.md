# Swagger\Client\UserApi

All URIs are relative to *https://api.uber.com/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**historyGet**](UserApi.md#historyGet) | **GET** /history | User Activity
[**meGet**](UserApi.md#meGet) | **GET** /me | User Profile


# **historyGet**
> \Swagger\Client\Model\Activities historyGet($offset, $limit)

User Activity

The User Activity endpoint returns data about a user's lifetime activity with Uber. The response will include pickup locations and times, dropoff locations and times, the distance of past requests, and information about which products were requested.<br><br>The history array in the response will have a maximum length based on the limit parameter. The response value count may exceed limit, therefore subsequent API requests may be necessary.

### Example 
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$api_instance = new Swagger\Client\Api\UserApi();
$offset = 56; // int | Offset the list of returned results by this amount. Default is zero.
$limit = 56; // int | Number of items to retrieve. Default is 5, maximum is 100.

try { 
    $result = $api_instance->historyGet($offset, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserApi->historyGet: ', $e->getMessage(), "\n";
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **offset** | **int**| Offset the list of returned results by this amount. Default is zero. | [optional] 
 **limit** | **int**| Number of items to retrieve. Default is 5, maximum is 100. | [optional] 

### Return type

[**\Swagger\Client\Model\Activities**](Activities.md)

### Authorization

No authorization required

### HTTP reuqest headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **meGet**
> \Swagger\Client\Model\Profile meGet()

User Profile

The User Profile endpoint returns information about the Uber user that has authorized with the application.

### Example 
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$api_instance = new Swagger\Client\Api\UserApi();

try { 
    $result = $api_instance->meGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserApi->meGet: ', $e->getMessage(), "\n";
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\Swagger\Client\Model\Profile**](Profile.md)

### Authorization

No authorization required

### HTTP reuqest headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

