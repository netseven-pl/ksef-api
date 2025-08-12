# # EntityAuthorizationGrant

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Identyfikator uprawnienia. | [optional]
**author_identifier** | **string** | Identyfikator osoby nadającej uprawnienie. | [optional]
**author_identifier_type** | [**\OpenAPI\Client\Model\EntityAuthorizationsAuthorIdentifierType**](EntityAuthorizationsAuthorIdentifierType.md) | Typ identyfikatora osoby nadającej uprawnienie. | [optional]
**authorized_entity_identifier** | **string** | Identyfikator podmiotu uprawnionego. | [optional]
**authorized_entity_identifier_type** | [**\OpenAPI\Client\Model\EntityAuthorizationsAuthorizedEntityIdentifierType**](EntityAuthorizationsAuthorizedEntityIdentifierType.md) | Typ identyfikatora podmiotu uprawnionego. | [optional]
**authorizing_entity_identifier** | **string** | Identyfikator podmiotu uprawniającego. | [optional]
**authorizing_entity_identifier_type** | [**\OpenAPI\Client\Model\EntityAuthorizationsAuthorizingEntityIdentifierType**](EntityAuthorizationsAuthorizingEntityIdentifierType.md) | Typ identyfikatora podmiotu uprawniającego. | [optional]
**authorization_scope** | [**\OpenAPI\Client\Model\InvoicePermissionType**](InvoicePermissionType.md) | Uprawnienie. | [optional]
**description** | **string** | Opis uprawnienia. | [optional]
**start_date** | **\DateTime** | Data rozpoczęcia obowiązywania uprawnienia. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
