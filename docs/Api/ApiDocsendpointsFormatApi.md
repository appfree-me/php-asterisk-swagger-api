# Swagger\Client\ApiDocsendpointsFormatApi

All URIs are relative to *http://localhost:18088/ari*

Method | HTTP request | Description
------------- | ------------- | -------------
[**callList**](ApiDocsendpointsFormatApi.md#callList) | **GET** /endpoints | List all endpoints.
[**get**](ApiDocsendpointsFormatApi.md#get) | **GET** /endpoints/{tech}/{resource} | Details for an endpoint.
[**listByTech**](ApiDocsendpointsFormatApi.md#listByTech) | **GET** /endpoints/{tech} | List available endoints for a given endpoint technology.
[**refer**](ApiDocsendpointsFormatApi.md#refer) | **POST** /endpoints/refer | Refer an endpoint or technology URI to some technology URI or endpoint.
[**referToEndpoint**](ApiDocsendpointsFormatApi.md#referToEndpoint) | **POST** /endpoints/{tech}/{resource}/refer | Refer an endpoint or technology URI to some technology URI or endpoint.
[**sendMessage**](ApiDocsendpointsFormatApi.md#sendMessage) | **PUT** /endpoints/sendMessage | Send a message to some technology URI or endpoint.
[**sendMessageToEndpoint**](ApiDocsendpointsFormatApi.md#sendMessageToEndpoint) | **PUT** /endpoints/{tech}/{resource}/sendMessage | Send a message to some endpoint in a technology.


# **callList**
> callList()

List all endpoints.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ApiDocsendpointsFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $apiInstance->callList();
} catch (Exception $e) {
    echo 'Exception when calling ApiDocsendpointsFormatApi->callList: ', $e->getMessage(), PHP_EOL;
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

$apiInstance = new Swagger\Client\Api\ApiDocsendpointsFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$tech = "tech_example"; // string | Technology of the endpoint
$resource = "resource_example"; // string | ID of the endpoint

try {
    $apiInstance->get($tech, $resource);
} catch (Exception $e) {
    echo 'Exception when calling ApiDocsendpointsFormatApi->get: ', $e->getMessage(), PHP_EOL;
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

$apiInstance = new Swagger\Client\Api\ApiDocsendpointsFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$tech = "tech_example"; // string | Technology of the endpoints (sip,iax2,...)

try {
    $apiInstance->listByTech($tech);
} catch (Exception $e) {
    echo 'Exception when calling ApiDocsendpointsFormatApi->listByTech: ', $e->getMessage(), PHP_EOL;
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

# **refer**
> refer($to, $from, $refer_to, $to_self, $variables)

Refer an endpoint or technology URI to some technology URI or endpoint.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ApiDocsendpointsFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$to = "to_example"; // string | The endpoint resource or technology specific URI that should be referred to somewhere. Valid resource is pjsip.
$from = "from_example"; // string | The endpoint resource or technology specific identity to refer from.
$refer_to = "refer_to_example"; // string | The endpoint resource or technology specific URI to refer to.
$to_self = false; // bool | If true and \"refer_to\" refers to an Asterisk endpoint, the \"refer_to\" value is set to point to this Asterisk endpoint - so the referee is referred to Asterisk. Otherwise, use the contact URI associated with the endpoint.
$variables = new \Swagger\Client\Model\Containers(); // \Swagger\Client\Model\Containers | The \"variables\" key in the body object holds technology specific key/value pairs to append to the message. These can be interpreted and used by the various resource types; for example, the pjsip resource type will add the key/value pairs as SIP headers. The \"display_name\" key is used by the PJSIP technology. Its value will be prepended as a display name to the Refer-To URI.

try {
    $apiInstance->refer($to, $from, $refer_to, $to_self, $variables);
} catch (Exception $e) {
    echo 'Exception when calling ApiDocsendpointsFormatApi->refer: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **to** | **string**| The endpoint resource or technology specific URI that should be referred to somewhere. Valid resource is pjsip. |
 **from** | **string**| The endpoint resource or technology specific identity to refer from. |
 **refer_to** | **string**| The endpoint resource or technology specific URI to refer to. |
 **to_self** | **bool**| If true and \&quot;refer_to\&quot; refers to an Asterisk endpoint, the \&quot;refer_to\&quot; value is set to point to this Asterisk endpoint - so the referee is referred to Asterisk. Otherwise, use the contact URI associated with the endpoint. | [optional] [default to false]
 **variables** | [**\Swagger\Client\Model\Containers**](../Model/Containers.md)| The \&quot;variables\&quot; key in the body object holds technology specific key/value pairs to append to the message. These can be interpreted and used by the various resource types; for example, the pjsip resource type will add the key/value pairs as SIP headers. The \&quot;display_name\&quot; key is used by the PJSIP technology. Its value will be prepended as a display name to the Refer-To URI. | [optional]

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **referToEndpoint**
> referToEndpoint($tech, $resource, $from, $refer_to, $to_self, $variables)

Refer an endpoint or technology URI to some technology URI or endpoint.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ApiDocsendpointsFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$tech = "tech_example"; // string | Technology of the endpoint
$resource = "resource_example"; // string | ID of the endpoint
$from = "from_example"; // string | The endpoint resource or technology specific identity to refer from.
$refer_to = "refer_to_example"; // string | The endpoint resource or technology specific URI to refer to.
$to_self = false; // bool | If true and \"refer_to\" refers to an Asterisk endpoint, the \"refer_to\" value is set to point to this Asterisk endpoint - so the referee is referred to Asterisk. Otherwise, use the contact URI associated with the endpoint.
$variables = new \Swagger\Client\Model\Containers(); // \Swagger\Client\Model\Containers | The \"variables\" key in the body object holds technology specific key/value pairs to append to the message. These can be interpreted and used by the various resource types; for example, the pjsip resource type will add the key/value pairs as SIP headers,

try {
    $apiInstance->referToEndpoint($tech, $resource, $from, $refer_to, $to_self, $variables);
} catch (Exception $e) {
    echo 'Exception when calling ApiDocsendpointsFormatApi->referToEndpoint: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **tech** | **string**| Technology of the endpoint |
 **resource** | **string**| ID of the endpoint |
 **from** | **string**| The endpoint resource or technology specific identity to refer from. |
 **refer_to** | **string**| The endpoint resource or technology specific URI to refer to. |
 **to_self** | **bool**| If true and \&quot;refer_to\&quot; refers to an Asterisk endpoint, the \&quot;refer_to\&quot; value is set to point to this Asterisk endpoint - so the referee is referred to Asterisk. Otherwise, use the contact URI associated with the endpoint. | [optional] [default to false]
 **variables** | [**\Swagger\Client\Model\Containers**](../Model/Containers.md)| The \&quot;variables\&quot; key in the body object holds technology specific key/value pairs to append to the message. These can be interpreted and used by the various resource types; for example, the pjsip resource type will add the key/value pairs as SIP headers, | [optional]

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

$apiInstance = new Swagger\Client\Api\ApiDocsendpointsFormatApi(
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
    echo 'Exception when calling ApiDocsendpointsFormatApi->sendMessage: ', $e->getMessage(), PHP_EOL;
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

$apiInstance = new Swagger\Client\Api\ApiDocsendpointsFormatApi(
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
    echo 'Exception when calling ApiDocsendpointsFormatApi->sendMessageToEndpoint: ', $e->getMessage(), PHP_EOL;
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

