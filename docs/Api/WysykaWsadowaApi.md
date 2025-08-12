# OpenAPI\Client\WysykaWsadowaApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**apiV2SessionsBatchReferenceNumberClosePost()**](WysykaWsadowaApi.md#apiV2SessionsBatchReferenceNumberClosePost) | **POST** /api/v2/sessions/batch/{referenceNumber}/close | Zamknięcie sesji wsadowej |
| [**batchOpen()**](WysykaWsadowaApi.md#batchOpen) | **POST** /api/v2/sessions/batch | Otwarcie sesji wsadowej |


## `apiV2SessionsBatchReferenceNumberClosePost()`

```php
apiV2SessionsBatchReferenceNumberClosePost($reference_number)
```

Zamknięcie sesji wsadowej

Zamyka sesję wsadową, rozpoczyna procesowanie paczki faktur i generowanie UPO dla prawidłowych faktur oraz zbiorczego UPO dla sesji.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\WysykaWsadowaApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$reference_number = 'reference_number_example'; // string | Numer referencyjny sesji

try {
    $apiInstance->apiV2SessionsBatchReferenceNumberClosePost($reference_number);
} catch (Exception $e) {
    echo 'Exception when calling WysykaWsadowaApi->apiV2SessionsBatchReferenceNumberClosePost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **reference_number** | **string**| Numer referencyjny sesji | |

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

## `batchOpen()`

```php
batchOpen($open_batch_session_request): \OpenAPI\Client\Model\OpenBatchSessionResponse
```

Otwarcie sesji wsadowej

Otwiera sesję do wysyłki wsadowej faktur. Należy przekazać schemat wysyłanych faktur, informacje o paczce faktur oraz informacje o kluczu używanym do szyfrowania.    > Więcej informacji:  > - [Przygotwanie paczki faktur](https://github.com/CIRFMF/ksef-docs/blob/main/sesja-wsadowa.md)  > - [Klucz publiczny Ministersta Finansów](/public-keys/publicKey.pem)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\WysykaWsadowaApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$open_batch_session_request = {"formCode":{"systemCode":"FA (2)","schemaVersion":"1-0E","value":"FA"},"batchFile":{"fileSize":16037,"fileHash":"WO86CC+1Lef11wEosItld/NPwxGN8tobOMLqk9PQjgs=","fileParts":[{"ordinalNumber":1,"fileName":"92cca5be-7f37-4d36-98bb-1f5369841038.zip.aes","fileSize":16048,"fileHash":"23ZyDAN0H/+yhC/En2xbNfF0tajAWSfejDaXD7fc2AE="}]},"encryption":{"encryptedSymmetricKey":"bYqmPAglF01AxZim4oNa+1NerhZYfFgLMnvksBprUur1aesQ0Y5jsmOIfCrozfMkF2tjdO+uOsBg4FPlDgjChwN2/tz2Hqwtxq3RkTr1SjY4x8jxJFpPedcS7EI+XO8C+i9mLj7TFx9p/bg07yM9vHtMAk5b88Ay9Qc3+T5Ch1DM2ClR3sVu2DqdlKzmbINY+rhfGtXn58Qo0XRyESGgc6M0iTZVBRPuPXLnD8a1KpOneCpNzLwxgT6Ei3ivLOpPWT53PxkRTaQ8puj6CIiCKo4FHQzHuI/NmrAhYU7TkNm2kymP/OxBgWdg3XB74tqNFfT8RZN1bZXuPhBidDOqa+xsqY3E871FSDmQwZf58HmoNl31XNvpnryiRGfnAISt+m+ELqgksAresVu6E9poUL1yiff+IOHSZABoYpNiqwnbT8qyW1uk8lKLyFVFu+kOsbzBk1OWWHqSkNFDaznDa2MKjHonOXI0uyKaKWvoBFC4dWN1PVumfpSSFAeYgNpAyVrZdcVOuiliEWepTDjGzJoOafTvwr5za2S6B5bPECDpX7JXazV7Olkq7ezG0w8y3olx+0C+NHoCk8B5/cm4gtVHTgKjiLSGpKJVOJABLXFkOyIOjbQsVe4ryX0Qy+SfL7JIQvTWvM5xkCoOMbzLdMo9tNo5qE34sguFI+lIevY=","initializationVector":"jWpJLNBHJ5pQEGCBglmIAw=="},"offlineMode":false}; // \OpenAPI\Client\Model\OpenBatchSessionRequest

try {
    $result = $apiInstance->batchOpen($open_batch_session_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WysykaWsadowaApi->batchOpen: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **open_batch_session_request** | [**\OpenAPI\Client\Model\OpenBatchSessionRequest**](../Model/OpenBatchSessionRequest.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\OpenBatchSessionResponse**](../Model/OpenBatchSessionResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
