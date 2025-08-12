# # InvoiceStatusResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**reference_number** | **string** |  | [optional]
**ordinal_number** | **int** |  | [optional]
**ksef_number** | **string** |  | [optional]
**invoice_number** | **string** |  | [optional]
**invoice_file_name** | **string** |  | [optional]
**receive_date** | **\DateTime** |  | [optional]
**status** | [**\OpenAPI\Client\Model\StatusInfo**](StatusInfo.md) | Status faktury.    | Code | Description | Details |  | --- | --- | --- |  | 100 | Dokument faktury przyjęty | - |  | 200 | Sukces | - |  | 300 | Trwa przetwarzanie | - |  | 410 | Nieprawidłowy zakres uprawnień | - |  | 430 | Błąd weryfikacji pliku faktury | - |  | 435 | Błąd odszyfrowania pliku | - |  | 440 | Duplikat faktury | - |  | 450 | Błąd weryfikacji semantyki dokumentu faktury | - |  | 500 | Nieznany błąd ({statusCode}) | - | | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
