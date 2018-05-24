## Version 0.2.2 to 0.2.4
---
### :sparkles: Added
---
* `GET` /api/v1/documents/{id4n}/{organizationId}/{fileName}/metadata - Retrieve a document (meta-data only, no content)
* `GET` /api/v1/public/documents/{id4n}/{organizationId}/{fileName}/metadata - Retrieve a document (meta-data only, no content)

### :recycle: Removed
---
* `GET` ~~/api/v1/documents/{id4n}/{organizationId}/{fileName}~~ - Retrieve a document (meta-data only, no content)
* `DELETE` ~~/api/v1/documents/{id4n}/{organizationId}/{fileName}~~ - Delete a document
* `PATCH` ~~/api/v1/documents/{id4n}/{organizationId}/{fileName}~~ - Update a document
* `GET` ~~/api/v1/documents/{id4n}/{organizationId}/{fileName}/content~~ - Read document contents
* `PUT` ~~/api/v1/documents/{id4n}/{organizationId}/{fileName}/content~~ - Write document contents
* `GET` ~~/api/v1/public/documents/{id4n}/{organizationId}/{fileName}/content~~ - Read document contents
* `PUT` ~~/api/v1/documents/{id4n}/{organizationId}~~ - Create an empty document for an id4n

### :wrench: Changed
---
* `PUT` /account/registration Complete registration  
  * :x: Property `code`
  * :x: Property `errorId`
  * :x: Property `errorList`
  * :x: Property `message`
* `POST` /account/verification Verify registration  
  * :x: Property `code`
  * :x: Property `errorId`
  * :x: Property `errorList`
  * :x: Property `message`
* `DELETE` /api/v1/apikeys/{key} Delete API key  
  * :x: Property `code`
  * :x: Property `errorId`
  * :x: Property `errorList`
  * :x: Property `message`
* `PUT` /api/v1/apikeys/{key} Update API keys  
  * :x: Property `code`
  * :x: Property `errorId`
  * :x: Property `errorList`
  * :x: Property `message`
* `DELETE` /api/v1/apikeys/{key}/privileges Remove privilege  
  * :x: Property `code`
  * :x: Property `errorId`
  * :x: Property `errorList`
  * :x: Property `message`
* `POST` /api/v1/apikeys/{key}/privileges Add privilege  
  * :x: Property `code`
  * :x: Property `errorId`
  * :x: Property `errorList`
  * :x: Property `message`
* `DELETE` /api/v1/apikeys/{key}/privileges/{privilege}/id4ns Remove id4ns of a privilege  
  * :x: Property `code`
  * :x: Property `errorId`
  * :x: Property `errorList`
  * :x: Property `message`
* `POST` /api/v1/apikeys/{key}/privileges/{privilege}/id4ns Add ID4ns of a privilege  
  * :x: Property `code`
  * :x: Property `errorId`
  * :x: Property `errorList`
  * :x: Property `message`
* `GET` /api/v1/billing/{organizationId} Get billing amount of services for a given organization  
  * :heavy_plus_sign: Parameter `fromDate` - Billing start date
  * :heavy_plus_sign: Parameter `toDate` - Billing end date
* `GET` /api/v1/billing/{organizationId}/positions Get billing positions for a given organization  
  * :heavy_plus_sign: Parameter `fromDate` - Billing start date
  * :heavy_plus_sign: Parameter `toDate` - Billing end date
* `DELETE` /api/v1/collections/labelled/{collectionId4n}/elements Remove elements from labelled collection  
  * :x: Property `code`
  * :x: Property `errorId`
  * :x: Property `errorList`
  * :x: Property `message`
* `POST` /api/v1/collections/labelled/{collectionId4n}/elements Add elements to labelled collection  
  * :x: Property `code`
  * :x: Property `errorId`
  * :x: Property `errorList`
  * :x: Property `message`
* `DELETE` /api/v1/collections/labelled/{id4n} Delete labelled collection  
  * :x: Property `code`
  * :x: Property `errorId`
  * :x: Property `errorList`
  * :x: Property `message`
* `DELETE` /api/v1/collections/logistic/{collectionId4n}/elements Remove elements from logistic collection  
  * :x: Property `code`
  * :x: Property `errorId`
  * :x: Property `errorList`
  * :x: Property `message`
* `POST` /api/v1/collections/logistic/{collectionId4n}/elements Add elements to logistic collection  
  * :x: Property `code`
  * :x: Property `errorId`
  * :x: Property `errorList`
  * :x: Property `message`
* `DELETE` /api/v1/collections/routing/{collectionId4n}/elements Remove elements from routing collection  
  * :x: Property `code`
  * :x: Property `errorId`
  * :x: Property `errorList`
  * :x: Property `message`
* `POST` /api/v1/collections/routing/{collectionId4n}/elements Add element to routing collection  
  * :x: Property `code`
  * :x: Property `errorId`
  * :x: Property `errorList`
  * :x: Property `message`
* `DELETE` /api/v1/collections/routing/{id4n} Delete routing collection  
  * :x: Property `code`
  * :x: Property `errorId`
  * :x: Property `errorList`
  * :x: Property `message`
* `DELETE` /api/v1/collections/{id4n} Delete collection  
  * :x: Property `code`
  * :x: Property `errorId`
  * :x: Property `errorList`
  * :x: Property `message`
* `DELETE` /api/v1/collections/{id4n}/elements Remove elements from collection  
  * :x: Property `code`
  * :x: Property `errorId`
  * :x: Property `errorList`
  * :x: Property `message`
* `POST` /api/v1/collections/{id4n}/elements Add elements to collection  
  * :x: Property `code`
  * :x: Property `errorId`
  * :x: Property `errorList`
  * :x: Property `message`
* `DELETE` /api/v1/guids/{id4n}/alias/{aliasType} Remove aliases from GUIDs  
  * :x: Property `code`
  * :x: Property `errorId`
  * :x: Property `errorList`
  * :x: Property `message`
* `POST` /api/v1/guids/{id4n}/alias/{aliasType} Add alias for GUIDs  
  * :x: Property `code`
  * :x: Property `errorId`
  * :x: Property `errorList`
  * :x: Property `message`
* `PUT` /api/v1/microstorage/{id4n}/{organization} Write data to microstorage  
  * Parameter `body` :memo: binary data -> null
* `DELETE` /api/v1/organizations/{organizationId} Delete organization  
  * :x: Property `code`
  * :x: Property `errorId`
  * :x: Property `errorList`
  * :x: Property `message`
* `DELETE` /api/v1/organizations/{organizationId}/addresses/billing Remove billing address  
  * :x: Property `code`
  * :x: Property `errorId`
  * :x: Property `errorList`
  * :x: Property `message`
* `DELETE` /api/v1/organizations/{organizationId}/logo Delete organization logo  
  * :x: Property `code`
  * :x: Property `errorId`
  * :x: Property `errorList`
  * :x: Property `message`
* `POST` /api/v1/organizations/{organizationId}/users/invite Invite Users  
  * :x: Property `code`
  * :x: Property `errorId`
  * :x: Property `errorList`
  * :x: Property `message`
* `DELETE` /api/v1/organizations/{organizationId}/users/{username}/roles Remove role(s) from user  
  * :x: Property `code`
  * :x: Property `errorId`
  * :x: Property `errorList`
  * :x: Property `message`
* `POST` /api/v1/organizations/{organizationId}/users/{username}/roles Add role(s) to user  
  * :x: Property `code`
  * :x: Property `errorId`
  * :x: Property `errorList`
  * :x: Property `message`
* `PUT` /api/v1/routingfiles/{id4n} Store routing file  
  * :x: Property `code`
  * :x: Property `errorId`
  * :x: Property `errorList`
  * :x: Property `message`
* `GET` /go/{guid} Forward  
  * :x: Property `code`
  * :x: Property `errorId`
  * :x: Property `errorList`
  * :x: Property `message`

