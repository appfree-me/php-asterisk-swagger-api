# Swagger\Client\ChannelsFormatApi

All URIs are relative to *http://localhost:8088/ari*

Method | HTTP request | Description
------------- | ------------- | -------------
[**answer**](ChannelsFormatApi.md#answer) | **POST** /channels/{channelId}/answer | Answer a channel.
[**callList**](ChannelsFormatApi.md#callList) | **GET** /channels | List all active channels in Asterisk.
[**continueInDialplan**](ChannelsFormatApi.md#continueInDialplan) | **POST** /channels/{channelId}/continue | Exit application; continue execution in the dialplan.
[**create**](ChannelsFormatApi.md#create) | **POST** /channels/create | Create channel.
[**dial**](ChannelsFormatApi.md#dial) | **POST** /channels/{channelId}/dial | Dial a created channel.
[**externalMedia**](ChannelsFormatApi.md#externalMedia) | **POST** /channels/externalMedia | Start an External Media session.
[**get**](ChannelsFormatApi.md#get) | **GET** /channels/{channelId} | Channel details.
[**getChannelVar**](ChannelsFormatApi.md#getChannelVar) | **GET** /channels/{channelId}/variable | Get the value of a channel variable or function.
[**hangup**](ChannelsFormatApi.md#hangup) | **DELETE** /channels/{channelId} | Delete (i.e. hangup) a channel.
[**hold**](ChannelsFormatApi.md#hold) | **POST** /channels/{channelId}/hold | Hold a channel.
[**move**](ChannelsFormatApi.md#move) | **POST** /channels/{channelId}/move | Move the channel from one Stasis application to another.
[**mute**](ChannelsFormatApi.md#mute) | **POST** /channels/{channelId}/mute | Mute a channel.
[**originate**](ChannelsFormatApi.md#originate) | **POST** /channels | Create a new channel (originate).
[**originateWithId**](ChannelsFormatApi.md#originateWithId) | **POST** /channels/{channelId} | Create a new channel (originate with id).
[**play**](ChannelsFormatApi.md#play) | **POST** /channels/{channelId}/play | Start playback of media.
[**playWithId**](ChannelsFormatApi.md#playWithId) | **POST** /channels/{channelId}/play/{playbackId} | Start playback of media and specify the playbackId.
[**record**](ChannelsFormatApi.md#record) | **POST** /channels/{channelId}/record | Start a recording.
[**redirect**](ChannelsFormatApi.md#redirect) | **POST** /channels/{channelId}/redirect | Redirect the channel to a different location.
[**ring**](ChannelsFormatApi.md#ring) | **POST** /channels/{channelId}/ring | Indicate ringing to a channel.
[**ringStop**](ChannelsFormatApi.md#ringStop) | **DELETE** /channels/{channelId}/ring | Stop ringing indication on a channel if locally generated.
[**rtpstatistics**](ChannelsFormatApi.md#rtpstatistics) | **GET** /channels/{channelId}/rtp_statistics | RTP stats on a channel.
[**sendDTMF**](ChannelsFormatApi.md#sendDTMF) | **POST** /channels/{channelId}/dtmf | Send provided DTMF to a given channel.
[**setChannelVar**](ChannelsFormatApi.md#setChannelVar) | **POST** /channels/{channelId}/variable | Set the value of a channel variable or function.
[**snoopChannel**](ChannelsFormatApi.md#snoopChannel) | **POST** /channels/{channelId}/snoop | Start snooping.
[**snoopChannelWithId**](ChannelsFormatApi.md#snoopChannelWithId) | **POST** /channels/{channelId}/snoop/{snoopId} | Start snooping.
[**startMoh**](ChannelsFormatApi.md#startMoh) | **POST** /channels/{channelId}/moh | Play music on hold to a channel.
[**startSilence**](ChannelsFormatApi.md#startSilence) | **POST** /channels/{channelId}/silence | Play silence to a channel.
[**stopMoh**](ChannelsFormatApi.md#stopMoh) | **DELETE** /channels/{channelId}/moh | Stop playing music on hold to a channel.
[**stopSilence**](ChannelsFormatApi.md#stopSilence) | **DELETE** /channels/{channelId}/silence | Stop playing silence to a channel.
[**unhold**](ChannelsFormatApi.md#unhold) | **DELETE** /channels/{channelId}/hold | Remove a channel from hold.
[**unmute**](ChannelsFormatApi.md#unmute) | **DELETE** /channels/{channelId}/mute | Unmute a channel.


# **answer**
> answer($channel_id)

Answer a channel.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ChannelsFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$channel_id = "channel_id_example"; // string | Channel's id

try {
    $apiInstance->answer($channel_id);
} catch (Exception $e) {
    echo 'Exception when calling ChannelsFormatApi->answer: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **channel_id** | **string**| Channel&#39;s id |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **callList**
> callList()

List all active channels in Asterisk.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ChannelsFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $apiInstance->callList();
} catch (Exception $e) {
    echo 'Exception when calling ChannelsFormatApi->callList: ', $e->getMessage(), PHP_EOL;
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

# **continueInDialplan**
> continueInDialplan($channel_id, $context, $extension, $priority, $label)

Exit application; continue execution in the dialplan.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ChannelsFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$channel_id = "channel_id_example"; // string | Channel's id
$context = "context_example"; // string | The context to continue to.
$extension = "extension_example"; // string | The extension to continue to.
$priority = 56; // int | The priority to continue to.
$label = "label_example"; // string | The label to continue to - will supersede 'priority' if both are provided.

try {
    $apiInstance->continueInDialplan($channel_id, $context, $extension, $priority, $label);
} catch (Exception $e) {
    echo 'Exception when calling ChannelsFormatApi->continueInDialplan: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **channel_id** | **string**| Channel&#39;s id |
 **context** | **string**| The context to continue to. | [optional]
 **extension** | **string**| The extension to continue to. | [optional]
 **priority** | **int**| The priority to continue to. | [optional]
 **label** | **string**| The label to continue to - will supersede &#39;priority&#39; if both are provided. | [optional]

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **create**
> create($endpoint, $app, $app_args, $channel_id, $other_channel_id, $originator, $formats, $variables)

Create channel.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ChannelsFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$endpoint = "endpoint_example"; // string | Endpoint for channel communication
$app = "app_example"; // string | Stasis Application to place channel into
$app_args = "app_args_example"; // string | The application arguments to pass to the Stasis application provided by 'app'. Mutually exclusive with 'context', 'extension', 'priority', and 'label'.
$channel_id = "channel_id_example"; // string | The unique id to assign the channel on creation.
$other_channel_id = "other_channel_id_example"; // string | The unique id to assign the second channel when using local channels.
$originator = "originator_example"; // string | Unique ID of the calling channel
$formats = "formats_example"; // string | The format name capability list to use if originator is not specified. Ex. \"ulaw,slin16\".  Format names can be found with \"core show codecs\".
$variables = new \Swagger\Client\Model\Containers(); // \Swagger\Client\Model\Containers | The \"variables\" key in the body object holds variable key/value pairs to set on the channel on creation. Other keys in the body object are interpreted as query parameters. Ex. { \"endpoint\": \"SIP/Alice\", \"variables\": { \"CALLERID(name)\": \"Alice\" } }

try {
    $apiInstance->create($endpoint, $app, $app_args, $channel_id, $other_channel_id, $originator, $formats, $variables);
} catch (Exception $e) {
    echo 'Exception when calling ChannelsFormatApi->create: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **endpoint** | **string**| Endpoint for channel communication |
 **app** | **string**| Stasis Application to place channel into |
 **app_args** | **string**| The application arguments to pass to the Stasis application provided by &#39;app&#39;. Mutually exclusive with &#39;context&#39;, &#39;extension&#39;, &#39;priority&#39;, and &#39;label&#39;. | [optional]
 **channel_id** | **string**| The unique id to assign the channel on creation. | [optional]
 **other_channel_id** | **string**| The unique id to assign the second channel when using local channels. | [optional]
 **originator** | **string**| Unique ID of the calling channel | [optional]
 **formats** | **string**| The format name capability list to use if originator is not specified. Ex. \&quot;ulaw,slin16\&quot;.  Format names can be found with \&quot;core show codecs\&quot;. | [optional]
 **variables** | [**\Swagger\Client\Model\Containers**](../Model/Containers.md)| The \&quot;variables\&quot; key in the body object holds variable key/value pairs to set on the channel on creation. Other keys in the body object are interpreted as query parameters. Ex. { \&quot;endpoint\&quot;: \&quot;SIP/Alice\&quot;, \&quot;variables\&quot;: { \&quot;CALLERID(name)\&quot;: \&quot;Alice\&quot; } } | [optional]

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **dial**
> dial($channel_id, $caller, $timeout)

Dial a created channel.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ChannelsFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$channel_id = "channel_id_example"; // string | Channel's id
$caller = "caller_example"; // string | Channel ID of caller
$timeout = 0; // int | Dial timeout

try {
    $apiInstance->dial($channel_id, $caller, $timeout);
} catch (Exception $e) {
    echo 'Exception when calling ChannelsFormatApi->dial: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **channel_id** | **string**| Channel&#39;s id |
 **caller** | **string**| Channel ID of caller | [optional]
 **timeout** | **int**| Dial timeout | [optional] [default to 0]

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **externalMedia**
> externalMedia($app, $external_host, $format, $channel_id, $variables, $encapsulation, $transport, $connection_type, $direction, $data)

Start an External Media session.

Create a channel to an External Media source/sink.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ChannelsFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$app = "app_example"; // string | Stasis Application to place channel into
$external_host = "external_host_example"; // string | Hostname/ip:port of external host
$format = "format_example"; // string | Format to encode audio in
$channel_id = "channel_id_example"; // string | The unique id to assign the channel on creation.
$variables = new \Swagger\Client\Model\Containers(); // \Swagger\Client\Model\Containers | The \"variables\" key in the body object holds variable key/value pairs to set on the channel on creation. Other keys in the body object are interpreted as query parameters. Ex. { \"endpoint\": \"SIP/Alice\", \"variables\": { \"CALLERID(name)\": \"Alice\" } }
$encapsulation = "rtp"; // string | Payload encapsulation protocol
$transport = "udp"; // string | Transport protocol
$connection_type = "client"; // string | Connection type (client/server)
$direction = "both"; // string | External media direction
$data = "data_example"; // string | An arbitrary data field

try {
    $apiInstance->externalMedia($app, $external_host, $format, $channel_id, $variables, $encapsulation, $transport, $connection_type, $direction, $data);
} catch (Exception $e) {
    echo 'Exception when calling ChannelsFormatApi->externalMedia: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **app** | **string**| Stasis Application to place channel into |
 **external_host** | **string**| Hostname/ip:port of external host |
 **format** | **string**| Format to encode audio in |
 **channel_id** | **string**| The unique id to assign the channel on creation. | [optional]
 **variables** | [**\Swagger\Client\Model\Containers**](../Model/Containers.md)| The \&quot;variables\&quot; key in the body object holds variable key/value pairs to set on the channel on creation. Other keys in the body object are interpreted as query parameters. Ex. { \&quot;endpoint\&quot;: \&quot;SIP/Alice\&quot;, \&quot;variables\&quot;: { \&quot;CALLERID(name)\&quot;: \&quot;Alice\&quot; } } | [optional]
 **encapsulation** | **string**| Payload encapsulation protocol | [optional] [default to rtp]
 **transport** | **string**| Transport protocol | [optional] [default to udp]
 **connection_type** | **string**| Connection type (client/server) | [optional] [default to client]
 **direction** | **string**| External media direction | [optional] [default to both]
 **data** | **string**| An arbitrary data field | [optional]

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **get**
> get($channel_id)

Channel details.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ChannelsFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$channel_id = "channel_id_example"; // string | Channel's id

try {
    $apiInstance->get($channel_id);
} catch (Exception $e) {
    echo 'Exception when calling ChannelsFormatApi->get: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **channel_id** | **string**| Channel&#39;s id |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getChannelVar**
> getChannelVar($channel_id, $variable)

Get the value of a channel variable or function.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ChannelsFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$channel_id = "channel_id_example"; // string | Channel's id
$variable = "variable_example"; // string | The channel variable or function to get

try {
    $apiInstance->getChannelVar($channel_id, $variable);
} catch (Exception $e) {
    echo 'Exception when calling ChannelsFormatApi->getChannelVar: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **channel_id** | **string**| Channel&#39;s id |
 **variable** | **string**| The channel variable or function to get |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **hangup**
> hangup($channel_id, $reason_code, $reason)

Delete (i.e. hangup) a channel.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ChannelsFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$channel_id = "channel_id_example"; // string | Channel's id
$reason_code = "reason_code_example"; // string | The reason code for hanging up the channel for detail use. Mutually exclusive with 'reason'. See detail hangup codes at here. https://wiki.asterisk.org/wiki/display/AST/Hangup+Cause+Mappings
$reason = "reason_example"; // string | Reason for hanging up the channel for simple use. Mutually exclusive with 'reason_code'.

try {
    $apiInstance->hangup($channel_id, $reason_code, $reason);
} catch (Exception $e) {
    echo 'Exception when calling ChannelsFormatApi->hangup: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **channel_id** | **string**| Channel&#39;s id |
 **reason_code** | **string**| The reason code for hanging up the channel for detail use. Mutually exclusive with &#39;reason&#39;. See detail hangup codes at here. https://wiki.asterisk.org/wiki/display/AST/Hangup+Cause+Mappings | [optional]
 **reason** | **string**| Reason for hanging up the channel for simple use. Mutually exclusive with &#39;reason_code&#39;. | [optional]

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **hold**
> hold($channel_id)

Hold a channel.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ChannelsFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$channel_id = "channel_id_example"; // string | Channel's id

try {
    $apiInstance->hold($channel_id);
} catch (Exception $e) {
    echo 'Exception when calling ChannelsFormatApi->hold: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **channel_id** | **string**| Channel&#39;s id |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **move**
> move($channel_id, $app, $app_args)

Move the channel from one Stasis application to another.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ChannelsFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$channel_id = "channel_id_example"; // string | Channel's id
$app = "app_example"; // string | The channel will be passed to this Stasis application.
$app_args = "app_args_example"; // string | The application arguments to pass to the Stasis application provided by 'app'.

try {
    $apiInstance->move($channel_id, $app, $app_args);
} catch (Exception $e) {
    echo 'Exception when calling ChannelsFormatApi->move: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **channel_id** | **string**| Channel&#39;s id |
 **app** | **string**| The channel will be passed to this Stasis application. |
 **app_args** | **string**| The application arguments to pass to the Stasis application provided by &#39;app&#39;. | [optional]

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **mute**
> mute($channel_id, $direction)

Mute a channel.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ChannelsFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$channel_id = "channel_id_example"; // string | Channel's id
$direction = "both"; // string | Direction in which to mute audio

try {
    $apiInstance->mute($channel_id, $direction);
} catch (Exception $e) {
    echo 'Exception when calling ChannelsFormatApi->mute: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **channel_id** | **string**| Channel&#39;s id |
 **direction** | **string**| Direction in which to mute audio | [optional] [default to both]

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **originate**
> originate($endpoint, $extension, $context, $priority, $label, $app, $app_args, $caller_id, $timeout, $variables, $channel_id, $other_channel_id, $originator, $formats)

Create a new channel (originate).

The new channel is created immediately and a snapshot of it returned. If a Stasis application is provided it will be automatically subscribed to the originated channel for further events and updates.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ChannelsFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$endpoint = "endpoint_example"; // string | Endpoint to call.
$extension = "extension_example"; // string | The extension to dial after the endpoint answers. Mutually exclusive with 'app'.
$context = "context_example"; // string | The context to dial after the endpoint answers. If omitted, uses 'default'. Mutually exclusive with 'app'.
$priority = 789; // int | The priority to dial after the endpoint answers. If omitted, uses 1. Mutually exclusive with 'app'.
$label = "label_example"; // string | The label to dial after the endpoint answers. Will supersede 'priority' if provided. Mutually exclusive with 'app'.
$app = "app_example"; // string | The application that is subscribed to the originated channel. When the channel is answered, it will be passed to this Stasis application. Mutually exclusive with 'context', 'extension', 'priority', and 'label'.
$app_args = "app_args_example"; // string | The application arguments to pass to the Stasis application provided by 'app'. Mutually exclusive with 'context', 'extension', 'priority', and 'label'.
$caller_id = "caller_id_example"; // string | CallerID to use when dialing the endpoint or extension.
$timeout = 30; // int | Timeout (in seconds) before giving up dialing, or -1 for no timeout.
$variables = new \Swagger\Client\Model\Containers(); // \Swagger\Client\Model\Containers | The \"variables\" key in the body object holds variable key/value pairs to set on the channel on creation. Other keys in the body object are interpreted as query parameters. Ex. { \"endpoint\": \"SIP/Alice\", \"variables\": { \"CALLERID(name)\": \"Alice\" } }
$channel_id = "channel_id_example"; // string | The unique id to assign the channel on creation.
$other_channel_id = "other_channel_id_example"; // string | The unique id to assign the second channel when using local channels.
$originator = "originator_example"; // string | The unique id of the channel which is originating this one.
$formats = "formats_example"; // string | The format name capability list to use if originator is not specified. Ex. \"ulaw,slin16\".  Format names can be found with \"core show codecs\".

try {
    $apiInstance->originate($endpoint, $extension, $context, $priority, $label, $app, $app_args, $caller_id, $timeout, $variables, $channel_id, $other_channel_id, $originator, $formats);
} catch (Exception $e) {
    echo 'Exception when calling ChannelsFormatApi->originate: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **endpoint** | **string**| Endpoint to call. |
 **extension** | **string**| The extension to dial after the endpoint answers. Mutually exclusive with &#39;app&#39;. | [optional]
 **context** | **string**| The context to dial after the endpoint answers. If omitted, uses &#39;default&#39;. Mutually exclusive with &#39;app&#39;. | [optional]
 **priority** | **int**| The priority to dial after the endpoint answers. If omitted, uses 1. Mutually exclusive with &#39;app&#39;. | [optional]
 **label** | **string**| The label to dial after the endpoint answers. Will supersede &#39;priority&#39; if provided. Mutually exclusive with &#39;app&#39;. | [optional]
 **app** | **string**| The application that is subscribed to the originated channel. When the channel is answered, it will be passed to this Stasis application. Mutually exclusive with &#39;context&#39;, &#39;extension&#39;, &#39;priority&#39;, and &#39;label&#39;. | [optional]
 **app_args** | **string**| The application arguments to pass to the Stasis application provided by &#39;app&#39;. Mutually exclusive with &#39;context&#39;, &#39;extension&#39;, &#39;priority&#39;, and &#39;label&#39;. | [optional]
 **caller_id** | **string**| CallerID to use when dialing the endpoint or extension. | [optional]
 **timeout** | **int**| Timeout (in seconds) before giving up dialing, or -1 for no timeout. | [optional] [default to 30]
 **variables** | [**\Swagger\Client\Model\Containers**](../Model/Containers.md)| The \&quot;variables\&quot; key in the body object holds variable key/value pairs to set on the channel on creation. Other keys in the body object are interpreted as query parameters. Ex. { \&quot;endpoint\&quot;: \&quot;SIP/Alice\&quot;, \&quot;variables\&quot;: { \&quot;CALLERID(name)\&quot;: \&quot;Alice\&quot; } } | [optional]
 **channel_id** | **string**| The unique id to assign the channel on creation. | [optional]
 **other_channel_id** | **string**| The unique id to assign the second channel when using local channels. | [optional]
 **originator** | **string**| The unique id of the channel which is originating this one. | [optional]
 **formats** | **string**| The format name capability list to use if originator is not specified. Ex. \&quot;ulaw,slin16\&quot;.  Format names can be found with \&quot;core show codecs\&quot;. | [optional]

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **originateWithId**
> originateWithId($channel_id, $endpoint, $extension, $context, $priority, $label, $app, $app_args, $caller_id, $timeout, $variables, $other_channel_id, $originator, $formats)

Create a new channel (originate with id).

The new channel is created immediately and a snapshot of it returned. If a Stasis application is provided it will be automatically subscribed to the originated channel for further events and updates.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ChannelsFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$channel_id = "channel_id_example"; // string | The unique id to assign the channel on creation.
$endpoint = "endpoint_example"; // string | Endpoint to call.
$extension = "extension_example"; // string | The extension to dial after the endpoint answers. Mutually exclusive with 'app'.
$context = "context_example"; // string | The context to dial after the endpoint answers. If omitted, uses 'default'. Mutually exclusive with 'app'.
$priority = 789; // int | The priority to dial after the endpoint answers. If omitted, uses 1. Mutually exclusive with 'app'.
$label = "label_example"; // string | The label to dial after the endpoint answers. Will supersede 'priority' if provided. Mutually exclusive with 'app'.
$app = "app_example"; // string | The application that is subscribed to the originated channel. When the channel is answered, it will be passed to this Stasis application. Mutually exclusive with 'context', 'extension', 'priority', and 'label'.
$app_args = "app_args_example"; // string | The application arguments to pass to the Stasis application provided by 'app'. Mutually exclusive with 'context', 'extension', 'priority', and 'label'.
$caller_id = "caller_id_example"; // string | CallerID to use when dialing the endpoint or extension.
$timeout = 30; // int | Timeout (in seconds) before giving up dialing, or -1 for no timeout.
$variables = new \Swagger\Client\Model\Containers(); // \Swagger\Client\Model\Containers | The \"variables\" key in the body object holds variable key/value pairs to set on the channel on creation. Other keys in the body object are interpreted as query parameters. Ex. { \"endpoint\": \"SIP/Alice\", \"variables\": { \"CALLERID(name)\": \"Alice\" } }
$other_channel_id = "other_channel_id_example"; // string | The unique id to assign the second channel when using local channels.
$originator = "originator_example"; // string | The unique id of the channel which is originating this one.
$formats = "formats_example"; // string | The format name capability list to use if originator is not specified. Ex. \"ulaw,slin16\".  Format names can be found with \"core show codecs\".

try {
    $apiInstance->originateWithId($channel_id, $endpoint, $extension, $context, $priority, $label, $app, $app_args, $caller_id, $timeout, $variables, $other_channel_id, $originator, $formats);
} catch (Exception $e) {
    echo 'Exception when calling ChannelsFormatApi->originateWithId: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **channel_id** | **string**| The unique id to assign the channel on creation. |
 **endpoint** | **string**| Endpoint to call. |
 **extension** | **string**| The extension to dial after the endpoint answers. Mutually exclusive with &#39;app&#39;. | [optional]
 **context** | **string**| The context to dial after the endpoint answers. If omitted, uses &#39;default&#39;. Mutually exclusive with &#39;app&#39;. | [optional]
 **priority** | **int**| The priority to dial after the endpoint answers. If omitted, uses 1. Mutually exclusive with &#39;app&#39;. | [optional]
 **label** | **string**| The label to dial after the endpoint answers. Will supersede &#39;priority&#39; if provided. Mutually exclusive with &#39;app&#39;. | [optional]
 **app** | **string**| The application that is subscribed to the originated channel. When the channel is answered, it will be passed to this Stasis application. Mutually exclusive with &#39;context&#39;, &#39;extension&#39;, &#39;priority&#39;, and &#39;label&#39;. | [optional]
 **app_args** | **string**| The application arguments to pass to the Stasis application provided by &#39;app&#39;. Mutually exclusive with &#39;context&#39;, &#39;extension&#39;, &#39;priority&#39;, and &#39;label&#39;. | [optional]
 **caller_id** | **string**| CallerID to use when dialing the endpoint or extension. | [optional]
 **timeout** | **int**| Timeout (in seconds) before giving up dialing, or -1 for no timeout. | [optional] [default to 30]
 **variables** | [**\Swagger\Client\Model\Containers**](../Model/Containers.md)| The \&quot;variables\&quot; key in the body object holds variable key/value pairs to set on the channel on creation. Other keys in the body object are interpreted as query parameters. Ex. { \&quot;endpoint\&quot;: \&quot;SIP/Alice\&quot;, \&quot;variables\&quot;: { \&quot;CALLERID(name)\&quot;: \&quot;Alice\&quot; } } | [optional]
 **other_channel_id** | **string**| The unique id to assign the second channel when using local channels. | [optional]
 **originator** | **string**| The unique id of the channel which is originating this one. | [optional]
 **formats** | **string**| The format name capability list to use if originator is not specified. Ex. \&quot;ulaw,slin16\&quot;.  Format names can be found with \&quot;core show codecs\&quot;. | [optional]

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **play**
> play($channel_id, $media, $lang, $offsetms, $skipms, $playback_id)

Start playback of media.

The media URI may be any of a number of URI's. Currently sound:, recording:, number:, digits:, characters:, and tone: URI's are supported. This operation creates a playback resource that can be used to control the playback of media (pause, rewind, fast forward, etc.)

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ChannelsFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$channel_id = "channel_id_example"; // string | Channel's id
$media = array("media_example"); // string[] | Media URIs to play.
$lang = "lang_example"; // string | For sounds, selects language for sound.
$offsetms = 56; // int | Number of milliseconds to skip before playing. Only applies to the first URI if multiple media URIs are specified.
$skipms = 3000; // int | Number of milliseconds to skip for forward/reverse operations.
$playback_id = "playback_id_example"; // string | Playback ID.

try {
    $apiInstance->play($channel_id, $media, $lang, $offsetms, $skipms, $playback_id);
} catch (Exception $e) {
    echo 'Exception when calling ChannelsFormatApi->play: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **channel_id** | **string**| Channel&#39;s id |
 **media** | [**string[]**](../Model/string.md)| Media URIs to play. |
 **lang** | **string**| For sounds, selects language for sound. | [optional]
 **offsetms** | **int**| Number of milliseconds to skip before playing. Only applies to the first URI if multiple media URIs are specified. | [optional]
 **skipms** | **int**| Number of milliseconds to skip for forward/reverse operations. | [optional] [default to 3000]
 **playback_id** | **string**| Playback ID. | [optional]

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **playWithId**
> playWithId($channel_id, $playback_id, $media, $lang, $offsetms, $skipms)

Start playback of media and specify the playbackId.

The media URI may be any of a number of URI's. Currently sound:, recording:, number:, digits:, characters:, and tone: URI's are supported. This operation creates a playback resource that can be used to control the playback of media (pause, rewind, fast forward, etc.)

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ChannelsFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$channel_id = "channel_id_example"; // string | Channel's id
$playback_id = "playback_id_example"; // string | Playback ID.
$media = array("media_example"); // string[] | Media URIs to play.
$lang = "lang_example"; // string | For sounds, selects language for sound.
$offsetms = 56; // int | Number of milliseconds to skip before playing. Only applies to the first URI if multiple media URIs are specified.
$skipms = 3000; // int | Number of milliseconds to skip for forward/reverse operations.

try {
    $apiInstance->playWithId($channel_id, $playback_id, $media, $lang, $offsetms, $skipms);
} catch (Exception $e) {
    echo 'Exception when calling ChannelsFormatApi->playWithId: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **channel_id** | **string**| Channel&#39;s id |
 **playback_id** | **string**| Playback ID. |
 **media** | [**string[]**](../Model/string.md)| Media URIs to play. |
 **lang** | **string**| For sounds, selects language for sound. | [optional]
 **offsetms** | **int**| Number of milliseconds to skip before playing. Only applies to the first URI if multiple media URIs are specified. | [optional]
 **skipms** | **int**| Number of milliseconds to skip for forward/reverse operations. | [optional] [default to 3000]

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **record**
> record($channel_id, $name, $format, $max_duration_seconds, $max_silence_seconds, $if_exists, $beep, $terminate_on)

Start a recording.

Record audio from a channel. Note that this will not capture audio sent to the channel. The bridge itself has a record feature if that's what you want.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ChannelsFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$channel_id = "channel_id_example"; // string | Channel's id
$name = "name_example"; // string | Recording's filename
$format = "format_example"; // string | Format to encode audio in
$max_duration_seconds = 0; // int | Maximum duration of the recording, in seconds. 0 for no limit
$max_silence_seconds = 0; // int | Maximum duration of silence, in seconds. 0 for no limit
$if_exists = "fail"; // string | Action to take if a recording with the same name already exists.
$beep = false; // bool | Play beep when recording begins
$terminate_on = "none"; // string | DTMF input to terminate recording

try {
    $apiInstance->record($channel_id, $name, $format, $max_duration_seconds, $max_silence_seconds, $if_exists, $beep, $terminate_on);
} catch (Exception $e) {
    echo 'Exception when calling ChannelsFormatApi->record: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **channel_id** | **string**| Channel&#39;s id |
 **name** | **string**| Recording&#39;s filename |
 **format** | **string**| Format to encode audio in |
 **max_duration_seconds** | **int**| Maximum duration of the recording, in seconds. 0 for no limit | [optional] [default to 0]
 **max_silence_seconds** | **int**| Maximum duration of silence, in seconds. 0 for no limit | [optional] [default to 0]
 **if_exists** | **string**| Action to take if a recording with the same name already exists. | [optional] [default to fail]
 **beep** | **bool**| Play beep when recording begins | [optional] [default to false]
 **terminate_on** | **string**| DTMF input to terminate recording | [optional] [default to none]

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **redirect**
> redirect($channel_id, $endpoint)

Redirect the channel to a different location.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ChannelsFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$channel_id = "channel_id_example"; // string | Channel's id
$endpoint = "endpoint_example"; // string | The endpoint to redirect the channel to

try {
    $apiInstance->redirect($channel_id, $endpoint);
} catch (Exception $e) {
    echo 'Exception when calling ChannelsFormatApi->redirect: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **channel_id** | **string**| Channel&#39;s id |
 **endpoint** | **string**| The endpoint to redirect the channel to |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **ring**
> ring($channel_id)

Indicate ringing to a channel.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ChannelsFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$channel_id = "channel_id_example"; // string | Channel's id

try {
    $apiInstance->ring($channel_id);
} catch (Exception $e) {
    echo 'Exception when calling ChannelsFormatApi->ring: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **channel_id** | **string**| Channel&#39;s id |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **ringStop**
> ringStop($channel_id)

Stop ringing indication on a channel if locally generated.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ChannelsFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$channel_id = "channel_id_example"; // string | Channel's id

try {
    $apiInstance->ringStop($channel_id);
} catch (Exception $e) {
    echo 'Exception when calling ChannelsFormatApi->ringStop: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **channel_id** | **string**| Channel&#39;s id |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **rtpstatistics**
> rtpstatistics($channel_id)

RTP stats on a channel.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ChannelsFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$channel_id = "channel_id_example"; // string | Channel's id

try {
    $apiInstance->rtpstatistics($channel_id);
} catch (Exception $e) {
    echo 'Exception when calling ChannelsFormatApi->rtpstatistics: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **channel_id** | **string**| Channel&#39;s id |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **sendDTMF**
> sendDTMF($channel_id, $dtmf, $before, $between, $duration, $after)

Send provided DTMF to a given channel.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ChannelsFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$channel_id = "channel_id_example"; // string | Channel's id
$dtmf = "dtmf_example"; // string | DTMF To send.
$before = 0; // int | Amount of time to wait before DTMF digits (specified in milliseconds) start.
$between = 100; // int | Amount of time in between DTMF digits (specified in milliseconds).
$duration = 100; // int | Length of each DTMF digit (specified in milliseconds).
$after = 0; // int | Amount of time to wait after DTMF digits (specified in milliseconds) end.

try {
    $apiInstance->sendDTMF($channel_id, $dtmf, $before, $between, $duration, $after);
} catch (Exception $e) {
    echo 'Exception when calling ChannelsFormatApi->sendDTMF: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **channel_id** | **string**| Channel&#39;s id |
 **dtmf** | **string**| DTMF To send. | [optional]
 **before** | **int**| Amount of time to wait before DTMF digits (specified in milliseconds) start. | [optional] [default to 0]
 **between** | **int**| Amount of time in between DTMF digits (specified in milliseconds). | [optional] [default to 100]
 **duration** | **int**| Length of each DTMF digit (specified in milliseconds). | [optional] [default to 100]
 **after** | **int**| Amount of time to wait after DTMF digits (specified in milliseconds) end. | [optional] [default to 0]

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **setChannelVar**
> setChannelVar($channel_id, $variable, $value)

Set the value of a channel variable or function.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ChannelsFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$channel_id = "channel_id_example"; // string | Channel's id
$variable = "variable_example"; // string | The channel variable or function to set
$value = "value_example"; // string | The value to set the variable to

try {
    $apiInstance->setChannelVar($channel_id, $variable, $value);
} catch (Exception $e) {
    echo 'Exception when calling ChannelsFormatApi->setChannelVar: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **channel_id** | **string**| Channel&#39;s id |
 **variable** | **string**| The channel variable or function to set |
 **value** | **string**| The value to set the variable to | [optional]

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **snoopChannel**
> snoopChannel($channel_id, $app, $spy, $whisper, $app_args, $snoop_id)

Start snooping.

Snoop (spy/whisper) on a specific channel.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ChannelsFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$channel_id = "channel_id_example"; // string | Channel's id
$app = "app_example"; // string | Application the snooping channel is placed into
$spy = "none"; // string | Direction of audio to spy on
$whisper = "none"; // string | Direction of audio to whisper into
$app_args = "app_args_example"; // string | The application arguments to pass to the Stasis application
$snoop_id = "snoop_id_example"; // string | Unique ID to assign to snooping channel

try {
    $apiInstance->snoopChannel($channel_id, $app, $spy, $whisper, $app_args, $snoop_id);
} catch (Exception $e) {
    echo 'Exception when calling ChannelsFormatApi->snoopChannel: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **channel_id** | **string**| Channel&#39;s id |
 **app** | **string**| Application the snooping channel is placed into |
 **spy** | **string**| Direction of audio to spy on | [optional] [default to none]
 **whisper** | **string**| Direction of audio to whisper into | [optional] [default to none]
 **app_args** | **string**| The application arguments to pass to the Stasis application | [optional]
 **snoop_id** | **string**| Unique ID to assign to snooping channel | [optional]

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **snoopChannelWithId**
> snoopChannelWithId($channel_id, $snoop_id, $app, $spy, $whisper, $app_args)

Start snooping.

Snoop (spy/whisper) on a specific channel.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ChannelsFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$channel_id = "channel_id_example"; // string | Channel's id
$snoop_id = "snoop_id_example"; // string | Unique ID to assign to snooping channel
$app = "app_example"; // string | Application the snooping channel is placed into
$spy = "none"; // string | Direction of audio to spy on
$whisper = "none"; // string | Direction of audio to whisper into
$app_args = "app_args_example"; // string | The application arguments to pass to the Stasis application

try {
    $apiInstance->snoopChannelWithId($channel_id, $snoop_id, $app, $spy, $whisper, $app_args);
} catch (Exception $e) {
    echo 'Exception when calling ChannelsFormatApi->snoopChannelWithId: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **channel_id** | **string**| Channel&#39;s id |
 **snoop_id** | **string**| Unique ID to assign to snooping channel |
 **app** | **string**| Application the snooping channel is placed into |
 **spy** | **string**| Direction of audio to spy on | [optional] [default to none]
 **whisper** | **string**| Direction of audio to whisper into | [optional] [default to none]
 **app_args** | **string**| The application arguments to pass to the Stasis application | [optional]

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **startMoh**
> startMoh($channel_id, $moh_class)

Play music on hold to a channel.

Using media operations such as /play on a channel playing MOH in this manner will suspend MOH without resuming automatically. If continuing music on hold is desired, the stasis application must reinitiate music on hold.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ChannelsFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$channel_id = "channel_id_example"; // string | Channel's id
$moh_class = "moh_class_example"; // string | Music on hold class to use

try {
    $apiInstance->startMoh($channel_id, $moh_class);
} catch (Exception $e) {
    echo 'Exception when calling ChannelsFormatApi->startMoh: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **channel_id** | **string**| Channel&#39;s id |
 **moh_class** | **string**| Music on hold class to use | [optional]

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **startSilence**
> startSilence($channel_id)

Play silence to a channel.

Using media operations such as /play on a channel playing silence in this manner will suspend silence without resuming automatically.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ChannelsFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$channel_id = "channel_id_example"; // string | Channel's id

try {
    $apiInstance->startSilence($channel_id);
} catch (Exception $e) {
    echo 'Exception when calling ChannelsFormatApi->startSilence: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **channel_id** | **string**| Channel&#39;s id |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **stopMoh**
> stopMoh($channel_id)

Stop playing music on hold to a channel.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ChannelsFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$channel_id = "channel_id_example"; // string | Channel's id

try {
    $apiInstance->stopMoh($channel_id);
} catch (Exception $e) {
    echo 'Exception when calling ChannelsFormatApi->stopMoh: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **channel_id** | **string**| Channel&#39;s id |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **stopSilence**
> stopSilence($channel_id)

Stop playing silence to a channel.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ChannelsFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$channel_id = "channel_id_example"; // string | Channel's id

try {
    $apiInstance->stopSilence($channel_id);
} catch (Exception $e) {
    echo 'Exception when calling ChannelsFormatApi->stopSilence: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **channel_id** | **string**| Channel&#39;s id |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **unhold**
> unhold($channel_id)

Remove a channel from hold.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ChannelsFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$channel_id = "channel_id_example"; // string | Channel's id

try {
    $apiInstance->unhold($channel_id);
} catch (Exception $e) {
    echo 'Exception when calling ChannelsFormatApi->unhold: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **channel_id** | **string**| Channel&#39;s id |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **unmute**
> unmute($channel_id, $direction)

Unmute a channel.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ChannelsFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$channel_id = "channel_id_example"; // string | Channel's id
$direction = "both"; // string | Direction in which to unmute audio

try {
    $apiInstance->unmute($channel_id, $direction);
} catch (Exception $e) {
    echo 'Exception when calling ChannelsFormatApi->unmute: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **channel_id** | **string**| Channel&#39;s id |
 **direction** | **string**| Direction in which to unmute audio | [optional] [default to both]

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

