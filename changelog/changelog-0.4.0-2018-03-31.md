## Version 0.2.2 to 0.4.0
---
### :sparkles: Added
---
* `GET` /api/v1/changelog/organization/{organizationId}/ - List change log entries of an organization
* `GET` /api/v1/documents/{id4n}/{organizationId}/{fileName}/metadata - Retrieve a document (meta-data only, no content)
* `PATCH` /api/v1/documents/{id4n}/{organizationId}/{fileName}/metadata - Update a document
* `GET` /api/v1/public/documents/{id4n}/{organizationId}/{fileName}/metadata - Retrieve a document (meta-data only, no content)
* `GET` /api/v1/public/routes/{id4n} - Retrieve all public routes for a GUID
* `GET` /api/v1/routingfiles/{id4n}/routes - Retrieve all web routes
* `GET` /api/v1/routingfiles/{id4n}/routes/{type} - Retrieve current route of a GUID (or ID4N)
* `GET` /api/v1/transfers/{id4n}/receiveInfo - Show transfer information
* `PUT` /api/v1/transfers/{id4n}/receiveInfo - Transfer a GUID or collection, obtaining it (i.e. becoming the holder) and if allowed also taking ownership
* `GET` /api/v1/transfers/{id4n}/sendInfo - Show transfer preparation information
* `PUT` /api/v1/transfers/{id4n}/sendInfo - Prepare an object for transfer

### :recycle: Removed
---
* `GET` ~~/api/v1/documents/{id4n}/{organizationId}/{fileName}/content~~ - Read document contents
* `PUT` ~~/api/v1/documents/{id4n}/{organizationId}/{fileName}/content~~ - Write document contents
* `GET` ~~/api/v1/public/documents/{id4n}/{organizationId}/{fileName}/content~~ - Read document contents
* `GET` ~~/api/v1/routingfiles/{id4n}/route/{type}~~ - Retrieve current route of a GUID (or ID4N)
* `PUT` ~~/api/v1/collections/labelled/{id4n}~~ - Set labelled collection values
* `PUT` ~~/api/v1/collections/logistic/{id4n}~~ - Replace logistic collection
* `PUT` ~~/api/v1/collections/routing/{id4n}~~ - Update routing collection
* `PUT` ~~/api/v1/collections/{id4n}~~ - Set collection
* `PATCH` ~~/api/v1/documents/{id4n}/{organizationId}/{fileName}~~ - Update a document

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
* `PATCH` /api/v1/collections/labelled/{id4n} Update labelled collection  
  * :heavy_plus_sign: Property `request.holderOrganizationId` - The UTC unix timestamp of when this collection has been created
  * :x: Property `request.nextScanOwnership`
* `GET` /api/v1/collections/labelled/{id4n} Find labelled collection  
  * :heavy_plus_sign: Property `holderOrganizationId` - The UTC unix timestamp of when this collection has been created
  * :x: Property `nextScanOwnership`
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
* `PATCH` /api/v1/collections/logistic/{id4n} Update logistic collection  
  * :heavy_plus_sign: Property `request.holderOrganizationId` - The UTC unix timestamp of when this collection has been created
  * :x: Property `request.nextScanOwnership`
* `GET` /api/v1/collections/logistic/{id4n} Find logistic collection  
  * :heavy_plus_sign: Property `holderOrganizationId` - The UTC unix timestamp of when this collection has been created
  * :x: Property `nextScanOwnership`
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
* `PATCH` /api/v1/collections/routing/{id4n} Update routing collection  
  * :heavy_plus_sign: Property `request.holderOrganizationId` - The UTC unix timestamp of when this collection has been created
  * :x: Property `request.nextScanOwnership`
* `GET` /api/v1/collections/routing/{id4n} Find routing collection  
  * :heavy_plus_sign: Property `holderOrganizationId` - The UTC unix timestamp of when this collection has been created
  * :x: Property `nextScanOwnership`
* `DELETE` /api/v1/collections/{id4n} Delete collection  
  * :x: Property `code`
  * :x: Property `errorId`
  * :x: Property `errorList`
  * :x: Property `message`
* `PATCH` /api/v1/collections/{id4n} Update collection  
  * :heavy_plus_sign: Property `request.holderOrganizationId` - The UTC unix timestamp of when this collection has been created
  * :x: Property `request.nextScanOwnership`
* `GET` /api/v1/collections/{id4n} Find collection  
  * :heavy_plus_sign: Property `holderOrganizationId` - The UTC unix timestamp of when this collection has been created
  * :x: Property `nextScanOwnership`
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
* `PUT` /api/v1/documents/{id4n}/{organizationId} Create an empty document for an id4n  
  * :heavy_plus_sign: Parameter `content` - content
  * :x: Parameter ~~`mimeType`~~ - mimeType
  * :x: Parameter ~~`document`~~ - document
  * :heavy_plus_sign: Property `mimeType` - Mime Type
* `PATCH` /api/v1/guids/{id4n} Change GUID information.  
  * :heavy_plus_sign: Property `request.holderOrganizationId` - Organization ID of the GUID holder
  * :x: Property `request.nextScanOwnership`
* `GET` /api/v1/guids/{id4n} Retrieve GUID information  
  * :heavy_plus_sign: Property `holderOrganizationId` - Organization ID of the GUID holder
  * :x: Property `nextScanOwnership`
* `PUT` /api/v1/guids/{id4n} Change GUID information.  
  * :heavy_plus_sign: Property `request.holderOrganizationId` - Organization ID of the GUID holder
  * :x: Property `request.nextScanOwnership`
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
* `GET` /api/v1/id4ns/{id4n} Retrieve ID4n information  
  * :heavy_plus_sign: Property `holderOrganizationId` - ${Id4nPresentation.Guid.holderOrganizationId}
  * :heavy_plus_sign: Property `ownerOrganizationId` - ${Id4nPresentation.Guid.ownerOrganizationId}
  * :x: Property `nextScanOwnership` - Indicates if next scan ownership is active or not. If privileges are missing or the type of object doesn't support NSO this value is null.
* `PUT` /api/v1/microstorage/{id4n}/{organization} Write data to microstorage  
  * Parameter `body`not required :memo: binary data -> body
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

