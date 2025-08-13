# # PersonPermissionsQueryRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**author_identifier** | [**\NetSeven\KseF2Model\PersonPermissionsAuthorIdentifier**](PersonPermissionsAuthorIdentifier.md) | Identyfikator osoby lub podmiotu nadającego uprawnienie.  | Type | Value |  | --- | --- |  | Nip | 10 cyfrowy numer NIP |  | Pesel | 11 cyfrowy numer PESEL |  | Fingerprint | Odcisk palca certyfikatu | | [optional]
**authorized_identifier** | [**\NetSeven\KseF2Model\PersonPermissionsAuthorizedIdentifier**](PersonPermissionsAuthorizedIdentifier.md) | Identyfikator osoby lub podmiotu uprawnionego.  | Type | Value |  | --- | --- |  | Nip | 10 cyfrowy numer NIP |  | Pesel | 11 cyfrowy numer PESEL |  | Fingerprint | Odcisk palca certyfikatu | | [optional]
**target_identifier** | [**\NetSeven\KseF2Model\PersonPermissionsTargetIdentifier**](PersonPermissionsTargetIdentifier.md) | Identyfikator podmiotu docelowego (dla uprawnień pośrednich).  | Type | Value |  | --- | --- |  | Nip | 10 cyfrowy numer NIP | | [optional]
**permission_types** | [**\NetSeven\KseF2Model\PersonPermissionType[]**](PersonPermissionType.md) | Możliwe uprawnienia do filtrowania. | [optional]
**permission_state** | [**\NetSeven\KseF2Model\PermissionState**](PermissionState.md) | Stan uprawnienia.   | Type | Value |  | --- | --- |  | Active | Uprawnienia aktywne |  | Inactive | Uprawnienia nieaktywne, nadane w sposób poœredni | | [optional]
**query_type** | [**\NetSeven\KseF2Model\PersonPermissionsQueryType**](PersonPermissionsQueryType.md) | Typ zapytania.  | Type | Value |  | --- | --- |  | PermissionsInCurrentContext | Uprawnienia posiadane w aktualnym kontekście |  | PermissionsGrantedInCurrentContext | Uprawnienia nadane w aktualnym kontekście | |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
