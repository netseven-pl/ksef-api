# # QueryCertificatesRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**certificate_serial_number** | **string** | Numer seryjny certyfikatu. Wyszukiwanie odbywa się na zasadzie dokładnego dopasowania (exact match). | [optional]
**name** | **string** | Nazwa własna certyfikatu. Wyszukiwanie jest częściowe, czyli zwracane są certyfikaty, których nazwa zawiera podany ciąg znaków (contains). | [optional]
**status** | [**\OpenAPI\Client\Model\CertificateListItemStatus**](CertificateListItemStatus.md) | Status certyfikatu.  | Wartość | Opis |  | --- | --- |  | Active | Certyfikat jest aktywny i może zostać użyty do uwierzytelnienia. |  | Blocked | Certyfikat został zablokowany i nie może zostać użyty do uwierzytelnienia.            Status przejściowy do czasu zakończenia procesu unieważniania. |  | Revoked | Certyfikat został unieważniony i nie może zostać użyty do uwierzytelnienia. |  | Expired | Certyfikat wygasł i nie może zostać użyty do uwierzytelnienia. | | [optional]
**expires_after** | **\DateTime** | Filtruje certyfikaty, które wygasają po podanej dacie. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
