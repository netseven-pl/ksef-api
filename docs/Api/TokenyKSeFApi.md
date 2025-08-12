# OpenAPI\Client\TokenyKSeFApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**apiV2TokensGet()**](TokenyKSeFApi.md#apiV2TokensGet) | **GET** /api/v2/tokens | Pobranie listy wygenerowanych tokenów |
| [**apiV2TokensPost()**](TokenyKSeFApi.md#apiV2TokensPost) | **POST** /api/v2/tokens | Wygenerowanie nowego tokena |
| [**apiV2TokensReferenceNumberDelete()**](TokenyKSeFApi.md#apiV2TokensReferenceNumberDelete) | **DELETE** /api/v2/tokens/{referenceNumber} | Unieważnienie tokena |
| [**apiV2TokensReferenceNumberGet()**](TokenyKSeFApi.md#apiV2TokensReferenceNumberGet) | **GET** /api/v2/tokens/{referenceNumber} | Pobranie statusu tokena |


## `apiV2TokensGet()`

```php
apiV2TokensGet($status, $x_continuation_token, $page_size): \OpenAPI\Client\Model\QueryTokensResponse
```

Pobranie listy wygenerowanych tokenów

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\TokenyKSeFApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$status = array(new \OpenAPI\Client\Model\\OpenAPI\Client\Model\AuthenticationTokenStatus()); // \OpenAPI\Client\Model\AuthenticationTokenStatus[] | Status tokenów do zwrócenia. W przypadku braku parametru zwracane są wszystkie tokeny. Parametr można przekazać wielokrotnie.  | Wartość | Opis |  | --- | --- |  | Pending | Token został utworzony ale jest jeszcze w trakcie aktywacji i nadawania uprawnień. Nie może być jeszcze wykorzystywany do uwierzytelniania. |  | Active | Token jest aktywny i może być wykorzystywany do uwierzytelniania. |  | Revoking | Token jest w trakcie unieważniania. Nie może już być wykorzystywany do uwierzytelniania. |  | Revoked | Token został unieważniony i nie może być wykorzystywany do uwierzytelniania. |  | Failed | Nie udało się aktywować tokena. Należy wygenerować nowy token, obecny nie może być wykorzystywany do uwierzytelniania. |
$x_continuation_token = 'x_continuation_token_example'; // string | Token służący do pobrania kolejnej strony wyników.
$page_size = 10; // int | Rozmiar strony wyników.

try {
    $result = $apiInstance->apiV2TokensGet($status, $x_continuation_token, $page_size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TokenyKSeFApi->apiV2TokensGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **status** | [**\OpenAPI\Client\Model\AuthenticationTokenStatus[]**](../Model/\OpenAPI\Client\Model\AuthenticationTokenStatus.md)| Status tokenów do zwrócenia. W przypadku braku parametru zwracane są wszystkie tokeny. Parametr można przekazać wielokrotnie.  | Wartość | Opis |  | --- | --- |  | Pending | Token został utworzony ale jest jeszcze w trakcie aktywacji i nadawania uprawnień. Nie może być jeszcze wykorzystywany do uwierzytelniania. |  | Active | Token jest aktywny i może być wykorzystywany do uwierzytelniania. |  | Revoking | Token jest w trakcie unieważniania. Nie może już być wykorzystywany do uwierzytelniania. |  | Revoked | Token został unieważniony i nie może być wykorzystywany do uwierzytelniania. |  | Failed | Nie udało się aktywować tokena. Należy wygenerować nowy token, obecny nie może być wykorzystywany do uwierzytelniania. | | [optional] |
| **x_continuation_token** | **string**| Token służący do pobrania kolejnej strony wyników. | [optional] |
| **page_size** | **int**| Rozmiar strony wyników. | [optional] [default to 10] |

### Return type

[**\OpenAPI\Client\Model\QueryTokensResponse**](../Model/QueryTokensResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `apiV2TokensPost()`

```php
apiV2TokensPost($generate_token_request): \OpenAPI\Client\Model\GenerateTokenResponse
```

Wygenerowanie nowego tokena

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\TokenyKSeFApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$generate_token_request = new \OpenAPI\Client\Model\GenerateTokenRequest(); // \OpenAPI\Client\Model\GenerateTokenRequest

try {
    $result = $apiInstance->apiV2TokensPost($generate_token_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TokenyKSeFApi->apiV2TokensPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **generate_token_request** | [**\OpenAPI\Client\Model\GenerateTokenRequest**](../Model/GenerateTokenRequest.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\GenerateTokenResponse**](../Model/GenerateTokenResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `apiV2TokensReferenceNumberDelete()`

```php
apiV2TokensReferenceNumberDelete($reference_number)
```

Unieważnienie tokena

Unieważniony token nie pozwoli już na uwierzytelnienie się za jego pomocą. Unieważnienie nie może zostać cofnięte.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\TokenyKSeFApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$reference_number = 'reference_number_example'; // string | Numer referencyjny tokena do unieważeniania.

try {
    $apiInstance->apiV2TokensReferenceNumberDelete($reference_number);
} catch (Exception $e) {
    echo 'Exception when calling TokenyKSeFApi->apiV2TokensReferenceNumberDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **reference_number** | **string**| Numer referencyjny tokena do unieważeniania. | |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `apiV2TokensReferenceNumberGet()`

```php
apiV2TokensReferenceNumberGet($reference_number): \OpenAPI\Client\Model\AuthenticationToken
```

Pobranie statusu tokena

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\TokenyKSeFApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$reference_number = 'reference_number_example'; // string | Numer referencyjny tokena.

try {
    $result = $apiInstance->apiV2TokensReferenceNumberGet($reference_number);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TokenyKSeFApi->apiV2TokensReferenceNumberGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **reference_number** | **string**| Numer referencyjny tokena. | |

### Return type

[**\OpenAPI\Client\Model\AuthenticationToken**](../Model/AuthenticationToken.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
