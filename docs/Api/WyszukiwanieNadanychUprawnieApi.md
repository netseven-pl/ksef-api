# NetSeven\WyszukiwanieNadanychUprawnieApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**apiV2PermissionsQueryAuthorizationsGrantsPost()**](WyszukiwanieNadanychUprawnieApi.md#apiV2PermissionsQueryAuthorizationsGrantsPost) | **POST** /api/v2/permissions/query/authorizations/grants | Pobranie listy uprawnień podmiotowych do obsługi faktur |
| [**apiV2PermissionsQueryEntitiesRolesGet()**](WyszukiwanieNadanychUprawnieApi.md#apiV2PermissionsQueryEntitiesRolesGet) | **GET** /api/v2/permissions/query/entities/roles | Pobranie listy ról podmiotu |
| [**apiV2PermissionsQueryEuEntitiesGrantsPost()**](WyszukiwanieNadanychUprawnieApi.md#apiV2PermissionsQueryEuEntitiesGrantsPost) | **POST** /api/v2/permissions/query/eu-entities/grants | Pobranie listy uprawnień administratorów lub reprezentantów podmiotów unijnych uprawnionych do samofakturowania |
| [**apiV2PermissionsQueryPersonsGrantsPost()**](WyszukiwanieNadanychUprawnieApi.md#apiV2PermissionsQueryPersonsGrantsPost) | **POST** /api/v2/permissions/query/persons/grants | Pobranie listy uprawnień do pracy w KSeF nadanych osobom fizycznym lub podmiotom |
| [**apiV2PermissionsQuerySubordinateEntitiesRolesPost()**](WyszukiwanieNadanychUprawnieApi.md#apiV2PermissionsQuerySubordinateEntitiesRolesPost) | **POST** /api/v2/permissions/query/subordinate-entities/roles | Pobranie listy podmiotów podrzędnych |
| [**apiV2PermissionsQuerySubunitsGrantsPost()**](WyszukiwanieNadanychUprawnieApi.md#apiV2PermissionsQuerySubunitsGrantsPost) | **POST** /api/v2/permissions/query/subunits/grants | Pobranie listy uprawnień administratorów jednostek i podmiotów podrzędnych |


## `apiV2PermissionsQueryAuthorizationsGrantsPost()`

```php
apiV2PermissionsQueryAuthorizationsGrantsPost($page_offset, $page_size, $entity_authorization_permissions_query_request): \NetSeven\KseF2Model\QueryEntityAuthorizationPermissionsResponse
```

Pobranie listy uprawnień podmiotowych do obsługi faktur

Zwraca listę uprawnień podmiotowych do obsługi faktur.    > Więcej informacji:  > - [Pobieranie listy uprawnień](https://github.com/CIRFMF/ksef-docs/blob/main/uprawnienia.md#pobranie-listy-uprawnie%C5%84-podmiotowych-do-obs%C5%82ugi-faktur)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new NetSeven\Api\WyszukiwanieNadanychUprawnieApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$page_offset = 56; // int | Numer strony wyników.
$page_size = 56; // int | Rozmiar strony wyników.
$entity_authorization_permissions_query_request = {"authorizedIdentifier":{"type":"Nip","value":"7762811692"},"queryType":"Granted","permissionTypes":["SelfInvoicing","TaxRepresentative","RRInvoicing"]}; // \NetSeven\KseF2Model\EntityAuthorizationPermissionsQueryRequest

try {
    $result = $apiInstance->apiV2PermissionsQueryAuthorizationsGrantsPost($page_offset, $page_size, $entity_authorization_permissions_query_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WyszukiwanieNadanychUprawnieApi->apiV2PermissionsQueryAuthorizationsGrantsPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page_offset** | **int**| Numer strony wyników. | [optional] |
| **page_size** | **int**| Rozmiar strony wyników. | [optional] |
| **entity_authorization_permissions_query_request** | [**\NetSeven\KseF2Model\EntityAuthorizationPermissionsQueryRequest**](../Model/EntityAuthorizationPermissionsQueryRequest.md)|  | [optional] |

### Return type

[**\NetSeven\KseF2Model\QueryEntityAuthorizationPermissionsResponse**](../Model/QueryEntityAuthorizationPermissionsResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `apiV2PermissionsQueryEntitiesRolesGet()`

```php
apiV2PermissionsQueryEntitiesRolesGet($page_offset, $page_size): \NetSeven\KseF2Model\QueryEntityRolesResponse
```

Pobranie listy ról podmiotu

Zwraca listę ról podmiotu.    > Więcej informacji:  > - [Pobieranie listy ról](https://github.com/CIRFMF/ksef-docs/blob/main/uprawnienia.md#pobranie-listy-r%C3%B3l-podmiotu)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new NetSeven\Api\WyszukiwanieNadanychUprawnieApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$page_offset = 56; // int | Numer strony wyników.
$page_size = 56; // int | Rozmiar strony wyników.

try {
    $result = $apiInstance->apiV2PermissionsQueryEntitiesRolesGet($page_offset, $page_size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WyszukiwanieNadanychUprawnieApi->apiV2PermissionsQueryEntitiesRolesGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page_offset** | **int**| Numer strony wyników. | [optional] |
| **page_size** | **int**| Rozmiar strony wyników. | [optional] |

### Return type

[**\NetSeven\KseF2Model\QueryEntityRolesResponse**](../Model/QueryEntityRolesResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `apiV2PermissionsQueryEuEntitiesGrantsPost()`

```php
apiV2PermissionsQueryEuEntitiesGrantsPost($page_offset, $page_size, $eu_entity_permissions_query_request): \NetSeven\KseF2Model\QueryEuEntityPermissionsResponse
```

Pobranie listy uprawnień administratorów lub reprezentantów podmiotów unijnych uprawnionych do samofakturowania

Zwraca listę uprawnień administratorów lub reprezentantów podmiotów unijnych uprawnionych do samofakturowania.    > Więcej informacji:  > - [Pobieranie listy uprawnień](https://github.com/CIRFMF/ksef-docs/blob/main/uprawnienia.md#pobranie-listy-uprawnie%C5%84-administrator%C3%B3w-lub-reprezentant%C3%B3w-podmiot%C3%B3w-unijnych-uprawnionych-do-samofakturowania)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new NetSeven\Api\WyszukiwanieNadanychUprawnieApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$page_offset = 56; // int | Numer strony wyników.
$page_size = 56; // int | Rozmiar strony wyników.
$eu_entity_permissions_query_request = {"vatUeIdentifier":"DE123456789012","permissionTypes":["VatUeManage","Introspection"]}; // \NetSeven\KseF2Model\EuEntityPermissionsQueryRequest

try {
    $result = $apiInstance->apiV2PermissionsQueryEuEntitiesGrantsPost($page_offset, $page_size, $eu_entity_permissions_query_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WyszukiwanieNadanychUprawnieApi->apiV2PermissionsQueryEuEntitiesGrantsPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page_offset** | **int**| Numer strony wyników. | [optional] |
| **page_size** | **int**| Rozmiar strony wyników. | [optional] |
| **eu_entity_permissions_query_request** | [**\NetSeven\KseF2Model\EuEntityPermissionsQueryRequest**](../Model/EuEntityPermissionsQueryRequest.md)|  | [optional] |

### Return type

[**\NetSeven\KseF2Model\QueryEuEntityPermissionsResponse**](../Model/QueryEuEntityPermissionsResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `apiV2PermissionsQueryPersonsGrantsPost()`

```php
apiV2PermissionsQueryPersonsGrantsPost($page_offset, $page_size, $person_permissions_query_request): \NetSeven\KseF2Model\QueryPersonPermissionsResponse
```

Pobranie listy uprawnień do pracy w KSeF nadanych osobom fizycznym lub podmiotom

Zwraca listę uprawnień do pracy w KSeF nadanych osobom fizycznym lub podmiotom.    > Więcej informacji:  > - [Pobieranie listy uprawnień](https://github.com/CIRFMF/ksef-docs/blob/main/uprawnienia.md#pobranie-listy-uprawnie%C5%84-do-pracy-w-ksef-nadanych-osobom-fizycznym-lub-podmiotom)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new NetSeven\Api\WyszukiwanieNadanychUprawnieApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$page_offset = 56; // int | Numer strony wyników.
$page_size = 56; // int | Rozmiar strony wyników.
$person_permissions_query_request = {"authorIdentifier":{"type":"Nip","value":"7762811692"},"permissionTypes":["CredentialsManage","CredentialsRead","InvoiceWrite"],"permissionState":"Active","queryType":"PermissionsInCurrentContext"}; // \NetSeven\KseF2Model\PersonPermissionsQueryRequest

try {
    $result = $apiInstance->apiV2PermissionsQueryPersonsGrantsPost($page_offset, $page_size, $person_permissions_query_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WyszukiwanieNadanychUprawnieApi->apiV2PermissionsQueryPersonsGrantsPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page_offset** | **int**| Numer strony wyników. | [optional] |
| **page_size** | **int**| Rozmiar strony wyników. | [optional] |
| **person_permissions_query_request** | [**\NetSeven\KseF2Model\PersonPermissionsQueryRequest**](../Model/PersonPermissionsQueryRequest.md)|  | [optional] |

### Return type

[**\NetSeven\KseF2Model\QueryPersonPermissionsResponse**](../Model/QueryPersonPermissionsResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `apiV2PermissionsQuerySubordinateEntitiesRolesPost()`

```php
apiV2PermissionsQuerySubordinateEntitiesRolesPost($page_offset, $page_size, $subordinate_entity_roles_query_request): \NetSeven\KseF2Model\QuerySubordinateEntityRolesResponse
```

Pobranie listy podmiotów podrzędnych

Zwraca liste podmiotów podrzędnych.    > Więcej informacji:  > - [Pobieranie listy podmiotów podrzędnych](https://github.com/CIRFMF/ksef-docs/blob/main/uprawnienia.md#pobranie-listy-podmiot%C3%B3w-podrz%C4%99dnych)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new NetSeven\Api\WyszukiwanieNadanychUprawnieApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$page_offset = 56; // int | Numer strony wyników.
$page_size = 56; // int | Rozmiar strony wyników.
$subordinate_entity_roles_query_request = {"subordinateEntityIdentifier":{"type":"Nip","value":"7762811692"}}; // \NetSeven\KseF2Model\SubordinateEntityRolesQueryRequest

try {
    $result = $apiInstance->apiV2PermissionsQuerySubordinateEntitiesRolesPost($page_offset, $page_size, $subordinate_entity_roles_query_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WyszukiwanieNadanychUprawnieApi->apiV2PermissionsQuerySubordinateEntitiesRolesPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page_offset** | **int**| Numer strony wyników. | [optional] |
| **page_size** | **int**| Rozmiar strony wyników. | [optional] |
| **subordinate_entity_roles_query_request** | [**\NetSeven\KseF2Model\SubordinateEntityRolesQueryRequest**](../Model/SubordinateEntityRolesQueryRequest.md)|  | [optional] |

### Return type

[**\NetSeven\KseF2Model\QuerySubordinateEntityRolesResponse**](../Model/QuerySubordinateEntityRolesResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `apiV2PermissionsQuerySubunitsGrantsPost()`

```php
apiV2PermissionsQuerySubunitsGrantsPost($page_offset, $page_size, $subunit_permissions_query_request): \NetSeven\KseF2Model\QuerySubunitPermissionsResponse
```

Pobranie listy uprawnień administratorów jednostek i podmiotów podrzędnych

Zwraca listę uprawnień administratorów jednostek i podmiotów podrzędnych.    > Więcej informacji:  > - [Pobieranie listy uprawnień](https://github.com/CIRFMF/ksef-docs/blob/main/uprawnienia.md#pobranie-listy-uprawnie%C5%84-administrator%C3%B3w-jednostek-i-podmiot%C3%B3w-podrz%C4%99dnych)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new NetSeven\Api\WyszukiwanieNadanychUprawnieApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$page_offset = 56; // int | Numer strony wyników.
$page_size = 56; // int | Rozmiar strony wyników.
$subunit_permissions_query_request = {"subunitIdentifier":{"type":"InternalId","value":"7762811692-12345"}}; // \NetSeven\KseF2Model\SubunitPermissionsQueryRequest

try {
    $result = $apiInstance->apiV2PermissionsQuerySubunitsGrantsPost($page_offset, $page_size, $subunit_permissions_query_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WyszukiwanieNadanychUprawnieApi->apiV2PermissionsQuerySubunitsGrantsPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page_offset** | **int**| Numer strony wyników. | [optional] |
| **page_size** | **int**| Rozmiar strony wyników. | [optional] |
| **subunit_permissions_query_request** | [**\NetSeven\KseF2Model\SubunitPermissionsQueryRequest**](../Model/SubunitPermissionsQueryRequest.md)|  | [optional] |

### Return type

[**\NetSeven\KseF2Model\QuerySubunitPermissionsResponse**](../Model/QuerySubunitPermissionsResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
