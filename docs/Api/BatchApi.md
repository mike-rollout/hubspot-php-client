# OpenAPI\Client\BatchApi

All URIs are relative to https://api.hubapi.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**postCrmV3ObjectsContactsBatchArchiveArchive()**](BatchApi.md#postCrmV3ObjectsContactsBatchArchiveArchive) | **POST** /crm/v3/objects/contacts/batch/archive | Archive a batch of contacts by ID |
| [**postCrmV3ObjectsContactsBatchCreateCreate()**](BatchApi.md#postCrmV3ObjectsContactsBatchCreateCreate) | **POST** /crm/v3/objects/contacts/batch/create | Create a batch of contacts |
| [**postCrmV3ObjectsContactsBatchReadRead()**](BatchApi.md#postCrmV3ObjectsContactsBatchReadRead) | **POST** /crm/v3/objects/contacts/batch/read | Read a batch of contacts by internal ID, or unique property values |
| [**postCrmV3ObjectsContactsBatchUpdateUpdate()**](BatchApi.md#postCrmV3ObjectsContactsBatchUpdateUpdate) | **POST** /crm/v3/objects/contacts/batch/update | Update a batch of contacts |


## `postCrmV3ObjectsContactsBatchArchiveArchive()`

```php
postCrmV3ObjectsContactsBatchArchiveArchive($batch_input_simple_public_object_id)
```

Archive a batch of contacts by ID

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

// Configure API key authorization: private_apps
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('private-app', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('private-app', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\BatchApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$batch_input_simple_public_object_id = new \OpenAPI\Client\Model\BatchInputSimplePublicObjectId(); // \OpenAPI\Client\Model\BatchInputSimplePublicObjectId

try {
    $apiInstance->postCrmV3ObjectsContactsBatchArchiveArchive($batch_input_simple_public_object_id);
} catch (Exception $e) {
    echo 'Exception when calling BatchApi->postCrmV3ObjectsContactsBatchArchiveArchive: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **batch_input_simple_public_object_id** | [**\OpenAPI\Client\Model\BatchInputSimplePublicObjectId**](../Model/BatchInputSimplePublicObjectId.md)|  | |

### Return type

void (empty response body)

### Authorization

[oauth2](../../README.md#oauth2), [private_apps](../../README.md#private_apps)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `*/*`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `postCrmV3ObjectsContactsBatchCreateCreate()`

```php
postCrmV3ObjectsContactsBatchCreateCreate($batch_input_simple_public_object_input_for_create): \OpenAPI\Client\Model\BatchResponseSimplePublicObject
```

Create a batch of contacts

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

// Configure API key authorization: private_apps
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('private-app', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('private-app', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\BatchApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$batch_input_simple_public_object_input_for_create = new \OpenAPI\Client\Model\BatchInputSimplePublicObjectInputForCreate(); // \OpenAPI\Client\Model\BatchInputSimplePublicObjectInputForCreate

try {
    $result = $apiInstance->postCrmV3ObjectsContactsBatchCreateCreate($batch_input_simple_public_object_input_for_create);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BatchApi->postCrmV3ObjectsContactsBatchCreateCreate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **batch_input_simple_public_object_input_for_create** | [**\OpenAPI\Client\Model\BatchInputSimplePublicObjectInputForCreate**](../Model/BatchInputSimplePublicObjectInputForCreate.md)|  | |

### Return type

[**\OpenAPI\Client\Model\BatchResponseSimplePublicObject**](../Model/BatchResponseSimplePublicObject.md)

### Authorization

[oauth2](../../README.md#oauth2), [private_apps](../../README.md#private_apps)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`, `*/*`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `postCrmV3ObjectsContactsBatchReadRead()`

```php
postCrmV3ObjectsContactsBatchReadRead($batch_read_input_simple_public_object_id, $archived): \OpenAPI\Client\Model\BatchResponseSimplePublicObject
```

Read a batch of contacts by internal ID, or unique property values

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

// Configure API key authorization: private_apps
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('private-app', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('private-app', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\BatchApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$batch_read_input_simple_public_object_id = new \OpenAPI\Client\Model\BatchReadInputSimplePublicObjectId(); // \OpenAPI\Client\Model\BatchReadInputSimplePublicObjectId
$archived = false; // bool | Whether to return only results that have been archived.

try {
    $result = $apiInstance->postCrmV3ObjectsContactsBatchReadRead($batch_read_input_simple_public_object_id, $archived);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BatchApi->postCrmV3ObjectsContactsBatchReadRead: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **batch_read_input_simple_public_object_id** | [**\OpenAPI\Client\Model\BatchReadInputSimplePublicObjectId**](../Model/BatchReadInputSimplePublicObjectId.md)|  | |
| **archived** | **bool**| Whether to return only results that have been archived. | [optional] [default to false] |

### Return type

[**\OpenAPI\Client\Model\BatchResponseSimplePublicObject**](../Model/BatchResponseSimplePublicObject.md)

### Authorization

[oauth2](../../README.md#oauth2), [private_apps](../../README.md#private_apps)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`, `*/*`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `postCrmV3ObjectsContactsBatchUpdateUpdate()`

```php
postCrmV3ObjectsContactsBatchUpdateUpdate($batch_input_simple_public_object_batch_input): \OpenAPI\Client\Model\BatchResponseSimplePublicObject
```

Update a batch of contacts

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

// Configure API key authorization: private_apps
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('private-app', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('private-app', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\BatchApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$batch_input_simple_public_object_batch_input = new \OpenAPI\Client\Model\BatchInputSimplePublicObjectBatchInput(); // \OpenAPI\Client\Model\BatchInputSimplePublicObjectBatchInput

try {
    $result = $apiInstance->postCrmV3ObjectsContactsBatchUpdateUpdate($batch_input_simple_public_object_batch_input);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BatchApi->postCrmV3ObjectsContactsBatchUpdateUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **batch_input_simple_public_object_batch_input** | [**\OpenAPI\Client\Model\BatchInputSimplePublicObjectBatchInput**](../Model/BatchInputSimplePublicObjectBatchInput.md)|  | |

### Return type

[**\OpenAPI\Client\Model\BatchResponseSimplePublicObject**](../Model/BatchResponseSimplePublicObject.md)

### Authorization

[oauth2](../../README.md#oauth2), [private_apps](../../README.md#private_apps)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`, `*/*`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
