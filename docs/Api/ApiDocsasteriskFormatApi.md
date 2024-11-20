# Swagger\Client\ApiDocsasteriskFormatApi

All URIs are relative to *http://localhost:18088/ari*

Method | HTTP request | Description
------------- | ------------- | -------------
[**addLog**](ApiDocsasteriskFormatApi.md#addLog) | **POST** /asterisk/logging/{logChannelName} | Adds a log channel.
[**deleteLog**](ApiDocsasteriskFormatApi.md#deleteLog) | **DELETE** /asterisk/logging/{logChannelName} | Deletes a log channel.
[**deleteObject**](ApiDocsasteriskFormatApi.md#deleteObject) | **DELETE** /asterisk/config/dynamic/{configClass}/{objectType}/{id} | Delete a dynamic configuration object.
[**getGlobalVar**](ApiDocsasteriskFormatApi.md#getGlobalVar) | **GET** /asterisk/variable | Get the value of a global variable.
[**getInfo**](ApiDocsasteriskFormatApi.md#getInfo) | **GET** /asterisk/info | Gets Asterisk system information.
[**getModule**](ApiDocsasteriskFormatApi.md#getModule) | **GET** /asterisk/modules/{moduleName} | Get Asterisk module information.
[**getObject**](ApiDocsasteriskFormatApi.md#getObject) | **GET** /asterisk/config/dynamic/{configClass}/{objectType}/{id} | Retrieve a dynamic configuration object.
[**listLogChannels**](ApiDocsasteriskFormatApi.md#listLogChannels) | **GET** /asterisk/logging | Gets Asterisk log channel information.
[**listModules**](ApiDocsasteriskFormatApi.md#listModules) | **GET** /asterisk/modules | List Asterisk modules.
[**loadModule**](ApiDocsasteriskFormatApi.md#loadModule) | **POST** /asterisk/modules/{moduleName} | Load an Asterisk module.
[**ping**](ApiDocsasteriskFormatApi.md#ping) | **GET** /asterisk/ping | Response pong message.
[**reloadModule**](ApiDocsasteriskFormatApi.md#reloadModule) | **PUT** /asterisk/modules/{moduleName} | Reload an Asterisk module.
[**rotateLog**](ApiDocsasteriskFormatApi.md#rotateLog) | **PUT** /asterisk/logging/{logChannelName}/rotate | Rotates a log channel.
[**setGlobalVar**](ApiDocsasteriskFormatApi.md#setGlobalVar) | **POST** /asterisk/variable | Set the value of a global variable.
[**unloadModule**](ApiDocsasteriskFormatApi.md#unloadModule) | **DELETE** /asterisk/modules/{moduleName} | Unload an Asterisk module.
[**updateObject**](ApiDocsasteriskFormatApi.md#updateObject) | **PUT** /asterisk/config/dynamic/{configClass}/{objectType}/{id} | Create or update a dynamic configuration object.


# **addLog**
> addLog($log_channel_name, $configuration)

Adds a log channel.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ApiDocsasteriskFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$log_channel_name = "log_channel_name_example"; // string | The log channel to add
$configuration = "configuration_example"; // string | levels of the log channel

try {
    $apiInstance->addLog($log_channel_name, $configuration);
} catch (Exception $e) {
    echo 'Exception when calling ApiDocsasteriskFormatApi->addLog: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **log_channel_name** | **string**| The log channel to add |
 **configuration** | **string**| levels of the log channel |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **deleteLog**
> deleteLog($log_channel_name)

Deletes a log channel.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ApiDocsasteriskFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$log_channel_name = "log_channel_name_example"; // string | Log channels name

try {
    $apiInstance->deleteLog($log_channel_name);
} catch (Exception $e) {
    echo 'Exception when calling ApiDocsasteriskFormatApi->deleteLog: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **log_channel_name** | **string**| Log channels name |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **deleteObject**
> deleteObject($config_class, $object_type, $id)

Delete a dynamic configuration object.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ApiDocsasteriskFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$config_class = "config_class_example"; // string | The configuration class containing dynamic configuration objects.
$object_type = "object_type_example"; // string | The type of configuration object to delete.
$id = "id_example"; // string | The unique identifier of the object to delete.

try {
    $apiInstance->deleteObject($config_class, $object_type, $id);
} catch (Exception $e) {
    echo 'Exception when calling ApiDocsasteriskFormatApi->deleteObject: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **config_class** | **string**| The configuration class containing dynamic configuration objects. |
 **object_type** | **string**| The type of configuration object to delete. |
 **id** | **string**| The unique identifier of the object to delete. |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getGlobalVar**
> getGlobalVar($variable)

Get the value of a global variable.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ApiDocsasteriskFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$variable = "variable_example"; // string | The variable to get

try {
    $apiInstance->getGlobalVar($variable);
} catch (Exception $e) {
    echo 'Exception when calling ApiDocsasteriskFormatApi->getGlobalVar: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **variable** | **string**| The variable to get |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getInfo**
> getInfo($only)

Gets Asterisk system information.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ApiDocsasteriskFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$only = array("only_example"); // string[] | Filter information returned

try {
    $apiInstance->getInfo($only);
} catch (Exception $e) {
    echo 'Exception when calling ApiDocsasteriskFormatApi->getInfo: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **only** | [**string[]**](../Model/string.md)| Filter information returned | [optional]

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getModule**
> getModule($module_name)

Get Asterisk module information.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ApiDocsasteriskFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$module_name = "module_name_example"; // string | Module's name

try {
    $apiInstance->getModule($module_name);
} catch (Exception $e) {
    echo 'Exception when calling ApiDocsasteriskFormatApi->getModule: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **module_name** | **string**| Module&#39;s name |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getObject**
> getObject($config_class, $object_type, $id)

Retrieve a dynamic configuration object.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ApiDocsasteriskFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$config_class = "config_class_example"; // string | The configuration class containing dynamic configuration objects.
$object_type = "object_type_example"; // string | The type of configuration object to retrieve.
$id = "id_example"; // string | The unique identifier of the object to retrieve.

try {
    $apiInstance->getObject($config_class, $object_type, $id);
} catch (Exception $e) {
    echo 'Exception when calling ApiDocsasteriskFormatApi->getObject: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **config_class** | **string**| The configuration class containing dynamic configuration objects. |
 **object_type** | **string**| The type of configuration object to retrieve. |
 **id** | **string**| The unique identifier of the object to retrieve. |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **listLogChannels**
> listLogChannels()

Gets Asterisk log channel information.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ApiDocsasteriskFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $apiInstance->listLogChannels();
} catch (Exception $e) {
    echo 'Exception when calling ApiDocsasteriskFormatApi->listLogChannels: ', $e->getMessage(), PHP_EOL;
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

# **listModules**
> listModules()

List Asterisk modules.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ApiDocsasteriskFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $apiInstance->listModules();
} catch (Exception $e) {
    echo 'Exception when calling ApiDocsasteriskFormatApi->listModules: ', $e->getMessage(), PHP_EOL;
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

# **loadModule**
> loadModule($module_name)

Load an Asterisk module.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ApiDocsasteriskFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$module_name = "module_name_example"; // string | Module's name

try {
    $apiInstance->loadModule($module_name);
} catch (Exception $e) {
    echo 'Exception when calling ApiDocsasteriskFormatApi->loadModule: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **module_name** | **string**| Module&#39;s name |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **ping**
> ping()

Response pong message.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ApiDocsasteriskFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $apiInstance->ping();
} catch (Exception $e) {
    echo 'Exception when calling ApiDocsasteriskFormatApi->ping: ', $e->getMessage(), PHP_EOL;
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

# **reloadModule**
> reloadModule($module_name)

Reload an Asterisk module.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ApiDocsasteriskFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$module_name = "module_name_example"; // string | Module's name

try {
    $apiInstance->reloadModule($module_name);
} catch (Exception $e) {
    echo 'Exception when calling ApiDocsasteriskFormatApi->reloadModule: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **module_name** | **string**| Module&#39;s name |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **rotateLog**
> rotateLog($log_channel_name)

Rotates a log channel.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ApiDocsasteriskFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$log_channel_name = "log_channel_name_example"; // string | Log channel's name

try {
    $apiInstance->rotateLog($log_channel_name);
} catch (Exception $e) {
    echo 'Exception when calling ApiDocsasteriskFormatApi->rotateLog: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **log_channel_name** | **string**| Log channel&#39;s name |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **setGlobalVar**
> setGlobalVar($variable, $value)

Set the value of a global variable.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ApiDocsasteriskFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$variable = "variable_example"; // string | The variable to set
$value = "value_example"; // string | The value to set the variable to

try {
    $apiInstance->setGlobalVar($variable, $value);
} catch (Exception $e) {
    echo 'Exception when calling ApiDocsasteriskFormatApi->setGlobalVar: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **variable** | **string**| The variable to set |
 **value** | **string**| The value to set the variable to | [optional]

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **unloadModule**
> unloadModule($module_name)

Unload an Asterisk module.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ApiDocsasteriskFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$module_name = "module_name_example"; // string | Module's name

try {
    $apiInstance->unloadModule($module_name);
} catch (Exception $e) {
    echo 'Exception when calling ApiDocsasteriskFormatApi->unloadModule: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **module_name** | **string**| Module&#39;s name |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **updateObject**
> updateObject($config_class, $object_type, $id, $fields)

Create or update a dynamic configuration object.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ApiDocsasteriskFormatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$config_class = "config_class_example"; // string | The configuration class containing dynamic configuration objects.
$object_type = "object_type_example"; // string | The type of configuration object to create or update.
$id = "id_example"; // string | The unique identifier of the object to create or update.
$fields = new \Swagger\Client\Model\Containers(); // \Swagger\Client\Model\Containers | The body object should have a value that is a list of ConfigTuples, which provide the fields to update. Ex. [ { \"attribute\": \"directmedia\", \"value\": \"false\" } ]

try {
    $apiInstance->updateObject($config_class, $object_type, $id, $fields);
} catch (Exception $e) {
    echo 'Exception when calling ApiDocsasteriskFormatApi->updateObject: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **config_class** | **string**| The configuration class containing dynamic configuration objects. |
 **object_type** | **string**| The type of configuration object to create or update. |
 **id** | **string**| The unique identifier of the object to create or update. |
 **fields** | [**\Swagger\Client\Model\Containers**](../Model/Containers.md)| The body object should have a value that is a list of ConfigTuples, which provide the fields to update. Ex. [ { \&quot;attribute\&quot;: \&quot;directmedia\&quot;, \&quot;value\&quot;: \&quot;false\&quot; } ] | [optional]

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

