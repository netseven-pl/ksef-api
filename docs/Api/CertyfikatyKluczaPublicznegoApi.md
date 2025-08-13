# NetSeven\CertyfikatyKluczaPublicznegoApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**apiV2SecurityPublicKeyCertificatesGet()**](CertyfikatyKluczaPublicznegoApi.md#apiV2SecurityPublicKeyCertificatesGet) | **GET** /api/v2/security/public-key-certificates | Pobranie certyfikatów |


## `apiV2SecurityPublicKeyCertificatesGet()`

```php
apiV2SecurityPublicKeyCertificatesGet(): \NetSeven\KseF2Model\PublicKeyCertificate[]
```

Pobranie certyfikatów

Zwraca informacje o kluczach publicznych używanych do szyfrowania danych przesyłanych do systemu KSeF.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new NetSeven\Api\CertyfikatyKluczaPublicznegoApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->apiV2SecurityPublicKeyCertificatesGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CertyfikatyKluczaPublicznegoApi->apiV2SecurityPublicKeyCertificatesGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\NetSeven\KseF2Model\PublicKeyCertificate[]**](../Model/PublicKeyCertificate.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
