# # AuthenticationOperationStatusResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**reference_number** | **string** | Numer referencyjny operacji uwierzytelnienia. |
**is_current** | **bool** | Czy sesja jest powiązana z aktualnie używanym tokenem. | [optional] [readonly]
**start_date** | **\DateTime** | Data rozpoczęcia operacji uwierzytelnienia. |
**authentication_method** | [**\NetSeven\KseF2Model\AuthenticationMethod**](AuthenticationMethod.md) | Użyta metoda uwierzytelnienia.  | Wartość | Opis |  | --- | --- |  | Token | Token KSeF. |  | TrustedProfile | Profil Zaufany. |  | InternalCertificate | Certyfikat KSeF. |  | QualifiedSignature | Podpis kwalifikowany. |  | QualifiedSeal | Pieczęć kwalifikowana. |  | PersonalSignature | Podpis osobisty. | |
**status** | [**\NetSeven\KseF2Model\StatusInfo**](StatusInfo.md) | Informacje o aktualnym statusie.  | Code | Description | Details |  | --- | --- | --- |  | 100 | Uwierzytelnianie w toku | - |  | 200 | Uwierzytelnianie zakończone sukcesem | - |  | 400 | Uwierzytelnianie zakończone niepowodzeniem | Nieważny certyfikat |  | 400 | Uwierzytelnianie zakończone niepowodzeniem | Błąd weryfikacji łańcucha certyfikatów |  | 400 | Uwierzytelnianie zakończone niepowodzeniem | Niezaufany łańcuch certyfikatów |  | 400 | Uwierzytelnianie zakończone niepowodzeniem | Certyfikat odwołany |  | 400 | Uwierzytelnianie zakończone niepowodzeniem | Niepoprawny certyfikat |  | 401 | Uwierzytelnienie unieważnione | Uwierzytelnienie i powiązane refresh tokeny zostały unieważnione przez użytkownika |  | 500 | Nieznany błąd | - | |
**is_token_redeemed** | **bool** | Czy został już wydany refresh token powiązany z danym uwierzytelnieniem. | [optional]
**last_token_refresh_date** | **\DateTime** | Data ostatniego odświeżenia tokena. | [optional]
**refresh_token_valid_until** | **\DateTime** | Termin ważności refresh tokena (o ile nie zostanie wcześniej unieważniony). | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
