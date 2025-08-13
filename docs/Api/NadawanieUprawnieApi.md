# NetSeven\NadawanieUprawnieApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**apiV2PermissionsAuthorizationsGrantsPost()**](NadawanieUprawnieApi.md#apiV2PermissionsAuthorizationsGrantsPost) | **POST** /api/v2/permissions/authorizations/grants | Nadanie uprawnień podmiotowych |
| [**apiV2PermissionsEntitiesGrantsPost()**](NadawanieUprawnieApi.md#apiV2PermissionsEntitiesGrantsPost) | **POST** /api/v2/permissions/entities/grants | Nadanie podmiotom uprawnień do obsługi faktur |
| [**apiV2PermissionsEuEntitiesAdministrationGrantsPost()**](NadawanieUprawnieApi.md#apiV2PermissionsEuEntitiesAdministrationGrantsPost) | **POST** /api/v2/permissions/eu-entities/administration/grants | Nadanie uprawnień administratora podmiotu unijnego |
| [**apiV2PermissionsEuEntitiesGrantsPost()**](NadawanieUprawnieApi.md#apiV2PermissionsEuEntitiesGrantsPost) | **POST** /api/v2/permissions/eu-entities/grants | Nadanie uprawnień reprezentanta podmiotu unijnego |
| [**apiV2PermissionsIndirectGrantsPost()**](NadawanieUprawnieApi.md#apiV2PermissionsIndirectGrantsPost) | **POST** /api/v2/permissions/indirect/grants | Nadanie uprawnień w sposób pośredni |
| [**apiV2PermissionsPersonsGrantsPost()**](NadawanieUprawnieApi.md#apiV2PermissionsPersonsGrantsPost) | **POST** /api/v2/permissions/persons/grants | Nadanie osobom fizycznym uprawnień do pracy w KSeF |
| [**apiV2PermissionsSubunitsGrantsPost()**](NadawanieUprawnieApi.md#apiV2PermissionsSubunitsGrantsPost) | **POST** /api/v2/permissions/subunits/grants | Nadanie uprawnień administratora podmiotu podrzędnego |


## `apiV2PermissionsAuthorizationsGrantsPost()`

```php
apiV2PermissionsAuthorizationsGrantsPost($entity_authorization_permissions_grant_request): \NetSeven\KseF2Model\PermissionsOperationResponse
```

Nadanie uprawnień podmiotowych

Rozpoczyna asynchroniczną operację nadawania uprawnień podmiotowych.    > Więcej informacji:  > - [Nadawanie uprawnień](https://github.com/CIRFMF/ksef-docs/blob/main/uprawnienia.md#nadanie-uprawnie%C5%84-podmiotowych)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new NetSeven\Api\NadawanieUprawnieApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$entity_authorization_permissions_grant_request = {"subjectIdentifier":{"type":"Nip","value":"7762811692"},"permission":"SelfInvoicing","description":"Uprawnienia do samofakturowania"}; // \NetSeven\KseF2Model\EntityAuthorizationPermissionsGrantRequest

try {
    $result = $apiInstance->apiV2PermissionsAuthorizationsGrantsPost($entity_authorization_permissions_grant_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NadawanieUprawnieApi->apiV2PermissionsAuthorizationsGrantsPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **entity_authorization_permissions_grant_request** | [**\NetSeven\KseF2Model\EntityAuthorizationPermissionsGrantRequest**](../Model/EntityAuthorizationPermissionsGrantRequest.md)|  | [optional] |

### Return type

[**\NetSeven\KseF2Model\PermissionsOperationResponse**](../Model/PermissionsOperationResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `apiV2PermissionsEntitiesGrantsPost()`

```php
apiV2PermissionsEntitiesGrantsPost($entity_permissions_grant_request): \NetSeven\KseF2Model\PermissionsOperationResponse
```

Nadanie podmiotom uprawnień do obsługi faktur

Rozpoczyna asynchroniczną operację nadawania podmiotom uprawnień do obsługi faktur.    > Więcej informacji:  > - [Nadawanie uprawnień](https://github.com/CIRFMF/ksef-docs/blob/main/uprawnienia.md#nadanie-podmiotom-uprawnie%C5%84-do-obs%C5%82ugi-faktur)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new NetSeven\Api\NadawanieUprawnieApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$entity_permissions_grant_request = {"subjectIdentifier":{"type":"Nip","value":"7762811692"},"permissions":[{"type":"InvoiceRead","canDelegate":true},{"type":"InvoiceWrite","canDelegate":true}],"description":"Uprawnienia do odczytu i wysyłania faktur z możliwością nadania ich pośrednio"}; // \NetSeven\KseF2Model\EntityPermissionsGrantRequest

try {
    $result = $apiInstance->apiV2PermissionsEntitiesGrantsPost($entity_permissions_grant_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NadawanieUprawnieApi->apiV2PermissionsEntitiesGrantsPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **entity_permissions_grant_request** | [**\NetSeven\KseF2Model\EntityPermissionsGrantRequest**](../Model/EntityPermissionsGrantRequest.md)|  | [optional] |

### Return type

[**\NetSeven\KseF2Model\PermissionsOperationResponse**](../Model/PermissionsOperationResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `apiV2PermissionsEuEntitiesAdministrationGrantsPost()`

```php
apiV2PermissionsEuEntitiesAdministrationGrantsPost($eu_entity_administration_permissions_grant_request): \NetSeven\KseF2Model\PermissionsOperationResponse
```

Nadanie uprawnień administratora podmiotu unijnego

Rozpoczyna asynchroniczną operację nadawania uprawnień administratora podmiotu unijnego.    > Więcej informacji:  > - [Nadawanie uprawnień](https://github.com/CIRFMF/ksef-docs/blob/main/uprawnienia.md#nadanie-uprawnie%C5%84-administratora-podmiotu-unijnego)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new NetSeven\Api\NadawanieUprawnieApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$eu_entity_administration_permissions_grant_request = {"subjectIdentifier":{"type":"Fingerprint","value":"CEB3643BAC2C111ADDE971BDA5A80163441867D65389FC0BC0DFF8B4C1CD4E59"},"contextIdentifier":{"type":"NipVatUe","value":"7762811692-DE123456789012"},"description":"Administrator podmiotu unijnego DE123456789012"}; // \NetSeven\KseF2Model\EuEntityAdministrationPermissionsGrantRequest

try {
    $result = $apiInstance->apiV2PermissionsEuEntitiesAdministrationGrantsPost($eu_entity_administration_permissions_grant_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NadawanieUprawnieApi->apiV2PermissionsEuEntitiesAdministrationGrantsPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **eu_entity_administration_permissions_grant_request** | [**\NetSeven\KseF2Model\EuEntityAdministrationPermissionsGrantRequest**](../Model/EuEntityAdministrationPermissionsGrantRequest.md)|  | [optional] |

### Return type

[**\NetSeven\KseF2Model\PermissionsOperationResponse**](../Model/PermissionsOperationResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `apiV2PermissionsEuEntitiesGrantsPost()`

```php
apiV2PermissionsEuEntitiesGrantsPost($eu_entity_permissions_grant_request): \NetSeven\KseF2Model\PermissionsOperationResponse
```

Nadanie uprawnień reprezentanta podmiotu unijnego

Rozpoczyna asynchroniczną operację nadawania uprawnień reprezentanta podmiotu unijnego.    > Więcej informacji:  > - [Nadawanie uprawnień](https://github.com/CIRFMF/ksef-docs/blob/main/uprawnienia.md#nadanie-uprawnie%C5%84-reprezentanta-podmiotu-unijnego)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new NetSeven\Api\NadawanieUprawnieApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$eu_entity_permissions_grant_request = {"subjectIdentifier":{"type":"Fingerprint","value":"CEB3643BAC2C111ADDE971BDA5A80163441867D65389FC0BC0DFF8B4C1CD4E59"},"permissions":["InvoiceRead","InvoiceWrite"],"description":"Reprezentant podmiotu unijnego"}; // \NetSeven\KseF2Model\EuEntityPermissionsGrantRequest

try {
    $result = $apiInstance->apiV2PermissionsEuEntitiesGrantsPost($eu_entity_permissions_grant_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NadawanieUprawnieApi->apiV2PermissionsEuEntitiesGrantsPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **eu_entity_permissions_grant_request** | [**\NetSeven\KseF2Model\EuEntityPermissionsGrantRequest**](../Model/EuEntityPermissionsGrantRequest.md)|  | [optional] |

### Return type

[**\NetSeven\KseF2Model\PermissionsOperationResponse**](../Model/PermissionsOperationResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `apiV2PermissionsIndirectGrantsPost()`

```php
apiV2PermissionsIndirectGrantsPost($indirect_permissions_grant_request): \NetSeven\KseF2Model\PermissionsOperationResponse
```

Nadanie uprawnień w sposób pośredni

Rozpoczyna asynchroniczną operację nadawania uprawnień w sposób pośredni.    > Więcej informacji:  > - [Nadawanie uprawnień](https://github.com/CIRFMF/ksef-docs/blob/main/uprawnienia.md#nadanie-uprawnie%C5%84-w-spos%C3%B3b-po%C5%9Bredni)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new NetSeven\Api\NadawanieUprawnieApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$indirect_permissions_grant_request = {"subjectIdentifier":{"type":"Pesel","value":"15062788702"},"permissions":["InvoiceWrite","InvoiceRead"],"description":"Uprawnienia generalne do odczytu i wysyłania faktur, nadane w sposób pośredni"}; // \NetSeven\KseF2Model\IndirectPermissionsGrantRequest

try {
    $result = $apiInstance->apiV2PermissionsIndirectGrantsPost($indirect_permissions_grant_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NadawanieUprawnieApi->apiV2PermissionsIndirectGrantsPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **indirect_permissions_grant_request** | [**\NetSeven\KseF2Model\IndirectPermissionsGrantRequest**](../Model/IndirectPermissionsGrantRequest.md)|  | [optional] |

### Return type

[**\NetSeven\KseF2Model\PermissionsOperationResponse**](../Model/PermissionsOperationResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `apiV2PermissionsPersonsGrantsPost()`

```php
apiV2PermissionsPersonsGrantsPost($person_permissions_grant_request): \NetSeven\KseF2Model\PermissionsOperationResponse
```

Nadanie osobom fizycznym uprawnień do pracy w KSeF

Rozpoczyna asynchroniczną operację nadawania osobom fizycznym uprawnień do pracy w KSeF.    > Więcej informacji:  > - [Nadawanie uprawnień](https://github.com/CIRFMF/ksef-docs/blob/main/uprawnienia.md#nadawanie-uprawnie%C5%84-osobom-fizycznym-do-pracy-w-ksef)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new NetSeven\Api\NadawanieUprawnieApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$person_permissions_grant_request = {"subjectIdentifier":{"type":"Pesel","value":"15062788702"},"permissions":["InvoiceRead","InvoiceWrite"],"description":"Uprawnienia do odczytu i wysyłania faktur"}; // \NetSeven\KseF2Model\PersonPermissionsGrantRequest

try {
    $result = $apiInstance->apiV2PermissionsPersonsGrantsPost($person_permissions_grant_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NadawanieUprawnieApi->apiV2PermissionsPersonsGrantsPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **person_permissions_grant_request** | [**\NetSeven\KseF2Model\PersonPermissionsGrantRequest**](../Model/PersonPermissionsGrantRequest.md)|  | [optional] |

### Return type

[**\NetSeven\KseF2Model\PermissionsOperationResponse**](../Model/PermissionsOperationResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `apiV2PermissionsSubunitsGrantsPost()`

```php
apiV2PermissionsSubunitsGrantsPost($subunit_permissions_grant_request): \NetSeven\KseF2Model\PermissionsOperationResponse
```

Nadanie uprawnień administratora podmiotu podrzędnego

Rozpoczyna asynchroniczną operację nadawania uprawnień administratora podmiotu podrzędnego.    > Więcej informacji:  > - [Nadawanie uprawnień](https://github.com/CIRFMF/ksef-docs/blob/main/uprawnienia.md#nadanie-uprawnie%C5%84-administratora-podmiotu-podrz%C4%99dnego)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new NetSeven\Api\NadawanieUprawnieApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$subunit_permissions_grant_request = {"subjectIdentifier":{"type":"Pesel","value":"15062788702"},"contextIdentifier":{"type":"InternalId","value":"7762811692-11111"},"description":"Administrator jednostki podrzędnej"}; // \NetSeven\KseF2Model\SubunitPermissionsGrantRequest

try {
    $result = $apiInstance->apiV2PermissionsSubunitsGrantsPost($subunit_permissions_grant_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NadawanieUprawnieApi->apiV2PermissionsSubunitsGrantsPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **subunit_permissions_grant_request** | [**\NetSeven\KseF2Model\SubunitPermissionsGrantRequest**](../Model/SubunitPermissionsGrantRequest.md)|  | [optional] |

### Return type

[**\NetSeven\KseF2Model\PermissionsOperationResponse**](../Model/PermissionsOperationResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
