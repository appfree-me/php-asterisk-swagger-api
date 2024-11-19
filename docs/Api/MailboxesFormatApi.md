# Swagger\Client\MailboxesFormatApi

All URIs are relative to *http://localhost:8088/ari*

Method | HTTP request | Description
------------- | ------------- | -------------
[**callList**](MailboxesFormatApi.md#callList) | **GET** /mailboxes | List all mailboxes.
[**delete**](MailboxesFormatApi.md#delete) | **DELETE** /mailboxes/{mailboxName} | Destroy a mailbox.
[**get**](MailboxesFormatApi.md#get) | **GET** /mailboxes/{mailboxName} | Retrieve the current state of a mailbox.
[**update**](MailboxesFormatApi.md#update) | **PUT** /mailboxes/{mailboxName} | Change the state of a mailbox. (Note - implicitly creates the mailbox).


# **callList**
> callList()

List all mailboxes.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\MailboxesFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $apiInstance->callList();
} catch (Exception $e) {
    echo 'Exception when calling MailboxesFormatApi->callList: ', $e->getMessage(), PHP_EOL;
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
> delete($mailbox_name)

Destroy a mailbox.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\MailboxesFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$mailbox_name = "mailbox_name_example"; // string | Name of the mailbox

try {
    $apiInstance->delete($mailbox_name);
} catch (Exception $e) {
    echo 'Exception when calling MailboxesFormatApi->delete: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **mailbox_name** | **string**| Name of the mailbox |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **get**
> get($mailbox_name)

Retrieve the current state of a mailbox.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\MailboxesFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$mailbox_name = "mailbox_name_example"; // string | Name of the mailbox

try {
    $apiInstance->get($mailbox_name);
} catch (Exception $e) {
    echo 'Exception when calling MailboxesFormatApi->get: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **mailbox_name** | **string**| Name of the mailbox |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **update**
> update($mailbox_name, $old_messages, $new_messages)

Change the state of a mailbox. (Note - implicitly creates the mailbox).

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\MailboxesFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$mailbox_name = "mailbox_name_example"; // string | Name of the mailbox
$old_messages = 56; // int | Count of old messages in the mailbox
$new_messages = 56; // int | Count of new messages in the mailbox

try {
    $apiInstance->update($mailbox_name, $old_messages, $new_messages);
} catch (Exception $e) {
    echo 'Exception when calling MailboxesFormatApi->update: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **mailbox_name** | **string**| Name of the mailbox |
 **old_messages** | **int**| Count of old messages in the mailbox |
 **new_messages** | **int**| Count of new messages in the mailbox |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

