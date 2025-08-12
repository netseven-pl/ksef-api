# OpenAPI\Client\StatusWysykiIUPOApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**apiV2SessionsGet()**](StatusWysykiIUPOApi.md#apiV2SessionsGet) | **GET** /api/v2/sessions | Pobranie listy sesji |
| [**apiV2SessionsReferenceNumberGet()**](StatusWysykiIUPOApi.md#apiV2SessionsReferenceNumberGet) | **GET** /api/v2/sessions/{referenceNumber} | Pobranie statusu sesji |
| [**apiV2SessionsReferenceNumberInvoicesFailedGet()**](StatusWysykiIUPOApi.md#apiV2SessionsReferenceNumberInvoicesFailedGet) | **GET** /api/v2/sessions/{referenceNumber}/invoices/failed | Pobranie niepoprawnie przetworzonych faktur sesji |
| [**apiV2SessionsReferenceNumberInvoicesGet()**](StatusWysykiIUPOApi.md#apiV2SessionsReferenceNumberInvoicesGet) | **GET** /api/v2/sessions/{referenceNumber}/invoices | Pobranie faktur sesji |
| [**apiV2SessionsReferenceNumberInvoicesInvoiceReferenceNumberGet()**](StatusWysykiIUPOApi.md#apiV2SessionsReferenceNumberInvoicesInvoiceReferenceNumberGet) | **GET** /api/v2/sessions/{referenceNumber}/invoices/{invoiceReferenceNumber} | Pobranie statusu faktury z sesji |
| [**apiV2SessionsReferenceNumberInvoicesInvoiceReferenceNumberUpoGet()**](StatusWysykiIUPOApi.md#apiV2SessionsReferenceNumberInvoicesInvoiceReferenceNumberUpoGet) | **GET** /api/v2/sessions/{referenceNumber}/invoices/{invoiceReferenceNumber}/upo | Pobranie UPO faktury z sesji na podstawie numeru referencyjnego faktury |
| [**apiV2SessionsReferenceNumberInvoicesKsefKsefNumberUpoGet()**](StatusWysykiIUPOApi.md#apiV2SessionsReferenceNumberInvoicesKsefKsefNumberUpoGet) | **GET** /api/v2/sessions/{referenceNumber}/invoices/ksef/{ksefNumber}/upo | Pobranie UPO faktury z sesji na podstawie numeru KSeF |
| [**apiV2SessionsReferenceNumberUpoUpoReferenceNumberGet()**](StatusWysykiIUPOApi.md#apiV2SessionsReferenceNumberUpoUpoReferenceNumberGet) | **GET** /api/v2/sessions/{referenceNumber}/upo/{upoReferenceNumber} | Pobranie UPO dla sesji |


## `apiV2SessionsGet()`

```php
apiV2SessionsGet($session_type, $page_size, $reference_number, $date_created_from, $date_created_to, $date_closed_from, $date_closed_to, $date_modified_from, $date_modified_to, $statuses, $x_continuation_token): \OpenAPI\Client\Model\SessionsQueryResponse
```

Pobranie listy sesji

Zwraca listę sesji spełniających podane kryteria wyszukiwania.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\StatusWysykiIUPOApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$session_type = 'session_type_example'; // \OpenAPIClientModelSessionType | Typ sesji.  | Wartość | Opis |  | --- | --- |  | Online | Wysyłka interaktywna (pojedyncze faktury). |  | Batch | Wysyłka wsadowa (paczka faktur). |
$page_size = 56; // int | Rozmiar strony.
$reference_number = 'reference_number_example'; // string | Numer referencyjny sesji.
$date_created_from = new \DateTime('2013-10-20T19:20:30+01:00'); // \DateTime | Data utworzenia sesji (od).
$date_created_to = new \DateTime('2013-10-20T19:20:30+01:00'); // \DateTime | Data utworzenia sesji (do).
$date_closed_from = new \DateTime('2013-10-20T19:20:30+01:00'); // \DateTime | Data zamknięcia sesji (od).
$date_closed_to = new \DateTime('2013-10-20T19:20:30+01:00'); // \DateTime | Data zamknięcia sesji (do).
$date_modified_from = new \DateTime('2013-10-20T19:20:30+01:00'); // \DateTime | Data ostatniej aktywności (wysyłka faktury lub zmiana statusu) w ramach sesji (od).
$date_modified_to = new \DateTime('2013-10-20T19:20:30+01:00'); // \DateTime | Data ostatniej aktywności (wysyłka faktury lub zmiana statusu) w ramach sesji (do).
$statuses = array(new \OpenAPI\Client\Model\\OpenAPI\Client\Model\CommonSessionStatus()); // \OpenAPI\Client\Model\CommonSessionStatus[] | Statusy sesji.  | Wartość | Opis |  | --- | --- |  | Succeeded | Sesja przetworzona poprawnie.            W trakcie przetwarzania sesji nie wystąpiły żadne błędy, ale część faktur nadal mogła zostać odrzucona. |  | InProgress | Sesja aktywna. |  | Failed | Sesja nie przetworzona z powodu błędów.            Na etapie rozpoczynania lub kończenia sesji wystąpiły błędy, które nie pozwoliły na jej poprawne przetworzenie. |
$x_continuation_token = 'x_continuation_token_example'; // string | Token służący do pobrania kolejnej strony wyników.

try {
    $result = $apiInstance->apiV2SessionsGet($session_type, $page_size, $reference_number, $date_created_from, $date_created_to, $date_closed_from, $date_closed_to, $date_modified_from, $date_modified_to, $statuses, $x_continuation_token);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StatusWysykiIUPOApi->apiV2SessionsGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **session_type** | **\OpenAPIClientModelSessionType**| Typ sesji.  | Wartość | Opis |  | --- | --- |  | Online | Wysyłka interaktywna (pojedyncze faktury). |  | Batch | Wysyłka wsadowa (paczka faktur). | | |
| **page_size** | **int**| Rozmiar strony. | [optional] |
| **reference_number** | **string**| Numer referencyjny sesji. | [optional] |
| **date_created_from** | **\DateTime**| Data utworzenia sesji (od). | [optional] |
| **date_created_to** | **\DateTime**| Data utworzenia sesji (do). | [optional] |
| **date_closed_from** | **\DateTime**| Data zamknięcia sesji (od). | [optional] |
| **date_closed_to** | **\DateTime**| Data zamknięcia sesji (do). | [optional] |
| **date_modified_from** | **\DateTime**| Data ostatniej aktywności (wysyłka faktury lub zmiana statusu) w ramach sesji (od). | [optional] |
| **date_modified_to** | **\DateTime**| Data ostatniej aktywności (wysyłka faktury lub zmiana statusu) w ramach sesji (do). | [optional] |
| **statuses** | [**\OpenAPI\Client\Model\CommonSessionStatus[]**](../Model/\OpenAPI\Client\Model\CommonSessionStatus.md)| Statusy sesji.  | Wartość | Opis |  | --- | --- |  | Succeeded | Sesja przetworzona poprawnie.            W trakcie przetwarzania sesji nie wystąpiły żadne błędy, ale część faktur nadal mogła zostać odrzucona. |  | InProgress | Sesja aktywna. |  | Failed | Sesja nie przetworzona z powodu błędów.            Na etapie rozpoczynania lub kończenia sesji wystąpiły błędy, które nie pozwoliły na jej poprawne przetworzenie. | | [optional] |
| **x_continuation_token** | **string**| Token służący do pobrania kolejnej strony wyników. | [optional] |

### Return type

[**\OpenAPI\Client\Model\SessionsQueryResponse**](../Model/SessionsQueryResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `apiV2SessionsReferenceNumberGet()`

```php
apiV2SessionsReferenceNumberGet($reference_number): \OpenAPI\Client\Model\SessionStatusResponse
```

Pobranie statusu sesji

Sprawdza bieżący status sesji o podanym numerze referencyjnym.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\StatusWysykiIUPOApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$reference_number = 'reference_number_example'; // string | Numer referencyjny sesji.

try {
    $result = $apiInstance->apiV2SessionsReferenceNumberGet($reference_number);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StatusWysykiIUPOApi->apiV2SessionsReferenceNumberGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **reference_number** | **string**| Numer referencyjny sesji. | |

### Return type

[**\OpenAPI\Client\Model\SessionStatusResponse**](../Model/SessionStatusResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `apiV2SessionsReferenceNumberInvoicesFailedGet()`

```php
apiV2SessionsReferenceNumberInvoicesFailedGet($reference_number, $x_continuation_token, $page_size): \OpenAPI\Client\Model\SessionInvoicesResponse
```

Pobranie niepoprawnie przetworzonych faktur sesji

Zwraca listę niepoprawnie przetworzonych faktur przesłanych w sesji wraz z ich statusami.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\StatusWysykiIUPOApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$reference_number = 'reference_number_example'; // string | Numer referencyjny sesji.
$x_continuation_token = 'x_continuation_token_example'; // string | Token służący do pobrania kolejnej strony wyników.
$page_size = 10; // int | Rozmiar strony wyników.

try {
    $result = $apiInstance->apiV2SessionsReferenceNumberInvoicesFailedGet($reference_number, $x_continuation_token, $page_size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StatusWysykiIUPOApi->apiV2SessionsReferenceNumberInvoicesFailedGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **reference_number** | **string**| Numer referencyjny sesji. | |
| **x_continuation_token** | **string**| Token służący do pobrania kolejnej strony wyników. | [optional] |
| **page_size** | **int**| Rozmiar strony wyników. | [optional] [default to 10] |

### Return type

[**\OpenAPI\Client\Model\SessionInvoicesResponse**](../Model/SessionInvoicesResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `apiV2SessionsReferenceNumberInvoicesGet()`

```php
apiV2SessionsReferenceNumberInvoicesGet($reference_number, $page_offset, $page_size): \OpenAPI\Client\Model\SessionInvoicesResponse
```

Pobranie faktur sesji

Zwraca listę faktur przesłanych w sesji wraz z ich statusami, oraz informacje na temat ilości poprawnie i niepoprawnie przetworzonych faktur.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\StatusWysykiIUPOApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$reference_number = 'reference_number_example'; // string | Numer referencyjny sesji.
$page_offset = 0; // int | Numer strony wyników.
$page_size = 10; // int | Rozmiar strony wyników.

try {
    $result = $apiInstance->apiV2SessionsReferenceNumberInvoicesGet($reference_number, $page_offset, $page_size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StatusWysykiIUPOApi->apiV2SessionsReferenceNumberInvoicesGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **reference_number** | **string**| Numer referencyjny sesji. | |
| **page_offset** | **int**| Numer strony wyników. | [optional] [default to 0] |
| **page_size** | **int**| Rozmiar strony wyników. | [optional] [default to 10] |

### Return type

[**\OpenAPI\Client\Model\SessionInvoicesResponse**](../Model/SessionInvoicesResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `apiV2SessionsReferenceNumberInvoicesInvoiceReferenceNumberGet()`

```php
apiV2SessionsReferenceNumberInvoicesInvoiceReferenceNumberGet($reference_number, $invoice_reference_number): \OpenAPI\Client\Model\InvoiceStatusResponse
```

Pobranie statusu faktury z sesji

Zwraca fakturę przesłaną w sesji wraz ze statusem.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\StatusWysykiIUPOApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$reference_number = 'reference_number_example'; // string | Numer referencyjny sesji.
$invoice_reference_number = 'invoice_reference_number_example'; // string | Numer referencyjny faktury.

try {
    $result = $apiInstance->apiV2SessionsReferenceNumberInvoicesInvoiceReferenceNumberGet($reference_number, $invoice_reference_number);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StatusWysykiIUPOApi->apiV2SessionsReferenceNumberInvoicesInvoiceReferenceNumberGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **reference_number** | **string**| Numer referencyjny sesji. | |
| **invoice_reference_number** | **string**| Numer referencyjny faktury. | |

### Return type

[**\OpenAPI\Client\Model\InvoiceStatusResponse**](../Model/InvoiceStatusResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `apiV2SessionsReferenceNumberInvoicesInvoiceReferenceNumberUpoGet()`

```php
apiV2SessionsReferenceNumberInvoicesInvoiceReferenceNumberUpoGet($reference_number, $invoice_reference_number): string
```

Pobranie UPO faktury z sesji na podstawie numeru referencyjnego faktury

Zwraca UPO faktury przesłanego w sesji na podstawie jego numeru KSeF.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\StatusWysykiIUPOApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$reference_number = 'reference_number_example'; // string | Numer referencyjny sesji.
$invoice_reference_number = 'invoice_reference_number_example'; // string | Numer referencyjny faktury.

try {
    $result = $apiInstance->apiV2SessionsReferenceNumberInvoicesInvoiceReferenceNumberUpoGet($reference_number, $invoice_reference_number);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StatusWysykiIUPOApi->apiV2SessionsReferenceNumberInvoicesInvoiceReferenceNumberUpoGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **reference_number** | **string**| Numer referencyjny sesji. | |
| **invoice_reference_number** | **string**| Numer referencyjny faktury. | |

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

## `apiV2SessionsReferenceNumberInvoicesKsefKsefNumberUpoGet()`

```php
apiV2SessionsReferenceNumberInvoicesKsefKsefNumberUpoGet($reference_number, $ksef_number): string
```

Pobranie UPO faktury z sesji na podstawie numeru KSeF

Zwraca UPO faktury przesłanego w sesji na podstawie jego numeru KSeF.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\StatusWysykiIUPOApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$reference_number = 'reference_number_example'; // string | Numer referencyjny sesji.
$ksef_number = 'ksef_number_example'; // string | Numer KSeF faktury.

try {
    $result = $apiInstance->apiV2SessionsReferenceNumberInvoicesKsefKsefNumberUpoGet($reference_number, $ksef_number);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StatusWysykiIUPOApi->apiV2SessionsReferenceNumberInvoicesKsefKsefNumberUpoGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **reference_number** | **string**| Numer referencyjny sesji. | |
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

## `apiV2SessionsReferenceNumberUpoUpoReferenceNumberGet()`

```php
apiV2SessionsReferenceNumberUpoUpoReferenceNumberGet($reference_number, $upo_reference_number): string
```

Pobranie UPO dla sesji

Zwraca XML zawierający zbiorcze UPO dla sesji.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\StatusWysykiIUPOApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$reference_number = 'reference_number_example'; // string | Numer referencyjny sesji.
$upo_reference_number = 'upo_reference_number_example'; // string | Numer referencyjny UPO.

try {
    $result = $apiInstance->apiV2SessionsReferenceNumberUpoUpoReferenceNumberGet($reference_number, $upo_reference_number);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StatusWysykiIUPOApi->apiV2SessionsReferenceNumberUpoUpoReferenceNumberGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **reference_number** | **string**| Numer referencyjny sesji. | |
| **upo_reference_number** | **string**| Numer referencyjny UPO. | |

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
