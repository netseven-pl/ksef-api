# # AsyncInvoicesQueryStatus

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**operation_reference_number** | **string** | Unikalny identyfikator operacji, nadany podczas inicjalizacji zapytania. |
**status** | [**\NetSeven\KseF2Model\StatusInfo**](StatusInfo.md) | Informacje o aktualnym statusie przetwarzania zapytania. |
**package_parts** | [**\NetSeven\KseF2Model\InvoicePackagePart[]**](InvoicePackagePart.md) | Lista plików dostępnych do pobrania.  Wypełniana tylko, gdy wynik zapytania jest gotowy. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
