# OpenAPIClient-php

No description provided (generated by Openapi Generator https://github.com/openapitools/openapi-generator)


## Installation & Usage

### Requirements

PHP 7.4 and later.
Should also work with PHP 8.0.

### Composer

To install the bindings via [Composer](https://getcomposer.org/), add the following to `composer.json`:

```json
{
  "repositories": [
    {
      "type": "vcs",
      "url": "https://github.com/GIT_USER_ID/GIT_REPO_ID.git"
    }
  ],
  "require": {
    "GIT_USER_ID/GIT_REPO_ID": "*@dev"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
<?php
require_once('/path/to/OpenAPIClient-php/vendor/autoload.php');
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



// Configure OAuth2 access token for authorization: oauth2
$config = Rollout\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

// Configure API key authorization: private_apps
$config = Rollout\Client\Configuration::getDefaultConfiguration()->setApiKey('private-app', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Rollout\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('private-app', 'Bearer');


$apiInstance = new Rollout\Client\Api\BasicApi(
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

## API Endpoints

All URIs are relative to *https://api.hubapi.com*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*BasicApi* | [**deleteCrmV3ObjectsContactsContactIdArchive**](docs/Api/BasicApi.md#deletecrmv3objectscontactscontactidarchive) | **DELETE** /crm/v3/objects/contacts/{contactId} | Archive
*BasicApi* | [**getCrmV3ObjectsContactsContactIdGetById**](docs/Api/BasicApi.md#getcrmv3objectscontactscontactidgetbyid) | **GET** /crm/v3/objects/contacts/{contactId} | Read
*BasicApi* | [**getCrmV3ObjectsContactsGetPage**](docs/Api/BasicApi.md#getcrmv3objectscontactsgetpage) | **GET** /crm/v3/objects/contacts | List
*BasicApi* | [**patchCrmV3ObjectsContactsContactIdUpdate**](docs/Api/BasicApi.md#patchcrmv3objectscontactscontactidupdate) | **PATCH** /crm/v3/objects/contacts/{contactId} | Update
*BasicApi* | [**postCrmV3ObjectsContactsCreate**](docs/Api/BasicApi.md#postcrmv3objectscontactscreate) | **POST** /crm/v3/objects/contacts | Create
*BatchApi* | [**postCrmV3ObjectsContactsBatchArchiveArchive**](docs/Api/BatchApi.md#postcrmv3objectscontactsbatcharchivearchive) | **POST** /crm/v3/objects/contacts/batch/archive | Archive a batch of contacts by ID
*BatchApi* | [**postCrmV3ObjectsContactsBatchCreateCreate**](docs/Api/BatchApi.md#postcrmv3objectscontactsbatchcreatecreate) | **POST** /crm/v3/objects/contacts/batch/create | Create a batch of contacts
*BatchApi* | [**postCrmV3ObjectsContactsBatchReadRead**](docs/Api/BatchApi.md#postcrmv3objectscontactsbatchreadread) | **POST** /crm/v3/objects/contacts/batch/read | Read a batch of contacts by internal ID, or unique property values
*BatchApi* | [**postCrmV3ObjectsContactsBatchUpdateUpdate**](docs/Api/BatchApi.md#postcrmv3objectscontactsbatchupdateupdate) | **POST** /crm/v3/objects/contacts/batch/update | Update a batch of contacts
*GDPRApi* | [**postCrmV3ObjectsContactsGdprDeletePurge**](docs/Api/GDPRApi.md#postcrmv3objectscontactsgdprdeletepurge) | **POST** /crm/v3/objects/contacts/gdpr-delete | GDPR DELETE
*PublicObjectApi* | [**postCrmV3ObjectsContactsMergeMerge**](docs/Api/PublicObjectApi.md#postcrmv3objectscontactsmergemerge) | **POST** /crm/v3/objects/contacts/merge | Merge two contacts with same type
*SearchApi* | [**postCrmV3ObjectsContactsSearchDoSearch**](docs/Api/SearchApi.md#postcrmv3objectscontactssearchdosearch) | **POST** /crm/v3/objects/contacts/search | 

## Models

- [AssociatedId](docs/Model/AssociatedId.md)
- [AssociationSpec](docs/Model/AssociationSpec.md)
- [BatchInputSimplePublicObjectBatchInput](docs/Model/BatchInputSimplePublicObjectBatchInput.md)
- [BatchInputSimplePublicObjectId](docs/Model/BatchInputSimplePublicObjectId.md)
- [BatchInputSimplePublicObjectInputForCreate](docs/Model/BatchInputSimplePublicObjectInputForCreate.md)
- [BatchReadInputSimplePublicObjectId](docs/Model/BatchReadInputSimplePublicObjectId.md)
- [BatchResponseSimplePublicObject](docs/Model/BatchResponseSimplePublicObject.md)
- [BatchResponseSimplePublicObjectWithErrors](docs/Model/BatchResponseSimplePublicObjectWithErrors.md)
- [CollectionResponseAssociatedId](docs/Model/CollectionResponseAssociatedId.md)
- [CollectionResponseSimplePublicObjectWithAssociationsForwardPaging](docs/Model/CollectionResponseSimplePublicObjectWithAssociationsForwardPaging.md)
- [CollectionResponseWithTotalSimplePublicObjectForwardPaging](docs/Model/CollectionResponseWithTotalSimplePublicObjectForwardPaging.md)
- [Error](docs/Model/Error.md)
- [ErrorDetail](docs/Model/ErrorDetail.md)
- [Filter](docs/Model/Filter.md)
- [FilterGroup](docs/Model/FilterGroup.md)
- [ForwardPaging](docs/Model/ForwardPaging.md)
- [NextPage](docs/Model/NextPage.md)
- [Paging](docs/Model/Paging.md)
- [PreviousPage](docs/Model/PreviousPage.md)
- [PublicAssociationsForObject](docs/Model/PublicAssociationsForObject.md)
- [PublicGdprDeleteInput](docs/Model/PublicGdprDeleteInput.md)
- [PublicMergeInput](docs/Model/PublicMergeInput.md)
- [PublicObjectId](docs/Model/PublicObjectId.md)
- [PublicObjectSearchRequest](docs/Model/PublicObjectSearchRequest.md)
- [SimplePublicObject](docs/Model/SimplePublicObject.md)
- [SimplePublicObjectBatchInput](docs/Model/SimplePublicObjectBatchInput.md)
- [SimplePublicObjectId](docs/Model/SimplePublicObjectId.md)
- [SimplePublicObjectInput](docs/Model/SimplePublicObjectInput.md)
- [SimplePublicObjectInputForCreate](docs/Model/SimplePublicObjectInputForCreate.md)
- [SimplePublicObjectWithAssociations](docs/Model/SimplePublicObjectWithAssociations.md)
- [StandardError](docs/Model/StandardError.md)
- [ValueWithTimestamp](docs/Model/ValueWithTimestamp.md)

## Authorization

Authentication schemes defined for the API:
### oauth2_legacy

- **Type**: `OAuth`
- **Flow**: `accessCode`
- **Authorization URL**: `https://app.hubspot.com/oauth/authorize`
- **Scopes**: 
    - **media_bridge.read**: Read media and media events
    - **crm.objects.goals.read**: Read goals
    - **tickets**: Read and write tickets
    - **crm.objects.custom.read**: View custom object records
    - **e-commerce**: e-commerce
    - **crm.objects.custom.write**: Change custom object records

### oauth2

- **Type**: `OAuth`
- **Flow**: `accessCode`
- **Authorization URL**: `https://app.hubspot.com/oauth/authorize`
- **Scopes**: 
    - **crm.objects.quotes.write**: Quotes
    - **crm.objects.deals.read**:  
    - **crm.objects.line_items.read**: Line Items
    - **crm.objects.deals.write**:  
    - **crm.objects.quotes.read**: Quotes
    - **crm.objects.line_items.write**: Line Items
    - **crm.objects.companies.read**:  
    - **crm.objects.companies.write**:  
    - **crm.objects.contacts.write**:  
    - **crm.objects.contacts.read**:  

### private_apps_legacy

- **Type**: API key
- **API key parameter name**: private-app-legacy
- **Location**: HTTP header


### private_apps

- **Type**: API key
- **API key parameter name**: private-app
- **Location**: HTTP header


## Tests

To run the tests, use:

```bash
composer install
vendor/bin/phpunit
```

## Author



## About this package

This PHP package is automatically generated by the [OpenAPI Generator](https://openapi-generator.tech) project:

- API version: `v3`
    - Generator version: `7.7.0`
- Build package: `org.openapitools.codegen.languages.PhpClientCodegen`
