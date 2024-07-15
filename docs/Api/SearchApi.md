# OpenAPI\Client\SearchApi

All URIs are relative to https://api.hubapi.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**postCrmV3ObjectsContactsSearchDoSearch()**](SearchApi.md#postCrmV3ObjectsContactsSearchDoSearch) | **POST** /crm/v3/objects/contacts/search |  |


## `postCrmV3ObjectsContactsSearchDoSearch()`

```php
postCrmV3ObjectsContactsSearchDoSearch($public_object_search_request): \OpenAPI\Client\Model\CollectionResponseWithTotalSimplePublicObjectForwardPaging
```



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


$apiInstance = new OpenAPI\Client\Api\SearchApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$public_object_search_request = new \OpenAPI\Client\Model\PublicObjectSearchRequest(); // \OpenAPI\Client\Model\PublicObjectSearchRequest

try {
    $result = $apiInstance->postCrmV3ObjectsContactsSearchDoSearch($public_object_search_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SearchApi->postCrmV3ObjectsContactsSearchDoSearch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **public_object_search_request** | [**\OpenAPI\Client\Model\PublicObjectSearchRequest**](../Model/PublicObjectSearchRequest.md)|  | |

### Return type

[**\OpenAPI\Client\Model\CollectionResponseWithTotalSimplePublicObjectForwardPaging**](../Model/CollectionResponseWithTotalSimplePublicObjectForwardPaging.md)

### Authorization

[oauth2](../../README.md#oauth2), [private_apps](../../README.md#private_apps)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`, `*/*`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
