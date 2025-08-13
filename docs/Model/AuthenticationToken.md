# # AuthenticationToken

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**reference_number** | **string** | Numer referencyjny tokena. | [optional]
**author_identifier** | [**\NetSeven\KseF2Model\SubjectIdentifier**](SubjectIdentifier.md) | Identyfikator osoby która wygenerowała token. | [optional]
**context_identifier** | [**\NetSeven\KseF2Model\ContextIdentifier**](ContextIdentifier.md) | Identyfikator kontekstu, w którym został wygenerowany token i do którego daje dostęp. | [optional]
**description** | **string** | Opis tokena. | [optional]
**requested_permissions** | [**\NetSeven\KseF2Model\TokenPermissionType[]**](TokenPermissionType.md) | Uprawnienia przypisane tokenowi. | [optional]
**date_created** | **\DateTime** | Data i czas utworzenia tokena. | [optional]
**status** | [**\NetSeven\KseF2Model\AuthenticationTokenStatus**](AuthenticationTokenStatus.md) | Status tokena.  | Wartość | Opis |  | --- | --- |  | Pending | Token został utworzony ale jest jeszcze w trakcie aktywacji i nadawania uprawnień. Nie może być jeszcze wykorzystywany do uwierzytelniania. |  | Active | Token jest aktywny i może być wykorzystywany do uwierzytelniania. |  | Revoking | Token jest w trakcie unieważniania. Nie może już być wykorzystywany do uwierzytelniania. |  | Revoked | Token został unieważniony i nie może być wykorzystywany do uwierzytelniania. |  | Failed | Nie udało się aktywować tokena. Należy wygenerować nowy token, obecny nie może być wykorzystywany do uwierzytelniania. | | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
