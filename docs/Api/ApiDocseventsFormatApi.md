# Swagger\Client\ApiDocseventsFormatApi

All URIs are relative to *http://localhost:18088/ari*

Method | HTTP request | Description
------------- | ------------- | -------------
[**eventWebsocket**](ApiDocseventsFormatApi.md#eventWebsocket) | **GET** /events | WebSocket connection for events.
[**userEvent**](ApiDocseventsFormatApi.md#userEvent) | **POST** /events/user/{eventName} | Generate a user event.


# **eventWebsocket**
> eventWebsocket($app, $subscribe_all)

WebSocket connection for events.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ApiDocseventsFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$app = array("app_example"); // string[] | Applications to subscribe to.
$subscribe_all = true; // bool | Subscribe to all Asterisk events. If provided, the applications listed will be subscribed to all events, effectively disabling the application specific subscriptions. Default is 'false'.

try {
    $apiInstance->eventWebsocket($app, $subscribe_all);
} catch (Exception $e) {
    echo 'Exception when calling ApiDocseventsFormatApi->eventWebsocket: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **app** | [**string[]**](../Model/string.md)| Applications to subscribe to. |
 **subscribe_all** | **bool**| Subscribe to all Asterisk events. If provided, the applications listed will be subscribed to all events, effectively disabling the application specific subscriptions. Default is &#39;false&#39;. | [optional]

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **userEvent**
> userEvent($event_name, $application, $source, $variables)

Generate a user event.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ApiDocseventsFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$event_name = "event_name_example"; // string | Event name
$application = "application_example"; // string | The name of the application that will receive this event
$source = array("source_example"); // string[] | URI for event source (channel:{channelId}, bridge:{bridgeId}, endpoint:{tech}/{resource}, deviceState:{deviceName}
$variables = new \Swagger\Client\Model\Containers(); // \Swagger\Client\Model\Containers | The \"variables\" key in the body object holds custom key/value pairs to add to the user event. Ex. { \"variables\": { \"key\": \"value\" } }

try {
    $apiInstance->userEvent($event_name, $application, $source, $variables);
} catch (Exception $e) {
    echo 'Exception when calling ApiDocseventsFormatApi->userEvent: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **event_name** | **string**| Event name |
 **application** | **string**| The name of the application that will receive this event |
 **source** | [**string[]**](../Model/string.md)| URI for event source (channel:{channelId}, bridge:{bridgeId}, endpoint:{tech}/{resource}, deviceState:{deviceName} | [optional]
 **variables** | [**\Swagger\Client\Model\Containers**](../Model/Containers.md)| The \&quot;variables\&quot; key in the body object holds custom key/value pairs to add to the user event. Ex. { \&quot;variables\&quot;: { \&quot;key\&quot;: \&quot;value\&quot; } } | [optional]

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

