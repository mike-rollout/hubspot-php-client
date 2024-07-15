# # Error

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**sub_category** | **string** | A specific category that contains more specific detail about the error | [optional]
**context** | **array<string,string[]>** | Context about the error condition | [optional]
**correlation_id** | **string** | A unique identifier for the request. Include this value with any error reports or support tickets |
**links** | **array<string,string>** | A map of link names to associated URIs containing documentation about the error or recommended remediation steps | [optional]
**message** | **string** | A human readable message describing the error along with remediation steps where appropriate |
**category** | **string** | The error category |
**errors** | [**\OpenAPI\Client\Model\ErrorDetail[]**](ErrorDetail.md) | further information about the error | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
