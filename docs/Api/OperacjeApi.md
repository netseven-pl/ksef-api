# OpenAPI\Client\OperacjeApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**apiV2PermissionsOperationsOperationReferenceNumberGet()**](OperacjeApi.md#apiV2PermissionsOperationsOperationReferenceNumberGet) | **GET** /api/v2/permissions/operations/{operationReferenceNumber} | Pobranie statusu operacji |


## `apiV2PermissionsOperationsOperationReferenceNumberGet()`

```php
apiV2PermissionsOperationsOperationReferenceNumberGet($operation_reference_number): \OpenAPI\Client\Model\PermissionsOperationStatusResponse
```

Pobranie statusu operacji

Zwraca status operacji asynchronicznej związanej z nadaniem lub odebraniem uprawnień.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\OperacjeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$operation_reference_number = 'operation_reference_number_example'; // string | Numer referencyjny operacji

try {
    $result = $apiInstance->apiV2PermissionsOperationsOperationReferenceNumberGet($operation_reference_number);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OperacjeApi->apiV2PermissionsOperationsOperationReferenceNumberGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **operation_reference_number** | **string**| Numer referencyjny operacji | |

### Return type

[**\OpenAPI\Client\Model\PermissionsOperationStatusResponse**](../Model/PermissionsOperationStatusResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
