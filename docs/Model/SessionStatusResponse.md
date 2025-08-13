# # SessionStatusResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**status** | [**\NetSeven\KseF2Model\StatusInfo**](StatusInfo.md) | Informacje o aktualnym statusie.                Sesja wsadowa:  | Code | Description | Details |  | --- | --- | --- |  | 100 | Sesja wsadowa rozpoczęta | - |  | 200 | Sesja wsadowa przetworzona pomyślnie | - |  | 300 | Trwa przetwarzanie | - |  | 405 | Błąd weryfikacji poprawności dostarczonych elementów paczki | - |  | 415 | Błąd odszyfrowania dostarczonego klucza | - |  | 430 | Błąd dekompresji pierwotnego archiwum | - |  | 435 | Błąd odszyfrowania zaszyfrowanych części archiwum | - |  | 500 | Nieznany błąd ({statusCode}) | - |    Sesja interaktywna:  | Code | Description | Details |  | --- | --- | --- |  | 100 | Sesja interaktywna otwarta | - |  | 200 | Sesja interaktywna przetworzona pomyślnie | - |  | 300 | Sesja interaktywna zamknięta | - |  | 415 | Błąd odszyfrowania dostarczonego klucza | - |  | * | description missing | - | |
**upo** | [**\NetSeven\KseF2Model\UpoResponse**](UpoResponse.md) | Informacja o UPO sesyjnym, zwracana gdy sesja została zamknięta i UPO zostało wygenerowane. | [optional]
**invoice_count** | **int** | Ilość przyjętych faktur w ramach sesji. | [optional]
**successful_invoice_count** | **int** | Ilość faktur przeprocesowanych w ramach sesji z sukcesem . | [optional]
**failed_invoice_count** | **int** | Ilość faktur przeprocesowanych w ramach sesji z błędem. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
