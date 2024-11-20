# Swagger\Client\ApiDocssoundsFormatApi

All URIs are relative to *http://localhost:18088/ari*

Method | HTTP request | Description
------------- | ------------- | -------------
[**callList**](ApiDocssoundsFormatApi.md#callList) | **GET** /sounds | List all sounds.
[**get**](ApiDocssoundsFormatApi.md#get) | **GET** /sounds/{soundId} | Get a sound&#39;s details.


# **callList**
> callList($lang, $format)

List all sounds.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ApiDocssoundsFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$lang = "lang_example"; // string | Lookup sound for a specific language.
$format = "format_example"; // string | Lookup sound in a specific format.

try {
    $apiInstance->callList($lang, $format);
} catch (Exception $e) {
    echo 'Exception when calling ApiDocssoundsFormatApi->callList: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **lang** | **string**| Lookup sound for a specific language. | [optional]
 **format** | **string**| Lookup sound in a specific format. | [optional]

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **get**
> get($sound_id)

Get a sound's details.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ApiDocssoundsFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$sound_id = "sound_id_example"; // string | Sound's id

try {
    $apiInstance->get($sound_id);
} catch (Exception $e) {
    echo 'Exception when calling ApiDocssoundsFormatApi->get: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **sound_id** | **string**| Sound&#39;s id |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

