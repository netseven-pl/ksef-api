# # PersonPermission

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Identyfikator uprawnienia. | [optional]
**authorized_identifier** | **string** | Identyfikator uprawnionego. | [optional]
**authorized_identifier_type** | [**\NetSeven\KseF2Model\PersonPermissionsAuthorizedIdentifierType**](PersonPermissionsAuthorizedIdentifierType.md) | Typ identyfikatora uprawnionego. | [optional]
**target_identifier** | **string** | Identyfikator podmiotu docelowego. | [optional]
**target_identifier_type** | [**\NetSeven\KseF2Model\PersonPermissionsTargetIdentifierType**](PersonPermissionsTargetIdentifierType.md) | Typ identyfikatora podmiotu docelowego. | [optional]
**author_identifier** | **string** | Identyfikator uprawniającego. | [optional]
**author_identifier_type** | [**\NetSeven\KseF2Model\PersonPermissionsAuthorIdentifierType**](PersonPermissionsAuthorIdentifierType.md) | Typ identyfikatora uprawniającego. | [optional]
**permission_scope** | [**\NetSeven\KseF2Model\PersonPermissionScope**](PersonPermissionScope.md) | Uprawnienie. | [optional]
**description** | **string** | Opis uprawnienia. | [optional]
**permission_state** | [**\NetSeven\KseF2Model\PermissionState**](PermissionState.md) | Stan uprawnienia. | [optional]
**start_date** | **\DateTime** | Data rozpoczęcia obowiązywania uprawnienia. | [optional]
**can_delegate** | **bool** | Informacja o możliwości dalszego nadawania uprawnienia w sposób pośredni. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
