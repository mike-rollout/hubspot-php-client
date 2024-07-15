# OpenAPI\Client\BasicApi

All URIs are relative to https://api.hubapi.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**deleteCrmV3ObjectsContactsContactIdArchive()**](BasicApi.md#deleteCrmV3ObjectsContactsContactIdArchive) | **DELETE** /crm/v3/objects/contacts/{contactId} | Archive |
| [**getCrmV3ObjectsContactsContactIdGetById()**](BasicApi.md#getCrmV3ObjectsContactsContactIdGetById) | **GET** /crm/v3/objects/contacts/{contactId} | Read |
| [**getCrmV3ObjectsContactsGetPage()**](BasicApi.md#getCrmV3ObjectsContactsGetPage) | **GET** /crm/v3/objects/contacts | List |
| [**patchCrmV3ObjectsContactsContactIdUpdate()**](BasicApi.md#patchCrmV3ObjectsContactsContactIdUpdate) | **PATCH** /crm/v3/objects/contacts/{contactId} | Update |
| [**postCrmV3ObjectsContactsCreate()**](BasicApi.md#postCrmV3ObjectsContactsCreate) | **POST** /crm/v3/objects/contacts | Create |


## `deleteCrmV3ObjectsContactsContactIdArchive()`

```php
deleteCrmV3ObjectsContactsContactIdArchive($contact_id)
```

Archive

Move an Object identified by `{contactId}` to the recycling bin.

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


$apiInstance = new OpenAPI\Client\Api\BasicApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$contact_id = 'contact_id_example'; // string

try {
    $apiInstance->deleteCrmV3ObjectsContactsContactIdArchive($contact_id);
} catch (Exception $e) {
    echo 'Exception when calling BasicApi->deleteCrmV3ObjectsContactsContactIdArchive: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **contact_id** | **string**|  | |

### Return type

void (empty response body)

### Authorization

[oauth2](../../README.md#oauth2), [private_apps](../../README.md#private_apps)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `*/*`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getCrmV3ObjectsContactsContactIdGetById()`

```php
getCrmV3ObjectsContactsContactIdGetById($contact_id, $properties, $properties_with_history, $associations, $archived): \OpenAPI\Client\Model\SimplePublicObjectWithAssociations
```

Read

Read an Object identified by `{contactId}`. `{contactId}` refers to the internal object ID.  Control what is returned via the `properties` query param.

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


$apiInstance = new OpenAPI\Client\Api\BasicApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$contact_id = 'contact_id_example'; // string
$properties = array('properties_example'); // string[] | A comma separated list of the properties to be returned in the response. If any of the specified properties are not present on the requested object(s), they will be ignored.
$properties_with_history = array('properties_with_history_example'); // string[] | A comma separated list of the properties to be returned along with their history of previous values. If any of the specified properties are not present on the requested object(s), they will be ignored.
$associations = array('associations_example'); // string[] | A comma separated list of object types to retrieve associated IDs for. If any of the specified associations do not exist, they will be ignored.
$archived = false; // bool | Whether to return only results that have been archived.

try {
    $result = $apiInstance->getCrmV3ObjectsContactsContactIdGetById($contact_id, $properties, $properties_with_history, $associations, $archived);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BasicApi->getCrmV3ObjectsContactsContactIdGetById: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **contact_id** | **string**|  | |
| **properties** | [**string[]**](../Model/string.md)| A comma separated list of the properties to be returned in the response. If any of the specified properties are not present on the requested object(s), they will be ignored. | [optional] |
| **properties_with_history** | [**string[]**](../Model/string.md)| A comma separated list of the properties to be returned along with their history of previous values. If any of the specified properties are not present on the requested object(s), they will be ignored. | [optional] |
| **associations** | [**string[]**](../Model/string.md)| A comma separated list of object types to retrieve associated IDs for. If any of the specified associations do not exist, they will be ignored. | [optional] |
| **archived** | **bool**| Whether to return only results that have been archived. | [optional] [default to false] |

### Return type

[**\OpenAPI\Client\Model\SimplePublicObjectWithAssociations**](../Model/SimplePublicObjectWithAssociations.md)

### Authorization

[oauth2](../../README.md#oauth2), [private_apps](../../README.md#private_apps)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `*/*`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getCrmV3ObjectsContactsGetPage()`

```php
getCrmV3ObjectsContactsGetPage($limit, $after, $properties, $properties_with_history, $associations, $archived): \OpenAPI\Client\Model\CollectionResponseSimplePublicObjectWithAssociationsForwardPaging
```

List

Read a page of contacts. Control what is returned via the `properties` query param.

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


$apiInstance = new OpenAPI\Client\Api\BasicApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$limit = 10; // int | The maximum number of results to display per page.
$after = 'after_example'; // string | The paging cursor token of the last successfully read resource will be returned as the `paging.next.after` JSON property of a paged response containing more results.
$properties = array('properties_example'); // string[] | A comma separated list of the properties to be returned in the response. If any of the specified properties are not present on the requested object(s), they will be ignored.
$properties_with_history = array('properties_with_history_example'); // string[] | A comma separated list of the properties to be returned along with their history of previous values. If any of the specified properties are not present on the requested object(s), they will be ignored. Usage of this parameter will reduce the maximum number of objects that can be read by a single request.
$associations = array('associations_example'); // string[] | A comma separated list of object types to retrieve associated IDs for. If any of the specified associations do not exist, they will be ignored.
$archived = false; // bool | Whether to return only results that have been archived.

try {
    $result = $apiInstance->getCrmV3ObjectsContactsGetPage($limit, $after, $properties, $properties_with_history, $associations, $archived);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BasicApi->getCrmV3ObjectsContactsGetPage: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **limit** | **int**| The maximum number of results to display per page. | [optional] [default to 10] |
| **after** | **string**| The paging cursor token of the last successfully read resource will be returned as the &#x60;paging.next.after&#x60; JSON property of a paged response containing more results. | [optional] |
| **properties** | [**string[]**](../Model/string.md)| A comma separated list of the properties to be returned in the response. If any of the specified properties are not present on the requested object(s), they will be ignored. | [optional] |
| **properties_with_history** | [**string[]**](../Model/string.md)| A comma separated list of the properties to be returned along with their history of previous values. If any of the specified properties are not present on the requested object(s), they will be ignored. Usage of this parameter will reduce the maximum number of objects that can be read by a single request. | [optional] |
| **associations** | [**string[]**](../Model/string.md)| A comma separated list of object types to retrieve associated IDs for. If any of the specified associations do not exist, they will be ignored. | [optional] |
| **archived** | **bool**| Whether to return only results that have been archived. | [optional] [default to false] |

### Return type

[**\OpenAPI\Client\Model\CollectionResponseSimplePublicObjectWithAssociationsForwardPaging**](../Model/CollectionResponseSimplePublicObjectWithAssociationsForwardPaging.md)

### Authorization

[oauth2](../../README.md#oauth2), [private_apps](../../README.md#private_apps)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `*/*`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `patchCrmV3ObjectsContactsContactIdUpdate()`

```php
patchCrmV3ObjectsContactsContactIdUpdate($contact_id, $simple_public_object_input): \OpenAPI\Client\Model\SimplePublicObject
```

Update

Perform a partial update of an Object identified by `{contactId}`. `{contactId}` refers to the internal object ID. Provided property values will be overwritten. Read-only and non-existent properties will be ignored. Properties values can be cleared by passing an empty string.

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


$apiInstance = new OpenAPI\Client\Api\BasicApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$contact_id = 'contact_id_example'; // string
$simple_public_object_input = new \OpenAPI\Client\Model\SimplePublicObjectInput(); // \OpenAPI\Client\Model\SimplePublicObjectInput

try {
    $result = $apiInstance->patchCrmV3ObjectsContactsContactIdUpdate($contact_id, $simple_public_object_input);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BasicApi->patchCrmV3ObjectsContactsContactIdUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **contact_id** | **string**|  | |
| **simple_public_object_input** | [**\OpenAPI\Client\Model\SimplePublicObjectInput**](../Model/SimplePublicObjectInput.md)|  | |

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

## `postCrmV3ObjectsContactsCreate()`

```php
postCrmV3ObjectsContactsCreate($simple_public_object_input_for_create): \OpenAPI\Client\Model\SimplePublicObject
```

Create

Create a contact with the given properties and return a copy of the object, including the ID. Documentation and examples for creating standard contacts is provided.

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


$apiInstance = new OpenAPI\Client\Api\BasicApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$simple_public_object_input_for_create = new \OpenAPI\Client\Model\SimplePublicObjectInputForCreate(); // \OpenAPI\Client\Model\SimplePublicObjectInputForCreate

try {
    $result = $apiInstance->postCrmV3ObjectsContactsCreate($simple_public_object_input_for_create);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BasicApi->postCrmV3ObjectsContactsCreate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **simple_public_object_input_for_create** | [**\OpenAPI\Client\Model\SimplePublicObjectInputForCreate**](../Model/SimplePublicObjectInputForCreate.md)|  | |

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
