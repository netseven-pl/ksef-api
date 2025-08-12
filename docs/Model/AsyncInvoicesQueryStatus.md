# # AsyncInvoicesQueryStatus

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**operation_reference_number** | **string** | Unikalny identyfikator operacji, nadany podczas inicjalizacji zapytania. |
**status** | [**\OpenAPI\Client\Model\StatusInfo**](StatusInfo.md) | Informacje o aktualnym statusie przetwarzania zapytania. |
**package_parts** | [**\OpenAPI\Client\Model\InvoicePackagePart[]**](InvoicePackagePart.md) | Lista plików dostępnych do pobrania.  Wypełniana tylko, gdy wynik zapytania jest gotowy. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
