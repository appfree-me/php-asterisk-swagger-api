# Swagger\Client\PlaybacksFormatApi

All URIs are relative to *http://localhost:8088/ari*

Method | HTTP request | Description
------------- | ------------- | -------------
[**control**](PlaybacksFormatApi.md#control) | **POST** /playbacks/{playbackId}/control | Control a playback.
[**get**](PlaybacksFormatApi.md#get) | **GET** /playbacks/{playbackId} | Get a playback&#39;s details.
[**stop**](PlaybacksFormatApi.md#stop) | **DELETE** /playbacks/{playbackId} | Stop a playback.


# **control**
> control($playback_id, $operation)

Control a playback.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\PlaybacksFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$playback_id = "playback_id_example"; // string | Playback's id
$operation = "operation_example"; // string | Operation to perform on the playback.

try {
    $apiInstance->control($playback_id, $operation);
} catch (Exception $e) {
    echo 'Exception when calling PlaybacksFormatApi->control: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **playback_id** | **string**| Playback&#39;s id |
 **operation** | **string**| Operation to perform on the playback. |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **get**
> get($playback_id)

Get a playback's details.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\PlaybacksFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$playback_id = "playback_id_example"; // string | Playback's id

try {
    $apiInstance->get($playback_id);
} catch (Exception $e) {
    echo 'Exception when calling PlaybacksFormatApi->get: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **playback_id** | **string**| Playback&#39;s id |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **stop**
> stop($playback_id)

Stop a playback.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\PlaybacksFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$playback_id = "playback_id_example"; // string | Playback's id

try {
    $apiInstance->stop($playback_id);
} catch (Exception $e) {
    echo 'Exception when calling PlaybacksFormatApi->stop: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **playback_id** | **string**| Playback&#39;s id |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

