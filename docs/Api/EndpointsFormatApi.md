# Swagger\Client\EndpointsFormatApi

All URIs are relative to *http://localhost:8088/ari*

Method | HTTP request | Description
------------- | ------------- | -------------
[**callList**](EndpointsFormatApi.md#callList) | **GET** /endpoints | List all endpoints.
[**get**](EndpointsFormatApi.md#get) | **GET** /endpoints/{tech}/{resource} | Details for an endpoint.
[**listByTech**](EndpointsFormatApi.md#listByTech) | **GET** /endpoints/{tech} | List available endoints for a given endpoint technology.
[**sendMessage**](EndpointsFormatApi.md#sendMessage) | **PUT** /endpoints/sendMessage | Send a message to some technology URI or endpoint.
[**sendMessageToEndpoint**](EndpointsFormatApi.md#sendMessageToEndpoint) | **PUT** /endpoints/{tech}/{resource}/sendMessage | Send a message to some endpoint in a technology.


# **callList**
> callList()

List all endpoints.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\EndpointsFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $apiInstance->callList();
} catch (Exception $e) {
    echo 'Exception when calling EndpointsFormatApi->callList: ', $e->getMessage(), PHP_EOL;
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

# **get**
> get($tech, $resource)

Details for an endpoint.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\EndpointsFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$tech = "tech_example"; // string | Technology of the endpoint
$resource = "resource_example"; // string | ID of the endpoint

try {
    $apiInstance->get($tech, $resource);
} catch (Exception $e) {
    echo 'Exception when calling EndpointsFormatApi->get: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **tech** | **string**| Technology of the endpoint |
 **resource** | **string**| ID of the endpoint |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **listByTech**
> listByTech($tech)

List available endoints for a given endpoint technology.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\EndpointsFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$tech = "tech_example"; // string | Technology of the endpoints (sip,iax2,...)

try {
    $apiInstance->listByTech($tech);
} catch (Exception $e) {
    echo 'Exception when calling EndpointsFormatApi->listByTech: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **tech** | **string**| Technology of the endpoints (sip,iax2,...) |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **sendMessage**
> sendMessage($to, $from, $body, $variables)

Send a message to some technology URI or endpoint.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\EndpointsFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$to = "to_example"; // string | The endpoint resource or technology specific URI to send the message to. Valid resources are sip, pjsip, and xmpp.
$from = "from_example"; // string | The endpoint resource or technology specific identity to send this message from. Valid resources are sip, pjsip, and xmpp.
$body = "body_example"; // string | The body of the message
$variables = new \Swagger\Client\Model\Containers(); // \Swagger\Client\Model\Containers | 

try {
    $apiInstance->sendMessage($to, $from, $body, $variables);
} catch (Exception $e) {
    echo 'Exception when calling EndpointsFormatApi->sendMessage: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **to** | **string**| The endpoint resource or technology specific URI to send the message to. Valid resources are sip, pjsip, and xmpp. |
 **from** | **string**| The endpoint resource or technology specific identity to send this message from. Valid resources are sip, pjsip, and xmpp. |
 **body** | **string**| The body of the message | [optional]
 **variables** | [**\Swagger\Client\Model\Containers**](../Model/Containers.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **sendMessageToEndpoint**
> sendMessageToEndpoint($tech, $resource, $from, $body, $variables)

Send a message to some endpoint in a technology.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\EndpointsFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$tech = "tech_example"; // string | Technology of the endpoint
$resource = "resource_example"; // string | ID of the endpoint
$from = "from_example"; // string | The endpoint resource or technology specific identity to send this message from. Valid resources are sip, pjsip, and xmpp.
$body = "body_example"; // string | The body of the message
$variables = new \Swagger\Client\Model\Containers(); // \Swagger\Client\Model\Containers | 

try {
    $apiInstance->sendMessageToEndpoint($tech, $resource, $from, $body, $variables);
} catch (Exception $e) {
    echo 'Exception when calling EndpointsFormatApi->sendMessageToEndpoint: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **tech** | **string**| Technology of the endpoint |
 **resource** | **string**| ID of the endpoint |
 **from** | **string**| The endpoint resource or technology specific identity to send this message from. Valid resources are sip, pjsip, and xmpp. |
 **body** | **string**| The body of the message | [optional]
 **variables** | [**\Swagger\Client\Model\Containers**](../Model/Containers.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

