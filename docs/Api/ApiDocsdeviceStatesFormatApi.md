# Swagger\Client\ApiDocsdeviceStatesFormatApi

All URIs are relative to *http://localhost:18088/ari*

Method | HTTP request | Description
------------- | ------------- | -------------
[**callList**](ApiDocsdeviceStatesFormatApi.md#callList) | **GET** /deviceStates | List all ARI controlled device states.
[**delete**](ApiDocsdeviceStatesFormatApi.md#delete) | **DELETE** /deviceStates/{deviceName} | Destroy a device-state controlled by ARI.
[**get**](ApiDocsdeviceStatesFormatApi.md#get) | **GET** /deviceStates/{deviceName} | Retrieve the current state of a device.
[**update**](ApiDocsdeviceStatesFormatApi.md#update) | **PUT** /deviceStates/{deviceName} | Change the state of a device controlled by ARI. (Note - implicitly creates the device state).


# **callList**
> callList()

List all ARI controlled device states.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ApiDocsdeviceStatesFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $apiInstance->callList();
} catch (Exception $e) {
    echo 'Exception when calling ApiDocsdeviceStatesFormatApi->callList: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **delete**
> delete($device_name)

Destroy a device-state controlled by ARI.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ApiDocsdeviceStatesFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$device_name = "device_name_example"; // string | Name of the device

try {
    $apiInstance->delete($device_name);
} catch (Exception $e) {
    echo 'Exception when calling ApiDocsdeviceStatesFormatApi->delete: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **device_name** | **string**| Name of the device |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **get**
> get($device_name)

Retrieve the current state of a device.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ApiDocsdeviceStatesFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$device_name = "device_name_example"; // string | Name of the device

try {
    $apiInstance->get($device_name);
} catch (Exception $e) {
    echo 'Exception when calling ApiDocsdeviceStatesFormatApi->get: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **device_name** | **string**| Name of the device |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **update**
> update($device_name, $device_state)

Change the state of a device controlled by ARI. (Note - implicitly creates the device state).

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ApiDocsdeviceStatesFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$device_name = "device_name_example"; // string | Name of the device
$device_state = "device_state_example"; // string | Device state value

try {
    $apiInstance->update($device_name, $device_state);
} catch (Exception $e) {
    echo 'Exception when calling ApiDocsdeviceStatesFormatApi->update: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **device_name** | **string**| Name of the device |
 **device_state** | **string**| Device state value |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

