# OpenAPI\Client\PobieranieFakturApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**apiV2InvoicesAsyncQueryOperationReferenceNumberGet()**](PobieranieFakturApi.md#apiV2InvoicesAsyncQueryOperationReferenceNumberGet) | **GET** /api/v2/invoices/async-query/{operationReferenceNumber} | [mock] Sprawdza status asynchronicznego zapytania o pobranie faktur |
| [**apiV2InvoicesAsyncQueryPost()**](PobieranieFakturApi.md#apiV2InvoicesAsyncQueryPost) | **POST** /api/v2/invoices/async-query | [mock] Inicjalizuje asynchroniczne zapytanie o pobranie faktur |
| [**apiV2InvoicesDownloadPost()**](PobieranieFakturApi.md#apiV2InvoicesDownloadPost) | **POST** /api/v2/invoices/download | [mock]Pobranie faktury  na podstawie numeru KSeF oraz danych faktury |
| [**apiV2InvoicesKsefKsefNumberGet()**](PobieranieFakturApi.md#apiV2InvoicesKsefKsefNumberGet) | **GET** /api/v2/invoices/ksef/{ksefNumber} | Pobranie faktury po numerze KSeF |
| [**apiV2InvoicesQueryPost()**](PobieranieFakturApi.md#apiV2InvoicesQueryPost) | **POST** /api/v2/invoices/query | [mock] Pobranie listy metadanych faktur |


## `apiV2InvoicesAsyncQueryOperationReferenceNumberGet()`

```php
apiV2InvoicesAsyncQueryOperationReferenceNumberGet($operation_reference_number): \OpenAPI\Client\Model\AsyncInvoicesQueryStatus
```

[mock] Sprawdza status asynchronicznego zapytania o pobranie faktur

Pobiera status wcześniej zainicjalizowanego zapytania asynchronicznego na podstawie identyfikatora operacji.  Umożliwia śledzenie postępu przetwarzania zapytania oraz pobranie gotowych paczek z wynikami, jeśli są już dostępne.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\PobieranieFakturApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$operation_reference_number = 'operation_reference_number_example'; // string | Unikalny identyfikator operacji zwrócony podczas inicjalizacji zapytania.

try {
    $result = $apiInstance->apiV2InvoicesAsyncQueryOperationReferenceNumberGet($operation_reference_number);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PobieranieFakturApi->apiV2InvoicesAsyncQueryOperationReferenceNumberGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **operation_reference_number** | **string**| Unikalny identyfikator operacji zwrócony podczas inicjalizacji zapytania. | |

### Return type

[**\OpenAPI\Client\Model\AsyncInvoicesQueryStatus**](../Model/AsyncInvoicesQueryStatus.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `apiV2InvoicesAsyncQueryPost()`

```php
apiV2InvoicesAsyncQueryPost($invoices_async_query_request): \OpenAPI\Client\Model\InitAsyncInvoicesQueryResponse
```

[mock] Inicjalizuje asynchroniczne zapytanie o pobranie faktur

Rozpoczyna asynchroniczny proces wyszukiwania faktur w systemie KSeF na podstawie przekazanych filtrów.  Wymagane jest przekazanie informacji o szyfrowaniu w polu `Encryption`, które służą do zaszyfrowania wygenerowanych paczek z fakturami.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\PobieranieFakturApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$invoices_async_query_request = new \OpenAPI\Client\Model\InvoicesAsyncQueryRequest(); // \OpenAPI\Client\Model\InvoicesAsyncQueryRequest | Zestaw filtrów dla wyszukiwania faktur.

try {
    $result = $apiInstance->apiV2InvoicesAsyncQueryPost($invoices_async_query_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PobieranieFakturApi->apiV2InvoicesAsyncQueryPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **invoices_async_query_request** | [**\OpenAPI\Client\Model\InvoicesAsyncQueryRequest**](../Model/InvoicesAsyncQueryRequest.md)| Zestaw filtrów dla wyszukiwania faktur. | [optional] |

### Return type

[**\OpenAPI\Client\Model\InitAsyncInvoicesQueryResponse**](../Model/InitAsyncInvoicesQueryResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `apiV2InvoicesDownloadPost()`

```php
apiV2InvoicesDownloadPost($download_invoice_request): string
```

[mock]Pobranie faktury  na podstawie numeru KSeF oraz danych faktury

Faktura zostanie zwrócona wyłącznie, jeśli wszystkie dane wejściowe są zgodne z danymi faktury w systemie.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\PobieranieFakturApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$download_invoice_request = new \OpenAPI\Client\Model\DownloadInvoiceRequest(); // \OpenAPI\Client\Model\DownloadInvoiceRequest

try {
    $result = $apiInstance->apiV2InvoicesDownloadPost($download_invoice_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PobieranieFakturApi->apiV2InvoicesDownloadPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **download_invoice_request** | [**\OpenAPI\Client\Model\DownloadInvoiceRequest**](../Model/DownloadInvoiceRequest.md)|  | [optional] |

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/xml`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `apiV2InvoicesKsefKsefNumberGet()`

```php
apiV2InvoicesKsefKsefNumberGet($ksef_number): string
```

Pobranie faktury po numerze KSeF

Zwraca fakturę o podanym numerze KSeF.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\PobieranieFakturApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$ksef_number = 'ksef_number_example'; // string | Numer KSeF faktury.

try {
    $result = $apiInstance->apiV2InvoicesKsefKsefNumberGet($ksef_number);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PobieranieFakturApi->apiV2InvoicesKsefKsefNumberGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **ksef_number** | **string**| Numer KSeF faktury. | |

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/xml`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `apiV2InvoicesQueryPost()`

```php
apiV2InvoicesQueryPost($page_offset, $page_size, $invoices_query_request): \OpenAPI\Client\Model\QueryInvoicesReponse
```

[mock] Pobranie listy metadanych faktur

Zwraca listę metadanych faktur spełniające podane kryteria wyszukiwania.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\PobieranieFakturApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$page_offset = 56; // int | Indeks pierwszej strony wyników (domyślnie 0).
$page_size = 56; // int | Rozmiar strony wyników(domyślnie 10).
$invoices_query_request = new \OpenAPI\Client\Model\InvoicesQueryRequest(); // \OpenAPI\Client\Model\InvoicesQueryRequest | Zestaw filtrów dla wyszukiwania metadanych.

try {
    $result = $apiInstance->apiV2InvoicesQueryPost($page_offset, $page_size, $invoices_query_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PobieranieFakturApi->apiV2InvoicesQueryPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page_offset** | **int**| Indeks pierwszej strony wyników (domyślnie 0). | [optional] |
| **page_size** | **int**| Rozmiar strony wyników(domyślnie 10). | [optional] |
| **invoices_query_request** | [**\OpenAPI\Client\Model\InvoicesQueryRequest**](../Model/InvoicesQueryRequest.md)| Zestaw filtrów dla wyszukiwania metadanych. | [optional] |

### Return type

[**\OpenAPI\Client\Model\QueryInvoicesReponse**](../Model/QueryInvoicesReponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
