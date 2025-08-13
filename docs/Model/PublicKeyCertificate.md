# # PublicKeyCertificate

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**certificate_pem** | **string** | Certyfikat klucza publicznego w formacie PEM. | [optional]
**valid_from** | **\DateTime** | Data początku obowiązywania certyfikatu. |
**valid_to** | **\DateTime** | Data końca obowiązywania certyfikatu. | [optional]
**usage** | [**\NetSeven\KseF2Model\PublicKeyCertificateUsage[]**](PublicKeyCertificateUsage.md) | Operacje do których może być używany certyfikat.  | Wartość | Opis |  | --- | --- |  | KsefTokenEncryption | Szyfrowanie tokenów KSeF przesyłanych w trakcie procesu uwierzytelniania. |  | SymmetricKeyEncryption | Szyfrowanie klucza symetrycznego wykorzystywanego do szyfrowania przesyłanych faktur. | |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
