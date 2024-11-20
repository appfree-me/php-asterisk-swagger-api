# Swagger\Client\ApiDocsbridgesFormatApi

All URIs are relative to *http://localhost:18088/ari*

Method | HTTP request | Description
------------- | ------------- | -------------
[**addChannel**](ApiDocsbridgesFormatApi.md#addChannel) | **POST** /bridges/{bridgeId}/addChannel | Add a channel to a bridge.
[**callList**](ApiDocsbridgesFormatApi.md#callList) | **GET** /bridges | List all active bridges in Asterisk.
[**clearVideoSource**](ApiDocsbridgesFormatApi.md#clearVideoSource) | **DELETE** /bridges/{bridgeId}/videoSource | Removes any explicit video source in a multi-party mixing bridge. This operation has no effect on bridges with two or fewer participants. When no explicit video source is set, talk detection will be used to determine the active video stream.
[**create**](ApiDocsbridgesFormatApi.md#create) | **POST** /bridges | Create a new bridge.
[**createWithId**](ApiDocsbridgesFormatApi.md#createWithId) | **POST** /bridges/{bridgeId} | Create a new bridge or updates an existing one.
[**destroy**](ApiDocsbridgesFormatApi.md#destroy) | **DELETE** /bridges/{bridgeId} | Shut down a bridge.
[**get**](ApiDocsbridgesFormatApi.md#get) | **GET** /bridges/{bridgeId} | Get bridge details.
[**play**](ApiDocsbridgesFormatApi.md#play) | **POST** /bridges/{bridgeId}/play | Start playback of media on a bridge.
[**playWithId**](ApiDocsbridgesFormatApi.md#playWithId) | **POST** /bridges/{bridgeId}/play/{playbackId} | Start playback of media on a bridge.
[**record**](ApiDocsbridgesFormatApi.md#record) | **POST** /bridges/{bridgeId}/record | Start a recording.
[**removeChannel**](ApiDocsbridgesFormatApi.md#removeChannel) | **POST** /bridges/{bridgeId}/removeChannel | Remove a channel from a bridge.
[**setVideoSource**](ApiDocsbridgesFormatApi.md#setVideoSource) | **POST** /bridges/{bridgeId}/videoSource/{channelId} | Set a channel as the video source in a multi-party mixing bridge. This operation has no effect on bridges with two or fewer participants.
[**startMoh**](ApiDocsbridgesFormatApi.md#startMoh) | **POST** /bridges/{bridgeId}/moh | Play music on hold to a bridge or change the MOH class that is playing.
[**stopMoh**](ApiDocsbridgesFormatApi.md#stopMoh) | **DELETE** /bridges/{bridgeId}/moh | Stop playing music on hold to a bridge.


# **addChannel**
> addChannel($bridge_id, $channel, $role, $absorb_dtmf, $mute, $inhibit_connected_line_updates)

Add a channel to a bridge.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ApiDocsbridgesFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$bridge_id = "bridge_id_example"; // string | Bridge's id
$channel = array("channel_example"); // string[] | Ids of channels to add to bridge
$role = "role_example"; // string | Channel's role in the bridge
$absorb_dtmf = false; // bool | Absorb DTMF coming from this channel, preventing it to pass through to the bridge
$mute = false; // bool | Mute audio from this channel, preventing it to pass through to the bridge
$inhibit_connected_line_updates = false; // bool | Do not present the identity of the newly connected channel to other bridge members

try {
    $apiInstance->addChannel($bridge_id, $channel, $role, $absorb_dtmf, $mute, $inhibit_connected_line_updates);
} catch (Exception $e) {
    echo 'Exception when calling ApiDocsbridgesFormatApi->addChannel: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **bridge_id** | **string**| Bridge&#39;s id |
 **channel** | [**string[]**](../Model/string.md)| Ids of channels to add to bridge |
 **role** | **string**| Channel&#39;s role in the bridge | [optional]
 **absorb_dtmf** | **bool**| Absorb DTMF coming from this channel, preventing it to pass through to the bridge | [optional] [default to false]
 **mute** | **bool**| Mute audio from this channel, preventing it to pass through to the bridge | [optional] [default to false]
 **inhibit_connected_line_updates** | **bool**| Do not present the identity of the newly connected channel to other bridge members | [optional] [default to false]

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

List all active bridges in Asterisk.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ApiDocsbridgesFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $apiInstance->callList();
} catch (Exception $e) {
    echo 'Exception when calling ApiDocsbridgesFormatApi->callList: ', $e->getMessage(), PHP_EOL;
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

# **clearVideoSource**
> clearVideoSource($bridge_id)

Removes any explicit video source in a multi-party mixing bridge. This operation has no effect on bridges with two or fewer participants. When no explicit video source is set, talk detection will be used to determine the active video stream.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ApiDocsbridgesFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$bridge_id = "bridge_id_example"; // string | Bridge's id

try {
    $apiInstance->clearVideoSource($bridge_id);
} catch (Exception $e) {
    echo 'Exception when calling ApiDocsbridgesFormatApi->clearVideoSource: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **bridge_id** | **string**| Bridge&#39;s id |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **create**
> create($type, $bridge_id, $name)

Create a new bridge.

This bridge persists until it has been shut down, or Asterisk has been shut down.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ApiDocsbridgesFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$type = "type_example"; // string | Comma separated list of bridge type attributes (mixing, holding, dtmf_events, proxy_media, video_sfu, video_single, sdp_label).
$bridge_id = "bridge_id_example"; // string | Unique ID to give to the bridge being created.
$name = "name_example"; // string | Name to give to the bridge being created.

try {
    $apiInstance->create($type, $bridge_id, $name);
} catch (Exception $e) {
    echo 'Exception when calling ApiDocsbridgesFormatApi->create: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **type** | **string**| Comma separated list of bridge type attributes (mixing, holding, dtmf_events, proxy_media, video_sfu, video_single, sdp_label). | [optional]
 **bridge_id** | **string**| Unique ID to give to the bridge being created. | [optional]
 **name** | **string**| Name to give to the bridge being created. | [optional]

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **createWithId**
> createWithId($bridge_id, $type, $name)

Create a new bridge or updates an existing one.

This bridge persists until it has been shut down, or Asterisk has been shut down.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ApiDocsbridgesFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$bridge_id = "bridge_id_example"; // string | Unique ID to give to the bridge being created.
$type = "type_example"; // string | Comma separated list of bridge type attributes (mixing, holding, dtmf_events, proxy_media, video_sfu, video_single, sdp_label) to set.
$name = "name_example"; // string | Set the name of the bridge.

try {
    $apiInstance->createWithId($bridge_id, $type, $name);
} catch (Exception $e) {
    echo 'Exception when calling ApiDocsbridgesFormatApi->createWithId: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **bridge_id** | **string**| Unique ID to give to the bridge being created. |
 **type** | **string**| Comma separated list of bridge type attributes (mixing, holding, dtmf_events, proxy_media, video_sfu, video_single, sdp_label) to set. | [optional]
 **name** | **string**| Set the name of the bridge. | [optional]

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **destroy**
> destroy($bridge_id)

Shut down a bridge.

If any channels are in this bridge, they will be removed and resume whatever they were doing beforehand.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ApiDocsbridgesFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$bridge_id = "bridge_id_example"; // string | Bridge's id

try {
    $apiInstance->destroy($bridge_id);
} catch (Exception $e) {
    echo 'Exception when calling ApiDocsbridgesFormatApi->destroy: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **bridge_id** | **string**| Bridge&#39;s id |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **get**
> get($bridge_id)

Get bridge details.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ApiDocsbridgesFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$bridge_id = "bridge_id_example"; // string | Bridge's id

try {
    $apiInstance->get($bridge_id);
} catch (Exception $e) {
    echo 'Exception when calling ApiDocsbridgesFormatApi->get: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **bridge_id** | **string**| Bridge&#39;s id |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **play**
> play($bridge_id, $media, $lang, $offsetms, $skipms, $playback_id)

Start playback of media on a bridge.

The media URI may be any of a number of URI's. Currently sound:, recording:, number:, digits:, characters:, and tone: URI's are supported. This operation creates a playback resource that can be used to control the playback of media (pause, rewind, fast forward, etc.)

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ApiDocsbridgesFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$bridge_id = "bridge_id_example"; // string | Bridge's id
$media = array("media_example"); // string[] | Media URIs to play.
$lang = "lang_example"; // string | For sounds, selects language for sound.
$offsetms = 0; // int | Number of milliseconds to skip before playing. Only applies to the first URI if multiple media URIs are specified.
$skipms = 3000; // int | Number of milliseconds to skip for forward/reverse operations.
$playback_id = "playback_id_example"; // string | Playback Id.

try {
    $apiInstance->play($bridge_id, $media, $lang, $offsetms, $skipms, $playback_id);
} catch (Exception $e) {
    echo 'Exception when calling ApiDocsbridgesFormatApi->play: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **bridge_id** | **string**| Bridge&#39;s id |
 **media** | [**string[]**](../Model/string.md)| Media URIs to play. |
 **lang** | **string**| For sounds, selects language for sound. | [optional]
 **offsetms** | **int**| Number of milliseconds to skip before playing. Only applies to the first URI if multiple media URIs are specified. | [optional] [default to 0]
 **skipms** | **int**| Number of milliseconds to skip for forward/reverse operations. | [optional] [default to 3000]
 **playback_id** | **string**| Playback Id. | [optional]

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **playWithId**
> playWithId($bridge_id, $playback_id, $media, $lang, $offsetms, $skipms)

Start playback of media on a bridge.

The media URI may be any of a number of URI's. Currently sound:, recording:, number:, digits:, characters:, and tone: URI's are supported. This operation creates a playback resource that can be used to control the playback of media (pause, rewind, fast forward, etc.)

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ApiDocsbridgesFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$bridge_id = "bridge_id_example"; // string | Bridge's id
$playback_id = "playback_id_example"; // string | Playback ID.
$media = array("media_example"); // string[] | Media URIs to play.
$lang = "lang_example"; // string | For sounds, selects language for sound.
$offsetms = 0; // int | Number of milliseconds to skip before playing. Only applies to the first URI if multiple media URIs are specified.
$skipms = 3000; // int | Number of milliseconds to skip for forward/reverse operations.

try {
    $apiInstance->playWithId($bridge_id, $playback_id, $media, $lang, $offsetms, $skipms);
} catch (Exception $e) {
    echo 'Exception when calling ApiDocsbridgesFormatApi->playWithId: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **bridge_id** | **string**| Bridge&#39;s id |
 **playback_id** | **string**| Playback ID. |
 **media** | [**string[]**](../Model/string.md)| Media URIs to play. |
 **lang** | **string**| For sounds, selects language for sound. | [optional]
 **offsetms** | **int**| Number of milliseconds to skip before playing. Only applies to the first URI if multiple media URIs are specified. | [optional] [default to 0]
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
> record($bridge_id, $name, $format, $max_duration_seconds, $max_silence_seconds, $if_exists, $beep, $terminate_on)

Start a recording.

This records the mixed audio from all channels participating in this bridge.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ApiDocsbridgesFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$bridge_id = "bridge_id_example"; // string | Bridge's id
$name = "name_example"; // string | Recording's filename
$format = "format_example"; // string | Format to encode audio in
$max_duration_seconds = 0; // int | Maximum duration of the recording, in seconds. 0 for no limit.
$max_silence_seconds = 0; // int | Maximum duration of silence, in seconds. 0 for no limit.
$if_exists = "fail"; // string | Action to take if a recording with the same name already exists.
$beep = false; // bool | Play beep when recording begins
$terminate_on = "none"; // string | DTMF input to terminate recording.

try {
    $apiInstance->record($bridge_id, $name, $format, $max_duration_seconds, $max_silence_seconds, $if_exists, $beep, $terminate_on);
} catch (Exception $e) {
    echo 'Exception when calling ApiDocsbridgesFormatApi->record: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **bridge_id** | **string**| Bridge&#39;s id |
 **name** | **string**| Recording&#39;s filename |
 **format** | **string**| Format to encode audio in |
 **max_duration_seconds** | **int**| Maximum duration of the recording, in seconds. 0 for no limit. | [optional] [default to 0]
 **max_silence_seconds** | **int**| Maximum duration of silence, in seconds. 0 for no limit. | [optional] [default to 0]
 **if_exists** | **string**| Action to take if a recording with the same name already exists. | [optional] [default to fail]
 **beep** | **bool**| Play beep when recording begins | [optional] [default to false]
 **terminate_on** | **string**| DTMF input to terminate recording. | [optional] [default to none]

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **removeChannel**
> removeChannel($bridge_id, $channel)

Remove a channel from a bridge.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ApiDocsbridgesFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$bridge_id = "bridge_id_example"; // string | Bridge's id
$channel = array("channel_example"); // string[] | Ids of channels to remove from bridge

try {
    $apiInstance->removeChannel($bridge_id, $channel);
} catch (Exception $e) {
    echo 'Exception when calling ApiDocsbridgesFormatApi->removeChannel: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **bridge_id** | **string**| Bridge&#39;s id |
 **channel** | [**string[]**](../Model/string.md)| Ids of channels to remove from bridge |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **setVideoSource**
> setVideoSource($bridge_id, $channel_id)

Set a channel as the video source in a multi-party mixing bridge. This operation has no effect on bridges with two or fewer participants.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ApiDocsbridgesFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$bridge_id = "bridge_id_example"; // string | Bridge's id
$channel_id = "channel_id_example"; // string | Channel's id

try {
    $apiInstance->setVideoSource($bridge_id, $channel_id);
} catch (Exception $e) {
    echo 'Exception when calling ApiDocsbridgesFormatApi->setVideoSource: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **bridge_id** | **string**| Bridge&#39;s id |
 **channel_id** | **string**| Channel&#39;s id |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **startMoh**
> startMoh($bridge_id, $moh_class)

Play music on hold to a bridge or change the MOH class that is playing.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ApiDocsbridgesFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$bridge_id = "bridge_id_example"; // string | Bridge's id
$moh_class = "moh_class_example"; // string | Channel's id

try {
    $apiInstance->startMoh($bridge_id, $moh_class);
} catch (Exception $e) {
    echo 'Exception when calling ApiDocsbridgesFormatApi->startMoh: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **bridge_id** | **string**| Bridge&#39;s id |
 **moh_class** | **string**| Channel&#39;s id | [optional]

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **stopMoh**
> stopMoh($bridge_id)

Stop playing music on hold to a bridge.

This will only stop music on hold being played via POST bridges/{bridgeId}/moh.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ApiDocsbridgesFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$bridge_id = "bridge_id_example"; // string | Bridge's id

try {
    $apiInstance->stopMoh($bridge_id);
} catch (Exception $e) {
    echo 'Exception when calling ApiDocsbridgesFormatApi->stopMoh: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **bridge_id** | **string**| Bridge&#39;s id |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

