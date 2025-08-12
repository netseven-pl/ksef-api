# OpenAPI\Client\CertyfikatyApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**apiV2CertificatesCertificateSerialNumberRevokePost()**](CertyfikatyApi.md#apiV2CertificatesCertificateSerialNumberRevokePost) | **POST** /api/v2/certificates/{certificateSerialNumber}/revoke | Unieważnienie certyfikatu |
| [**apiV2CertificatesEnrollmentsDataGet()**](CertyfikatyApi.md#apiV2CertificatesEnrollmentsDataGet) | **GET** /api/v2/certificates/enrollments/data | Pobranie danych do wniosku certyfikacyjnego |
| [**apiV2CertificatesEnrollmentsPost()**](CertyfikatyApi.md#apiV2CertificatesEnrollmentsPost) | **POST** /api/v2/certificates/enrollments | Wysyłka wniosku certyfikacyjnego |
| [**apiV2CertificatesEnrollmentsReferenceNumberGet()**](CertyfikatyApi.md#apiV2CertificatesEnrollmentsReferenceNumberGet) | **GET** /api/v2/certificates/enrollments/{referenceNumber} | Pobranie statusu przetwarzania wniosku certyfikacyjnego |
| [**apiV2CertificatesLimitsGet()**](CertyfikatyApi.md#apiV2CertificatesLimitsGet) | **GET** /api/v2/certificates/limits | Pobranie danych o limitach certyfikatów |
| [**apiV2CertificatesQueryPost()**](CertyfikatyApi.md#apiV2CertificatesQueryPost) | **POST** /api/v2/certificates/query | Pobranie listy metadanych certyfikatów |
| [**apiV2CertificatesRetrievePost()**](CertyfikatyApi.md#apiV2CertificatesRetrievePost) | **POST** /api/v2/certificates/retrieve | Pobranie certyfikatu lub listy certyfikatów |


## `apiV2CertificatesCertificateSerialNumberRevokePost()`

```php
apiV2CertificatesCertificateSerialNumberRevokePost($certificate_serial_number, $revoke_certificate_request)
```

Unieważnienie certyfikatu

Unieważnia certyfikat o podanym numerze seryjnym.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\CertyfikatyApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$certificate_serial_number = 'certificate_serial_number_example'; // string | Numer seryjny certyfikatu (w formacie szesnastkowym).
$revoke_certificate_request = new \OpenAPI\Client\Model\RevokeCertificateRequest(); // \OpenAPI\Client\Model\RevokeCertificateRequest | 

try {
    $apiInstance->apiV2CertificatesCertificateSerialNumberRevokePost($certificate_serial_number, $revoke_certificate_request);
} catch (Exception $e) {
    echo 'Exception when calling CertyfikatyApi->apiV2CertificatesCertificateSerialNumberRevokePost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **certificate_serial_number** | **string**| Numer seryjny certyfikatu (w formacie szesnastkowym). | |
| **revoke_certificate_request** | [**\OpenAPI\Client\Model\RevokeCertificateRequest**](../Model/RevokeCertificateRequest.md)|  | [optional] |

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

## `apiV2CertificatesEnrollmentsDataGet()`

```php
apiV2CertificatesEnrollmentsDataGet(): \OpenAPI\Client\Model\CertificateEnrollmentDataResponse
```

Pobranie danych do wniosku certyfikacyjnego

Zwraca dane wymagane do przygotowania wniosku certyfikacyjnego PKCS#10.    Dane te są zwracane na podstawie certyfikatu użytego w procesie uwierzytelnienia i identyfikują podmiot, który składa wniosek o certyfikat.      > Więcej informacji:  > - [Pobranie danych do wniosku certyfikacyjnego](https://github.com/CIRFMF/ksef-client-docs/blob/main/certyfikaty-wewn%C4%99trzne-KSeF.md#2-pobranie-danych-do-wniosku-certyfikacyjnego)  > - [Przygotowanie wniosku](https://github.com/CIRFMF/ksef-client-docs/blob/main/certyfikaty-wewn%C4%99trzne-KSeF.md#3-przygotowanie-csr-certificate-signing-request)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\CertyfikatyApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->apiV2CertificatesEnrollmentsDataGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CertyfikatyApi->apiV2CertificatesEnrollmentsDataGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Client\Model\CertificateEnrollmentDataResponse**](../Model/CertificateEnrollmentDataResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `apiV2CertificatesEnrollmentsPost()`

```php
apiV2CertificatesEnrollmentsPost($enroll_certificate_request): \OpenAPI\Client\Model\EnrollCertificateResponse
```

Wysyłka wniosku certyfikacyjnego

Przyjmuje wniosek certyfikacyjny i rozpoczyna jego przetwarzanie.    > Więcej informacji:  > - [Wysłanie wniosku certyfikacyjnego](https://github.com/CIRFMF/ksef-client-docs/blob/main/certyfikaty-wewn%C4%99trzne-KSeF.md#4-wys%C5%82anie-wniosku-certyfikacyjnego)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\CertyfikatyApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$enroll_certificate_request = new \OpenAPI\Client\Model\EnrollCertificateRequest(); // \OpenAPI\Client\Model\EnrollCertificateRequest | 

try {
    $result = $apiInstance->apiV2CertificatesEnrollmentsPost($enroll_certificate_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CertyfikatyApi->apiV2CertificatesEnrollmentsPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **enroll_certificate_request** | [**\OpenAPI\Client\Model\EnrollCertificateRequest**](../Model/EnrollCertificateRequest.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\EnrollCertificateResponse**](../Model/EnrollCertificateResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `apiV2CertificatesEnrollmentsReferenceNumberGet()`

```php
apiV2CertificatesEnrollmentsReferenceNumberGet($reference_number): \OpenAPI\Client\Model\CertificateEnrollmentStatusResponse
```

Pobranie statusu przetwarzania wniosku certyfikacyjnego

Zwraca informacje o statusie wniosku certyfikacyjnego.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\CertyfikatyApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$reference_number = 'reference_number_example'; // string | Numer referencyjny wniosku certyfikacyjnego

try {
    $result = $apiInstance->apiV2CertificatesEnrollmentsReferenceNumberGet($reference_number);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CertyfikatyApi->apiV2CertificatesEnrollmentsReferenceNumberGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **reference_number** | **string**| Numer referencyjny wniosku certyfikacyjnego | |

### Return type

[**\OpenAPI\Client\Model\CertificateEnrollmentStatusResponse**](../Model/CertificateEnrollmentStatusResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `apiV2CertificatesLimitsGet()`

```php
apiV2CertificatesLimitsGet(): \OpenAPI\Client\Model\CertificateLimitsResponse
```

Pobranie danych o limitach certyfikatów

Zwraca informacje o limitach certyfikatów oraz informacje czy użytkownik może zawnioskować o certyfikat KSeF.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\CertyfikatyApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->apiV2CertificatesLimitsGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CertyfikatyApi->apiV2CertificatesLimitsGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Client\Model\CertificateLimitsResponse**](../Model/CertificateLimitsResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `apiV2CertificatesQueryPost()`

```php
apiV2CertificatesQueryPost($page_size, $page_offset, $query_certificates_request): \OpenAPI\Client\Model\QueryCertificatesResponse
```

Pobranie listy metadanych certyfikatów

Zwraca listę certyfikatów spełniających podane kryteria wyszukiwania.  W przypadku braku podania kryteriów wyszukiwania zwrócona zostanie nieprzefiltrowana lista.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\CertyfikatyApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$page_size = 10; // int | Rozmiar strony wyników
$page_offset = 0; // int | Numer strony wyników
$query_certificates_request = new \OpenAPI\Client\Model\QueryCertificatesRequest(); // \OpenAPI\Client\Model\QueryCertificatesRequest | Kryteria filtrowania

try {
    $result = $apiInstance->apiV2CertificatesQueryPost($page_size, $page_offset, $query_certificates_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CertyfikatyApi->apiV2CertificatesQueryPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page_size** | **int**| Rozmiar strony wyników | [optional] [default to 10] |
| **page_offset** | **int**| Numer strony wyników | [optional] [default to 0] |
| **query_certificates_request** | [**\OpenAPI\Client\Model\QueryCertificatesRequest**](../Model/QueryCertificatesRequest.md)| Kryteria filtrowania | [optional] |

### Return type

[**\OpenAPI\Client\Model\QueryCertificatesResponse**](../Model/QueryCertificatesResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `apiV2CertificatesRetrievePost()`

```php
apiV2CertificatesRetrievePost($retrieve_certificates_request): \OpenAPI\Client\Model\RetrieveCertificatesResponse
```

Pobranie certyfikatu lub listy certyfikatów

Zwraca certyfikaty o podanych numerach seryjnych w formacie DER zakodowanym w Base64.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\CertyfikatyApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$retrieve_certificates_request = new \OpenAPI\Client\Model\RetrieveCertificatesRequest(); // \OpenAPI\Client\Model\RetrieveCertificatesRequest | 

try {
    $result = $apiInstance->apiV2CertificatesRetrievePost($retrieve_certificates_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CertyfikatyApi->apiV2CertificatesRetrievePost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **retrieve_certificates_request** | [**\OpenAPI\Client\Model\RetrieveCertificatesRequest**](../Model/RetrieveCertificatesRequest.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\RetrieveCertificatesResponse**](../Model/RetrieveCertificatesResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
