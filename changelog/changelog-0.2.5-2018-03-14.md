## Version 0.2.4 to 0.2.2
---
### :sparkles: Added
---
* `GET` /api/v1/documents/{id4n}/{organizationId}/{fileName} - Retrieve a document (meta-data only, no content)
* `DELETE` /api/v1/documents/{id4n}/{organizationId}/{fileName} - Delete a document
* `PATCH` /api/v1/documents/{id4n}/{organizationId}/{fileName} - Update a document
* `GET` /api/v1/documents/{id4n}/{organizationId}/{fileName}/content - Read document contents
* `PUT` /api/v1/documents/{id4n}/{organizationId}/{fileName}/content - Write document contents
* `GET` /api/v1/public/documents/{id4n}/{organizationId}/{fileName}/content - Read document contents
* `PUT` /api/v1/documents/{id4n}/{organizationId} - Create an empty document for an id4n

### :recycle: Removed
---
* `GET` ~~/api/v1/documents/{id4n}/{organizationId}/{fileName}/metadata~~ - Retrieve a document (meta-data only, no content)
* `GET` ~~/api/v1/public/documents/{id4n}/{organizationId}/{fileName}/metadata~~ - Retrieve a document (meta-data only, no content)

### :wrench: Changed
---
* `PUT` /account/registration Complete registration  
  * :heavy_plus_sign: Property `code`
  * :heavy_plus_sign: Property `errorId`
  * :heavy_plus_sign: Property `errorList`
  * :heavy_plus_sign: Property `message`
* `POST` /account/verification Verify registration  
  * :heavy_plus_sign: Property `code`
  * :heavy_plus_sign: Property `errorId`
  * :heavy_plus_sign: Property `errorList`
  * :heavy_plus_sign: Property `message`
* `DELETE` /api/v1/apikeys/{key} Delete API key  
  * :heavy_plus_sign: Property `code`
  * :heavy_plus_sign: Property `errorId`
  * :heavy_plus_sign: Property `errorList`
  * :heavy_plus_sign: Property `message`
* `PUT` /api/v1/apikeys/{key} Update API keys  
  * :heavy_plus_sign: Property `code`
  * :heavy_plus_sign: Property `errorId`
  * :heavy_plus_sign: Property `errorList`
  * :heavy_plus_sign: Property `message`
* `DELETE` /api/v1/apikeys/{key}/privileges Remove privilege  
  * :heavy_plus_sign: Property `code`
  * :heavy_plus_sign: Property `errorId`
  * :heavy_plus_sign: Property `errorList`
  * :heavy_plus_sign: Property `message`
* `POST` /api/v1/apikeys/{key}/privileges Add privilege  
  * :heavy_plus_sign: Property `code`
  * :heavy_plus_sign: Property `errorId`
  * :heavy_plus_sign: Property `errorList`
  * :heavy_plus_sign: Property `message`
* `DELETE` /api/v1/apikeys/{key}/privileges/{privilege}/id4ns Remove id4ns of a privilege  
  * :heavy_plus_sign: Property `code`
  * :heavy_plus_sign: Property `errorId`
  * :heavy_plus_sign: Property `errorList`
  * :heavy_plus_sign: Property `message`
* `POST` /api/v1/apikeys/{key}/privileges/{privilege}/id4ns Add ID4ns of a privilege  
  * :heavy_plus_sign: Property `code`
  * :heavy_plus_sign: Property `errorId`
  * :heavy_plus_sign: Property `errorList`
  * :heavy_plus_sign: Property `message`
* `GET` /api/v1/billing/{organizationId} Get billing amount of services for a given organization  
  * :x: Parameter ~~`fromDate`~~ - Billing start date
  * :x: Parameter ~~`toDate`~~ - Billing end date
* `GET` /api/v1/billing/{organizationId}/positions Get billing positions for a given organization  
  * :x: Parameter ~~`fromDate`~~ - Billing start date
  * :x: Parameter ~~`toDate`~~ - Billing end date
* `DELETE` /api/v1/collections/labelled/{collectionId4n}/elements Remove elements from labelled collection  
  * :heavy_plus_sign: Property `code`
  * :heavy_plus_sign: Property `errorId`
  * :heavy_plus_sign: Property `errorList`
  * :heavy_plus_sign: Property `message`
* `POST` /api/v1/collections/labelled/{collectionId4n}/elements Add elements to labelled collection  
  * :heavy_plus_sign: Property `code`
  * :heavy_plus_sign: Property `errorId`
  * :heavy_plus_sign: Property `errorList`
  * :heavy_plus_sign: Property `message`
* `DELETE` /api/v1/collections/labelled/{id4n} Delete labelled collection  
  * :heavy_plus_sign: Property `code`
  * :heavy_plus_sign: Property `errorId`
  * :heavy_plus_sign: Property `errorList`
  * :heavy_plus_sign: Property `message`
* `DELETE` /api/v1/collections/logistic/{collectionId4n}/elements Remove elements from logistic collection  
  * :heavy_plus_sign: Property `code`
  * :heavy_plus_sign: Property `errorId`
  * :heavy_plus_sign: Property `errorList`
  * :heavy_plus_sign: Property `message`
* `POST` /api/v1/collections/logistic/{collectionId4n}/elements Add elements to logistic collection  
  * :heavy_plus_sign: Property `code`
  * :heavy_plus_sign: Property `errorId`
  * :heavy_plus_sign: Property `errorList`
  * :heavy_plus_sign: Property `message`
* `DELETE` /api/v1/collections/routing/{collectionId4n}/elements Remove elements from routing collection  
  * :heavy_plus_sign: Property `code`
  * :heavy_plus_sign: Property `errorId`
  * :heavy_plus_sign: Property `errorList`
  * :heavy_plus_sign: Property `message`
* `POST` /api/v1/collections/routing/{collectionId4n}/elements Add element to routing collection  
  * :heavy_plus_sign: Property `code`
  * :heavy_plus_sign: Property `errorId`
  * :heavy_plus_sign: Property `errorList`
  * :heavy_plus_sign: Property `message`
* `DELETE` /api/v1/collections/routing/{id4n} Delete routing collection  
  * :heavy_plus_sign: Property `code`
  * :heavy_plus_sign: Property `errorId`
  * :heavy_plus_sign: Property `errorList`
  * :heavy_plus_sign: Property `message`
* `DELETE` /api/v1/collections/{id4n} Delete collection  
  * :heavy_plus_sign: Property `code`
  * :heavy_plus_sign: Property `errorId`
  * :heavy_plus_sign: Property `errorList`
  * :heavy_plus_sign: Property `message`
* `DELETE` /api/v1/collections/{id4n}/elements Remove elements from collection  
  * :heavy_plus_sign: Property `code`
  * :heavy_plus_sign: Property `errorId`
  * :heavy_plus_sign: Property `errorList`
  * :heavy_plus_sign: Property `message`
* `POST` /api/v1/collections/{id4n}/elements Add elements to collection  
  * :heavy_plus_sign: Property `code`
  * :heavy_plus_sign: Property `errorId`
  * :heavy_plus_sign: Property `errorList`
  * :heavy_plus_sign: Property `message`
* `DELETE` /api/v1/guids/{id4n}/alias/{aliasType} Remove aliases from GUIDs  
  * :heavy_plus_sign: Property `code`
  * :heavy_plus_sign: Property `errorId`
  * :heavy_plus_sign: Property `errorList`
  * :heavy_plus_sign: Property `message`
* `POST` /api/v1/guids/{id4n}/alias/{aliasType} Add alias for GUIDs  
  * :heavy_plus_sign: Property `code`
  * :heavy_plus_sign: Property `errorId`
  * :heavy_plus_sign: Property `errorList`
  * :heavy_plus_sign: Property `message`
* `PUT` /api/v1/microstorage/{id4n}/{organization} Write data to microstorage  
  * Parameter `body` :memo: null -> binary data
* `DELETE` /api/v1/organizations/{organizationId} Delete organization  
  * :heavy_plus_sign: Property `code`
  * :heavy_plus_sign: Property `errorId`
  * :heavy_plus_sign: Property `errorList`
  * :heavy_plus_sign: Property `message`
* `DELETE` /api/v1/organizations/{organizationId}/addresses/billing Remove billing address  
  * :heavy_plus_sign: Property `code`
  * :heavy_plus_sign: Property `errorId`
  * :heavy_plus_sign: Property `errorList`
  * :heavy_plus_sign: Property `message`
* `DELETE` /api/v1/organizations/{organizationId}/logo Delete organization logo  
  * :heavy_plus_sign: Property `code`
  * :heavy_plus_sign: Property `errorId`
  * :heavy_plus_sign: Property `errorList`
  * :heavy_plus_sign: Property `message`
* `POST` /api/v1/organizations/{organizationId}/users/invite Invite Users  
  * :heavy_plus_sign: Property `code`
  * :heavy_plus_sign: Property `errorId`
  * :heavy_plus_sign: Property `errorList`
  * :heavy_plus_sign: Property `message`
* `DELETE` /api/v1/organizations/{organizationId}/users/{username}/roles Remove role(s) from user  
  * :heavy_plus_sign: Property `code`
  * :heavy_plus_sign: Property `errorId`
  * :heavy_plus_sign: Property `errorList`
  * :heavy_plus_sign: Property `message`
* `POST` /api/v1/organizations/{organizationId}/users/{username}/roles Add role(s) to user  
  * :heavy_plus_sign: Property `code`
  * :heavy_plus_sign: Property `errorId`
  * :heavy_plus_sign: Property `errorList`
  * :heavy_plus_sign: Property `message`
* `PUT` /api/v1/routingfiles/{id4n} Store routing file  
  * :heavy_plus_sign: Property `code`
  * :heavy_plus_sign: Property `errorId`
  * :heavy_plus_sign: Property `errorList`
  * :heavy_plus_sign: Property `message`
* `GET` /go/{guid} Forward  
  * :heavy_plus_sign: Property `code`
  * :heavy_plus_sign: Property `errorId`
  * :heavy_plus_sign: Property `errorList`
  * :heavy_plus_sign: Property `message`

