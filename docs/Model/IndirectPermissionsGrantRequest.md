# # IndirectPermissionsGrantRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**subject_identifier** | [**\OpenAPI\Client\Model\IndirectPermissionsSubjectIdentifier**](IndirectPermissionsSubjectIdentifier.md) | Identyfikator osoby fizycznej.  | Type | Value |  | --- | --- |  | Nip | 10 cyfrowy numer NIP |  | Pesel | 11 cyfrowy numer PESEL |  | Fingerprint | Odcisk palca certyfikatu | |
**target_identifier** | [**\OpenAPI\Client\Model\IndirectPermissionsTargetIdentifier**](IndirectPermissionsTargetIdentifier.md) | Identyfikator podmiotu, w którego kontekście chcemy pośrednio nadać uprawnienia. W przypadku nadawania uprawnienia generalnego, pole to powinno mieć wartość null.  | Type | Value |  | --- | --- |  | Nip | 10 cyfrowy numer NIP |  | InternalId | Dwuczłonowy identyfikator składający się z numeru NIP i 5 cyfr: &#x60;{nip}-{5_cyfr}&#x60; | | [optional]
**permissions** | [**\OpenAPI\Client\Model\IndirectPermissionType[]**](IndirectPermissionType.md) | Lista nadawanych uprawnień. Każda wartość może wystąpić tylko raz. |
**description** | **string** | Opis nadawanych uprawnień. |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
