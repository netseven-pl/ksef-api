# # InvoicesAsyncQueryRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**encryption** | [**\NetSeven\KseF2Model\EncryptionInfo**](EncryptionInfo.md) | Informacje wymagane do zaszyfrowania wyniku zapytania. |
**subject_type** | [**\NetSeven\KseF2Model\InvoiceQuerySubjectType**](InvoiceQuerySubjectType.md) | Typ podmiotu, którego dotyczą kryteria filtrowania metadanych faktur.  Określa kontekst, w jakim przeszukiwane są dane. |
**date_range** | [**\NetSeven\KseF2Model\InvoiceQueryDateRange**](InvoiceQueryDateRange.md) | Typ i zakres dat, według którego mają być filtrowane faktury. |
**ksef_number** | **string** | Numer KSeF faktury. | [optional]
**invoice_number** | **string** | Numer faktury nadany przez wystawcę. | [optional]
**amount** | [**\NetSeven\KseF2Model\InvoiceQueryAmount**](InvoiceQueryAmount.md) | Filtr kwotowy – brutto, netto lub VAT (z wartością). | [optional]
**seller** | [**\NetSeven\KseF2Model\InvoiceQuerySeller**](InvoiceQuerySeller.md) | Dane sprzedawcy. | [optional]
**buyer** | [**\NetSeven\KseF2Model\InvoiceQueryBuyer**](InvoiceQueryBuyer.md) | Dane nabywcy. | [optional]
**currency_codes** | [**\NetSeven\KseF2Model\CurrencyCode[]**](CurrencyCode.md) | Kody walut. | [optional]
**is_hidden** | **bool** | Czy faktura została oznaczona jako ukryta. | [optional]
**invoicing_mode** | [**\NetSeven\KseF2Model\InvoicingMode**](InvoicingMode.md) | Tryb wystawienia faktury: online lub offline. | [optional]
**is_self_invoicing** | **bool** | Czy faktura została wystawiona w trybie samofakturowania. | [optional]
**invoice_schema** | [**\NetSeven\KseF2Model\InvoiceMetadataSchema**](InvoiceMetadataSchema.md) | Typ schematu dokumentu. | [optional]
**invoice_types** | [**\NetSeven\KseF2Model\InvoiceMetadataInvoiceType[]**](InvoiceMetadataInvoiceType.md) | Rodzaje faktur. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
