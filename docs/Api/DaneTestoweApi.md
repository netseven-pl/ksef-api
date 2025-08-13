# NetSeven\DaneTestoweApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**apiV2TestdataPermissionsPost()**](DaneTestoweApi.md#apiV2TestdataPermissionsPost) | **POST** /api/v2/testdata/permissions | Nadanie uprawnień testowemu podmiotowi/osobie fizycznej |
| [**apiV2TestdataPermissionsRevokePost()**](DaneTestoweApi.md#apiV2TestdataPermissionsRevokePost) | **POST** /api/v2/testdata/permissions/revoke | Odebranie uprawnień testowemu podmiotowi/osobie fizycznej |
| [**apiV2TestdataPersonPost()**](DaneTestoweApi.md#apiV2TestdataPersonPost) | **POST** /api/v2/testdata/person | Utworzenie osoby fizycznej |
| [**apiV2TestdataPersonRemovePost()**](DaneTestoweApi.md#apiV2TestdataPersonRemovePost) | **POST** /api/v2/testdata/person/remove | Usunięcie osoby fizycznej |
| [**apiV2TestdataSubjectPost()**](DaneTestoweApi.md#apiV2TestdataSubjectPost) | **POST** /api/v2/testdata/subject | Utworzenie podmiotu |
| [**apiV2TestdataSubjectRemovePost()**](DaneTestoweApi.md#apiV2TestdataSubjectRemovePost) | **POST** /api/v2/testdata/subject/remove | Usunięcie podmiotu |


## `apiV2TestdataPermissionsPost()`

```php
apiV2TestdataPermissionsPost($test_data_permissions_grant_request)
```

Nadanie uprawnień testowemu podmiotowi/osobie fizycznej

Nadawanie uprawnień testowemu podmiotowi lub osobie fizycznej, a także w ich kontekście.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new NetSeven\Api\DaneTestoweApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$test_data_permissions_grant_request = new \NetSeven\KseF2Model\TestDataPermissionsGrantRequest(); // \NetSeven\KseF2Model\TestDataPermissionsGrantRequest

try {
    $apiInstance->apiV2TestdataPermissionsPost($test_data_permissions_grant_request);
} catch (Exception $e) {
    echo 'Exception when calling DaneTestoweApi->apiV2TestdataPermissionsPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **test_data_permissions_grant_request** | [**\NetSeven\KseF2Model\TestDataPermissionsGrantRequest**](../Model/TestDataPermissionsGrantRequest.md)|  | [optional] |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `apiV2TestdataPermissionsRevokePost()`

```php
apiV2TestdataPermissionsRevokePost($test_data_permissions_revoke_request)
```

Odebranie uprawnień testowemu podmiotowi/osobie fizycznej

Odbieranie uprawnień nadanych testowemu podmiotowi lub osobie fizycznej, a także w ich kontekście.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new NetSeven\Api\DaneTestoweApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$test_data_permissions_revoke_request = new \NetSeven\KseF2Model\TestDataPermissionsRevokeRequest(); // \NetSeven\KseF2Model\TestDataPermissionsRevokeRequest

try {
    $apiInstance->apiV2TestdataPermissionsRevokePost($test_data_permissions_revoke_request);
} catch (Exception $e) {
    echo 'Exception when calling DaneTestoweApi->apiV2TestdataPermissionsRevokePost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **test_data_permissions_revoke_request** | [**\NetSeven\KseF2Model\TestDataPermissionsRevokeRequest**](../Model/TestDataPermissionsRevokeRequest.md)|  | [optional] |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `apiV2TestdataPersonPost()`

```php
apiV2TestdataPersonPost($person_create_request)
```

Utworzenie osoby fizycznej

Tworzenie nowej osoby fizycznej, której system nadaje uprawnienia właścicielskie. Można również określić, czy osoba ta jest komornikiem – wówczas otrzyma odpowiednie uprawnienie egzekucyjne.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new NetSeven\Api\DaneTestoweApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$person_create_request = new \NetSeven\KseF2Model\PersonCreateRequest(); // \NetSeven\KseF2Model\PersonCreateRequest

try {
    $apiInstance->apiV2TestdataPersonPost($person_create_request);
} catch (Exception $e) {
    echo 'Exception when calling DaneTestoweApi->apiV2TestdataPersonPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **person_create_request** | [**\NetSeven\KseF2Model\PersonCreateRequest**](../Model/PersonCreateRequest.md)|  | [optional] |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `apiV2TestdataPersonRemovePost()`

```php
apiV2TestdataPersonRemovePost($person_remove_request)
```

Usunięcie osoby fizycznej

Usuwanie testowej osoby fizycznej. System automatycznie odbierze jej wszystkie uprawnienia.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new NetSeven\Api\DaneTestoweApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$person_remove_request = new \NetSeven\KseF2Model\PersonRemoveRequest(); // \NetSeven\KseF2Model\PersonRemoveRequest

try {
    $apiInstance->apiV2TestdataPersonRemovePost($person_remove_request);
} catch (Exception $e) {
    echo 'Exception when calling DaneTestoweApi->apiV2TestdataPersonRemovePost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **person_remove_request** | [**\NetSeven\KseF2Model\PersonRemoveRequest**](../Model/PersonRemoveRequest.md)|  | [optional] |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `apiV2TestdataSubjectPost()`

```php
apiV2TestdataSubjectPost($subject_create_request)
```

Utworzenie podmiotu

Tworzenie nowego podmiotu testowego. W przypadku grupy VAT i JST istnieje możliwość stworzenia jednostek podrzędnych. W wyniku takiego działania w systemie powstanie powiązanie między tymi podmiotami.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new NetSeven\Api\DaneTestoweApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$subject_create_request = new \NetSeven\KseF2Model\SubjectCreateRequest(); // \NetSeven\KseF2Model\SubjectCreateRequest

try {
    $apiInstance->apiV2TestdataSubjectPost($subject_create_request);
} catch (Exception $e) {
    echo 'Exception when calling DaneTestoweApi->apiV2TestdataSubjectPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **subject_create_request** | [**\NetSeven\KseF2Model\SubjectCreateRequest**](../Model/SubjectCreateRequest.md)|  | [optional] |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `apiV2TestdataSubjectRemovePost()`

```php
apiV2TestdataSubjectRemovePost($subject_remove_request)
```

Usunięcie podmiotu

Usuwanie podmiotu testowego. W przypadku grupy VAT i JST usunięte zostaną również jednostki podrzędne.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new NetSeven\Api\DaneTestoweApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$subject_remove_request = new \NetSeven\KseF2Model\SubjectRemoveRequest(); // \NetSeven\KseF2Model\SubjectRemoveRequest

try {
    $apiInstance->apiV2TestdataSubjectRemovePost($subject_remove_request);
} catch (Exception $e) {
    echo 'Exception when calling DaneTestoweApi->apiV2TestdataSubjectRemovePost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **subject_remove_request** | [**\NetSeven\KseF2Model\SubjectRemoveRequest**](../Model/SubjectRemoveRequest.md)|  | [optional] |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
