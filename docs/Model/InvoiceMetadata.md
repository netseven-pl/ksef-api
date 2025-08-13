# # InvoiceMetadata

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ksef_number** | **string** | Numer KSeF faktury. |
**invoice_number** | **string** | Numer faktury nadany przez wystawcę. |
**invoice_date** | **\DateTime** | Data wystawienia faktury. |
**acquisition_date** | **\DateTime** | Data przyjęcia faktury do systemu KSeF. |
**seller** | [**\NetSeven\KseF2Model\InvoiceMetadataSeller**](InvoiceMetadataSeller.md) | Dane identyfikujące sprzedawcę. |
**buyer** | [**\NetSeven\KseF2Model\InvoiceMetadataBuyer**](InvoiceMetadataBuyer.md) | Dane identyfikujące nabywcę. |
**net_amount** | **float** | Łączna kwota netto. |
**gross_amount** | **float** | Łączna kwota brutto. |
**vat_amount** | **float** | Łączna kwota VAT. |
**currency** | [**\NetSeven\KseF2Model\CurrencyCode**](CurrencyCode.md) | Kod waluty. |
**invoicing_mode** | [**\NetSeven\KseF2Model\InvoicingMode**](InvoicingMode.md) | Tryb fakturowania (online/offline). |
**invoice_type** | [**\NetSeven\KseF2Model\InvoiceMetadataInvoiceType**](InvoiceMetadataInvoiceType.md) | Rodzaj faktury. |
**form_code** | [**\NetSeven\KseF2Model\FormCode**](FormCode.md) | Struktura dokumentu faktury.    Obsługiwane schematy:  | SystemCode | SchemaVersion | Value |  | --- | --- | --- |  | FA (2) | 1-0E | FA |  | FA (3) | 1-0E | FA | |
**is_hidden** | **bool** | Czy faktura została oznaczona jako ukryta. |
**is_self_invoicing** | **bool** | Czy faktura została wystawiona w trybie samofakturowania. |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
