# # CertificateListItem

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**certificate_serial_number** | **string** | Numer seryjny certyfikatu (w formacie szesnastkowym). |
**name** | **string** | Nazwa własna certyfikatu. |
**common_name** | **string** | Nazwa powszechna (CN) podmiotu, dla którego wystawiono certyfikat. |
**status** | [**\OpenAPI\Client\Model\CertificateListItemStatus**](CertificateListItemStatus.md) | Status certyfikatu.  | Wartość | Opis |  | --- | --- |  | Active | Certyfikat jest aktywny i może zostać użyty do uwierzytelnienia. |  | Blocked | Certyfikat został zablokowany i nie może zostać użyty do uwierzytelnienia.            Status przejściowy do czasu zakończenia procesu unieważniania. |  | Revoked | Certyfikat został unieważniony i nie może zostać użyty do uwierzytelnienia. |  | Expired | Certyfikat wygasł i nie może zostać użyty do uwierzytelnienia. | |
**subject_identifier** | **string** | Identyfikator podmiotu, dla którego wystawiono certyfikat. |
**subject_identifier_type** | **string** | Typ identyfikatora podmiotu, dla którego wystawiono certyfikat. |
**valid_from** | **\DateTime** | Data rozpoczęcia ważności certyfikatu. |
**valid_to** | **\DateTime** | Data wygaśnięcia certyfikatu. |
**last_use_date** | **\DateTime** | Data ostatniego użycia certyfikatu. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
