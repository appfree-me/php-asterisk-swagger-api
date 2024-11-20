# Swagger\Client\ApiDocsrecordingsFormatApi

All URIs are relative to *http://localhost:18088/ari*

Method | HTTP request | Description
------------- | ------------- | -------------
[**cancel**](ApiDocsrecordingsFormatApi.md#cancel) | **DELETE** /recordings/live/{recordingName} | Stop a live recording and discard it.
[**copyStored**](ApiDocsrecordingsFormatApi.md#copyStored) | **POST** /recordings/stored/{recordingName}/copy | Copy a stored recording.
[**deleteStored**](ApiDocsrecordingsFormatApi.md#deleteStored) | **DELETE** /recordings/stored/{recordingName} | Delete a stored recording.
[**getLive**](ApiDocsrecordingsFormatApi.md#getLive) | **GET** /recordings/live/{recordingName} | List live recordings.
[**getStored**](ApiDocsrecordingsFormatApi.md#getStored) | **GET** /recordings/stored/{recordingName} | Get a stored recording&#39;s details.
[**getStoredFile**](ApiDocsrecordingsFormatApi.md#getStoredFile) | **GET** /recordings/stored/{recordingName}/file | Get the file associated with the stored recording.
[**listStored**](ApiDocsrecordingsFormatApi.md#listStored) | **GET** /recordings/stored | List recordings that are complete.
[**mute**](ApiDocsrecordingsFormatApi.md#mute) | **POST** /recordings/live/{recordingName}/mute | Mute a live recording.
[**pause**](ApiDocsrecordingsFormatApi.md#pause) | **POST** /recordings/live/{recordingName}/pause | Pause a live recording.
[**stop**](ApiDocsrecordingsFormatApi.md#stop) | **POST** /recordings/live/{recordingName}/stop | Stop a live recording and store it.
[**unmute**](ApiDocsrecordingsFormatApi.md#unmute) | **DELETE** /recordings/live/{recordingName}/mute | Unmute a live recording.
[**unpause**](ApiDocsrecordingsFormatApi.md#unpause) | **DELETE** /recordings/live/{recordingName}/pause | Unpause a live recording.


# **cancel**
> cancel($recording_name)

Stop a live recording and discard it.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ApiDocsrecordingsFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$recording_name = "recording_name_example"; // string | The name of the recording

try {
    $apiInstance->cancel($recording_name);
} catch (Exception $e) {
    echo 'Exception when calling ApiDocsrecordingsFormatApi->cancel: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **recording_name** | **string**| The name of the recording |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **copyStored**
> copyStored($recording_name, $destination_recording_name)

Copy a stored recording.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ApiDocsrecordingsFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$recording_name = "recording_name_example"; // string | The name of the recording to copy
$destination_recording_name = "destination_recording_name_example"; // string | The destination name of the recording

try {
    $apiInstance->copyStored($recording_name, $destination_recording_name);
} catch (Exception $e) {
    echo 'Exception when calling ApiDocsrecordingsFormatApi->copyStored: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **recording_name** | **string**| The name of the recording to copy |
 **destination_recording_name** | **string**| The destination name of the recording |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **deleteStored**
> deleteStored($recording_name)

Delete a stored recording.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ApiDocsrecordingsFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$recording_name = "recording_name_example"; // string | The name of the recording

try {
    $apiInstance->deleteStored($recording_name);
} catch (Exception $e) {
    echo 'Exception when calling ApiDocsrecordingsFormatApi->deleteStored: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **recording_name** | **string**| The name of the recording |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getLive**
> getLive($recording_name)

List live recordings.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ApiDocsrecordingsFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$recording_name = "recording_name_example"; // string | The name of the recording

try {
    $apiInstance->getLive($recording_name);
} catch (Exception $e) {
    echo 'Exception when calling ApiDocsrecordingsFormatApi->getLive: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **recording_name** | **string**| The name of the recording |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getStored**
> getStored($recording_name)

Get a stored recording's details.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ApiDocsrecordingsFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$recording_name = "recording_name_example"; // string | The name of the recording

try {
    $apiInstance->getStored($recording_name);
} catch (Exception $e) {
    echo 'Exception when calling ApiDocsrecordingsFormatApi->getStored: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **recording_name** | **string**| The name of the recording |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getStoredFile**
> getStoredFile($recording_name)

Get the file associated with the stored recording.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ApiDocsrecordingsFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$recording_name = "recording_name_example"; // string | The name of the recording

try {
    $apiInstance->getStoredFile($recording_name);
} catch (Exception $e) {
    echo 'Exception when calling ApiDocsrecordingsFormatApi->getStoredFile: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **recording_name** | **string**| The name of the recording |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **listStored**
> listStored()

List recordings that are complete.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ApiDocsrecordingsFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $apiInstance->listStored();
} catch (Exception $e) {
    echo 'Exception when calling ApiDocsrecordingsFormatApi->listStored: ', $e->getMessage(), PHP_EOL;
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

# **mute**
> mute($recording_name)

Mute a live recording.

Muting a recording suspends silence detection, which will be restarted when the recording is unmuted.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ApiDocsrecordingsFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$recording_name = "recording_name_example"; // string | The name of the recording

try {
    $apiInstance->mute($recording_name);
} catch (Exception $e) {
    echo 'Exception when calling ApiDocsrecordingsFormatApi->mute: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **recording_name** | **string**| The name of the recording |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **pause**
> pause($recording_name)

Pause a live recording.

Pausing a recording suspends silence detection, which will be restarted when the recording is unpaused. Paused time is not included in the accounting for maxDurationSeconds.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ApiDocsrecordingsFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$recording_name = "recording_name_example"; // string | The name of the recording

try {
    $apiInstance->pause($recording_name);
} catch (Exception $e) {
    echo 'Exception when calling ApiDocsrecordingsFormatApi->pause: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **recording_name** | **string**| The name of the recording |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **stop**
> stop($recording_name)

Stop a live recording and store it.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ApiDocsrecordingsFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$recording_name = "recording_name_example"; // string | The name of the recording

try {
    $apiInstance->stop($recording_name);
} catch (Exception $e) {
    echo 'Exception when calling ApiDocsrecordingsFormatApi->stop: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **recording_name** | **string**| The name of the recording |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **unmute**
> unmute($recording_name)

Unmute a live recording.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ApiDocsrecordingsFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$recording_name = "recording_name_example"; // string | The name of the recording

try {
    $apiInstance->unmute($recording_name);
} catch (Exception $e) {
    echo 'Exception when calling ApiDocsrecordingsFormatApi->unmute: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **recording_name** | **string**| The name of the recording |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **unpause**
> unpause($recording_name)

Unpause a live recording.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ApiDocsrecordingsFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$recording_name = "recording_name_example"; // string | The name of the recording

try {
    $apiInstance->unpause($recording_name);
} catch (Exception $e) {
    echo 'Exception when calling ApiDocsrecordingsFormatApi->unpause: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **recording_name** | **string**| The name of the recording |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

