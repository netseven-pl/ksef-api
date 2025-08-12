# # EntityAuthorizationPermissionsQueryRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**authorizing_identifier** | [**\OpenAPI\Client\Model\EntityAuthorizationsAuthorizingEntityIdentifier**](EntityAuthorizationsAuthorizingEntityIdentifier.md) | Identyfikator podmiotu uprawniającego.  | Type | Value |  | --- | --- |  | Nip | 10 cyfrowy numer NIP | | [optional]
**authorized_identifier** | [**\OpenAPI\Client\Model\EntityAuthorizationsAuthorizedEntityIdentifier**](EntityAuthorizationsAuthorizedEntityIdentifier.md) | Identyfikator podmiotu uprawnionego.  | Type | Value |  | --- | --- |  | Nip | 10 cyfrowy numer NIP | | [optional]
**query_type** | [**\OpenAPI\Client\Model\QueryType**](QueryType.md) | Typ zapytania.  | Type | Value |  | --- | --- |  | Granted | Uprawnienia nadane innym podmiotom |  | Received | Uprawnienia otrzymane od innych podmiotów | |
**permission_types** | [**\OpenAPI\Client\Model\InvoicePermissionType[]**](InvoicePermissionType.md) | Możliwe uprawnienia do filtrowania. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
