# Swagger\Client\ApplicationsFormatApi

All URIs are relative to *http://localhost:8088/ari*

Method | HTTP request | Description
------------- | ------------- | -------------
[**callList**](ApplicationsFormatApi.md#callList) | **GET** /applications | List all applications.
[**filter**](ApplicationsFormatApi.md#filter) | **PUT** /applications/{applicationName}/eventFilter | Filter application events types.
[**get**](ApplicationsFormatApi.md#get) | **GET** /applications/{applicationName} | Get details of an application.
[**subscribe**](ApplicationsFormatApi.md#subscribe) | **POST** /applications/{applicationName}/subscription | Subscribe an application to a event source.
[**unsubscribe**](ApplicationsFormatApi.md#unsubscribe) | **DELETE** /applications/{applicationName}/subscription | Unsubscribe an application from an event source.


# **callList**
> callList()

List all applications.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ApplicationsFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $apiInstance->callList();
} catch (Exception $e) {
    echo 'Exception when calling ApplicationsFormatApi->callList: ', $e->getMessage(), PHP_EOL;
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

# **filter**
> filter($application_name, $filter)

Filter application events types.

Allowed and/or disallowed event type filtering can be done. The body (parameter) should specify a JSON key/value object that describes the type of event filtering needed. One, or both of the following keys can be designated:<br /><br />\"allowed\" - Specifies an allowed list of event types<br />\"disallowed\" - Specifies a disallowed list of event types<br /><br />Further, each of those key's value should be a JSON array that holds zero, or more JSON key/value objects. Each of these objects must contain the following key with an associated value:<br /><br />\"type\" - The type name of the event to filter<br /><br />The value must be the string name (case sensitive) of the event type that needs filtering. For example:<br /><br />{ \"allowed\": [ { \"type\": \"StasisStart\" }, { \"type\": \"StasisEnd\" } ] }<br /><br />As this specifies only an allowed list, then only those two event type messages are sent to the application. No other event messages are sent.<br /><br />The following rules apply:<br /><br />* If the body is empty, both the allowed and disallowed filters are set empty.<br />* If both list types are given then both are set to their respective values (note, specifying an empty array for a given type sets that type to empty).<br />* If only one list type is given then only that type is set. The other type is not updated.<br />* An empty \"allowed\" list means all events are allowed.<br />* An empty \"disallowed\" list means no events are disallowed.<br />* Disallowed events take precedence over allowed events if the event type is specified in both lists.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ApplicationsFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$application_name = "application_name_example"; // string | Application's name
$filter = new \stdClass; // object | Specify which event types to allow/disallow

try {
    $apiInstance->filter($application_name, $filter);
} catch (Exception $e) {
    echo 'Exception when calling ApplicationsFormatApi->filter: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **application_name** | **string**| Application&#39;s name |
 **filter** | [**object**](../Model/object.md)| Specify which event types to allow/disallow | [optional]

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **get**
> get($application_name)

Get details of an application.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ApplicationsFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$application_name = "application_name_example"; // string | Application's name

try {
    $apiInstance->get($application_name);
} catch (Exception $e) {
    echo 'Exception when calling ApplicationsFormatApi->get: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **application_name** | **string**| Application&#39;s name |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **subscribe**
> subscribe($application_name, $event_source)

Subscribe an application to a event source.

Returns the state of the application after the subscriptions have changed

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ApplicationsFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$application_name = "application_name_example"; // string | Application's name
$event_source = array("event_source_example"); // string[] | URI for event source (channel:{channelId}, bridge:{bridgeId}, endpoint:{tech}[/{resource}], deviceState:{deviceName}

try {
    $apiInstance->subscribe($application_name, $event_source);
} catch (Exception $e) {
    echo 'Exception when calling ApplicationsFormatApi->subscribe: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **application_name** | **string**| Application&#39;s name |
 **event_source** | [**string[]**](../Model/string.md)| URI for event source (channel:{channelId}, bridge:{bridgeId}, endpoint:{tech}[/{resource}], deviceState:{deviceName} |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **unsubscribe**
> unsubscribe($application_name, $event_source)

Unsubscribe an application from an event source.

Returns the state of the application after the subscriptions have changed

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ApplicationsFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$application_name = "application_name_example"; // string | Application's name
$event_source = array("event_source_example"); // string[] | URI for event source (channel:{channelId}, bridge:{bridgeId}, endpoint:{tech}[/{resource}], deviceState:{deviceName}

try {
    $apiInstance->unsubscribe($application_name, $event_source);
} catch (Exception $e) {
    echo 'Exception when calling ApplicationsFormatApi->unsubscribe: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **application_name** | **string**| Application&#39;s name |
 **event_source** | [**string[]**](../Model/string.md)| URI for event source (channel:{channelId}, bridge:{bridgeId}, endpoint:{tech}[/{resource}], deviceState:{deviceName} |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

