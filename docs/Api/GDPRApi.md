# OpenAPI\Client\GDPRApi

All URIs are relative to https://api.hubapi.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**postCrmV3ObjectsContactsGdprDeletePurge()**](GDPRApi.md#postCrmV3ObjectsContactsGdprDeletePurge) | **POST** /crm/v3/objects/contacts/gdpr-delete | GDPR DELETE |


## `postCrmV3ObjectsContactsGdprDeletePurge()`

```php
postCrmV3ObjectsContactsGdprDeletePurge($public_gdpr_delete_input)
```

GDPR DELETE

Permanently delete a contact and all associated content to follow GDPR. Use optional property 'idProperty' set to 'email' to identify contact by email address. If email address is not found, the email address will be added to a blocklist and prevent it from being used in the future.

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


$apiInstance = new OpenAPI\Client\Api\GDPRApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$public_gdpr_delete_input = new \OpenAPI\Client\Model\PublicGdprDeleteInput(); // \OpenAPI\Client\Model\PublicGdprDeleteInput

try {
    $apiInstance->postCrmV3ObjectsContactsGdprDeletePurge($public_gdpr_delete_input);
} catch (Exception $e) {
    echo 'Exception when calling GDPRApi->postCrmV3ObjectsContactsGdprDeletePurge: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **public_gdpr_delete_input** | [**\OpenAPI\Client\Model\PublicGdprDeleteInput**](../Model/PublicGdprDeleteInput.md)|  | |

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
