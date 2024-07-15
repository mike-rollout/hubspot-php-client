# OpenAPI\Client\PublicObjectApi

All URIs are relative to https://api.hubapi.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**postCrmV3ObjectsContactsMergeMerge()**](PublicObjectApi.md#postCrmV3ObjectsContactsMergeMerge) | **POST** /crm/v3/objects/contacts/merge | Merge two contacts with same type |


## `postCrmV3ObjectsContactsMergeMerge()`

```php
postCrmV3ObjectsContactsMergeMerge($public_merge_input): \OpenAPI\Client\Model\SimplePublicObject
```

Merge two contacts with same type

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


$apiInstance = new OpenAPI\Client\Api\PublicObjectApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$public_merge_input = new \OpenAPI\Client\Model\PublicMergeInput(); // \OpenAPI\Client\Model\PublicMergeInput

try {
    $result = $apiInstance->postCrmV3ObjectsContactsMergeMerge($public_merge_input);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PublicObjectApi->postCrmV3ObjectsContactsMergeMerge: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **public_merge_input** | [**\OpenAPI\Client\Model\PublicMergeInput**](../Model/PublicMergeInput.md)|  | |

### Return type

[**\OpenAPI\Client\Model\SimplePublicObject**](../Model/SimplePublicObject.md)

### Authorization

[oauth2](../../README.md#oauth2), [private_apps](../../README.md#private_apps)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`, `*/*`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
