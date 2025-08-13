# # SessionInvoice

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ordinal_number** | **int** | Numer sekwencyjny faktury w ramach sesji. |
**invoice_number** | **string** | Numer faktury. | [optional]
**ksef_number** | **string** | Numer KSeF. | [optional]
**reference_number** | **string** | Numer referencyjny faktury. | [optional]
**invoice_hash** | **string** | Skrót SHA256 faktury, zakodowany w formacie Base64. | [optional]
**invoice_file_name** | **string** | Nazwa pliku faktury (zwracana dla faktur wysyłanych wsadowo). | [optional]
**receive_date** | **\DateTime** | Data przyjęcia faktury. |
**status** | [**\NetSeven\KseF2Model\StatusInfo**](StatusInfo.md) | Status faktury.    | Code | Description | Details |  | --- | --- | --- |  | 100 | Dokument faktury przyjęty | - |  | 200 | Sukces | - |  | 300 | Trwa przetwarzanie | - |  | 410 | Nieprawidłowy zakres uprawnień | - |  | 430 | Błąd weryfikacji pliku faktury | - |  | 435 | Błąd odszyfrowania pliku | - |  | 440 | Duplikat faktury | - |  | 450 | Błąd weryfikacji semantyki dokumentu faktury | - |  | 500 | Nieznany błąd ({statusCode}) | - | |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
