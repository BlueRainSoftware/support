## Version 0.1.3 to 0.1.4
---
### :sparkles: Added
---
* `GET` /api/v1/collections/{id4n}/documents - List documents
* `GET` /api/v1/collections/{id4n}/documents/{organizationId} - List organization specific documents
* `PUT` /api/v1/collections/{id4n}/documents/{organizationId} - Create an empty document for an id4n
* `GET` /api/v1/collections/{id4n}/documents/{organizationId}/{fileName} - Retrieve a document (meta-data only, no content)
* `DELETE` /api/v1/collections/{id4n}/documents/{organizationId}/{fileName} - Delete a document
* `PATCH` /api/v1/collections/{id4n}/documents/{organizationId}/{fileName} - Update a document
* `GET` /api/v1/collections/{id4n}/documents/{organizationId}/{fileName}/content - Read document contents
* `PUT` /api/v1/collections/{id4n}/documents/{organizationId}/{fileName}/content - Write document contents
* `GET` /api/v1/collections/{id4n}/micro/{organization} - Read data from microstorage
* `PUT` /api/v1/collections/{id4n}/micro/{organization} - Write data to microstorage
* `GET` /api/v1/guids/{id4n}/documents - List documents
* `GET` /api/v1/guids/{id4n}/documents/{organizationId} - List organization specific documents
* `PUT` /api/v1/guids/{id4n}/documents/{organizationId} - Create an empty document for an id4n
* `GET` /api/v1/guids/{id4n}/documents/{organizationId}/{fileName} - Retrieve a document (meta-data only, no content)
* `DELETE` /api/v1/guids/{id4n}/documents/{organizationId}/{fileName} - Delete a document
* `PATCH` /api/v1/guids/{id4n}/documents/{organizationId}/{fileName} - Update a document
* `GET` /api/v1/guids/{id4n}/documents/{organizationId}/{fileName}/content - Read document contents
* `PUT` /api/v1/guids/{id4n}/documents/{organizationId}/{fileName}/content - Write document contents
* `GET` /api/v1/guids/{id4n}/micro/{organization} - Read data from microstorage
* `PUT` /api/v1/guids/{id4n}/micro/{organization} - Write data to microstorage
* `GET` /api/v1/id4ns/{id4n} - Retrieve ID4n information
* `GET` /api/v1/public/collections/{id4n}/documents - List organization specific documents
* `GET` /api/v1/public/collections/{id4n}/documents/{organizationId} - List organization specific documents
* `GET` /api/v1/public/collections/{id4n}/documents/{organizationId}/{fileName} - Retrieve a document (meta-data only, no content)
* `GET` /api/v1/public/collections/{id4n}/documents/{organizationId}/{fileName}/content - Read document contents
* `GET` /api/v1/public/guids/{id4n}/documents - List organization specific documents
* `GET` /api/v1/public/guids/{id4n}/documents/{organizationId} - List organization specific documents
* `GET` /api/v1/public/guids/{id4n}/documents/{organizationId}/{fileName} - Retrieve a document (meta-data only, no content)
* `GET` /api/v1/public/guids/{id4n}/documents/{organizationId}/{fileName}/content - Read document contents
* `POST` /api/v1/collections/labelled/{collectionId4n}/elements - Add elements to labelled collection
* `PATCH` /api/v1/collections/labelled/{id4n} - Update labelled collection
* `POST` /api/v1/collections/logistic/{collectionId4n}/elements - Add elements to logistic collection
* `PATCH` /api/v1/collections/logistic/{id4n} - Update logistic collection
* `POST` /api/v1/collections/routing/{collectionId4n}/elements - Add element to routing collection
* `PATCH` /api/v1/collections/routing/{id4n} - Update routing collection
* `PATCH` /api/v1/collections/{id4n} - Update collection
* `POST` /api/v1/collections/{id4n}/elements - Add elements to collection
* `PATCH` /api/v1/guids/{id4n} - Change GUID information.

### :recycle: Removed
---
* `PUT` ~~/api/v1/collections/labelled/{collectionId4n}/elements/{elementGuid}~~ - Add element to labelled collection
* `DELETE` ~~/api/v1/collections/labelled/{collectionId4n}/elements/{elementGuid}~~ - Remove element from labelled collection
* `DELETE` ~~/api/v1/collections/logistic/{collectionId4n}/elements/{elementId4n}~~ - Remove element from logistic collection
* `PUT` ~~/api/v1/collections/logistic/{collectionId4n}/elements/{guid}~~ - Add element to logistic collection
* `PUT` ~~/api/v1/collections/routing/{collectionId4n}/elements/{guid}~~ - Add element to routing collection
* `DELETE` ~~/api/v1/collections/routing/{collectionId4n}/elements/{guid}~~ - Remove element from routing collection
* `PUT` ~~/api/v1/collections/{id4n}/elements/{elementGuid}~~ - Add element to collection
* `DELETE` ~~/api/v1/collections/{id4n}/elements/{elementGuid}~~ - Remove element from collection
* `GET` ~~/api/v1/microstorage/{id4n}/{organization}~~ - Read data from microstorage
* `PUT` ~~/api/v1/microstorage/{id4n}/{organization}~~ - Write data to microstorage
* `PUT` ~~/api/v1/collections/labelled/{collectionId4n}/elements~~ - Add elements to labelled collection
* `PUT` ~~/api/v1/collections/logistic/{collectionId4n}/elements~~ - Add elements to logistic collection
* `PUT` ~~/api/v1/collections/routing/{collectionId4n}/elements~~ - Add element to routing collection
* `PUT` ~~/api/v1/collections/{id4n}/elements~~ - Add elements to collection

### :wrench: Changed
---
* `POST` /account/registration Register user  
  * :heavy_plus_sign: Property `id`
* `GET` /api/v1/apikeys Find API key by organization  
  * Parameter `offset` :memo: Start with the n-th element.  -> Start with the n-th element
  * Parameter `limit` :memo: The maximum count of returned elements. -> The maximum count of returned elements
* `GET` /api/v1/apikeys/privileges List all privileges  
  * Parameter `offset` :memo: Start with the n-th element.  -> Start with the n-th element
  * Parameter `limit` :memo: The maximum count of returned elements. -> The maximum count of returned elements
* `GET` /api/v1/apikeys/{key}/privileges List privileges  
  * Parameter `offset` :memo: Start with the n-th element.  -> Start with the n-th element
  * Parameter `limit` :memo: The maximum count of returned elements. -> The maximum count of returned elements
* `GET` /api/v1/apikeys/{key}/privileges/{privilege}/id4ns ID4ns of a privilege  
  * Parameter `offset` :memo: Start with the n-th element.  -> Start with the n-th element
  * Parameter `limit` :memo: The maximum count of returned elements. -> The maximum count of returned elements
* `GET` /api/v1/collections/labelled/{id4n}/elements List contents of the collection  
  * Parameter `offset` :memo: Start with the n-th element.  -> Start with the n-th element
  * Parameter `limit` :memo: The maximum count of returned elements. -> The maximum count of returned elements
* `GET` /api/v1/collections/logistic/{id4n}/elements List contents of the collection  
  * Parameter `offset` :memo: Start with the n-th element.  -> Start with the n-th element
  * Parameter `limit` :memo: The maximum count of returned elements. -> The maximum count of returned elements
* `GET` /api/v1/collections/routing/{id4n}/elements List contents of the collection  
  * Parameter `offset` :memo: Start with the n-th element.  -> Start with the n-th element
  * Parameter `limit` :memo: The maximum count of returned elements. -> The maximum count of returned elements
* `GET` /api/v1/collections/{id4n}/elements List contents of the collection  
  * Parameter `offset` :memo: Start with the n-th element.  -> Start with the n-th element
  * Parameter `limit` :memo: The maximum count of returned elements. -> The maximum count of returned elements
* `GET` /api/v1/countries List countries  
  * Parameter `offset` :memo: Start with the n-th element.  -> Start with the n-th element
  * Parameter `limit` :memo: The maximum count of returned elements. -> The maximum count of returned elements
* `GET` /api/v1/guids/withoutCollection Retrieve GUIDs not in any collection  
  * Parameter `offset` :memo: Start with the n-th element.  -> Start with the n-th element
  * Parameter `limit` :memo: The maximum count of returned elements. -> The maximum count of returned elements
* `GET` /api/v1/organizations/{organizationId}/collections Get collections of organization  
  * Parameter `offset` :memo: Start with the n-th element.  -> Start with the n-th element
  * Parameter `limit` :memo: The maximum count of returned elements. -> The maximum count of returned elements
* `POST` /api/v1/organizations/{organizationId}/logo Update organization logo  
  * :heavy_plus_sign: Property `uri` - The uri/url of the image
  * :x: Property `code`
  * :x: Property `errorId`
  * :x: Property `errorList`
  * :x: Property `message`
* `GET` /api/v1/organizations/{organizationId}/roles List users and their roles  
  * Parameter `offset` :memo: Start with the n-th element.  -> Start with the n-th element
  * Parameter `limit` :memo: The maximum count of returned elements. -> The maximum count of returned elements
* `GET` /api/v1/organizations/{organizationId}/users Find users in organization  
  * Parameter `offset` :memo: Start with the n-th element.  -> Start with the n-th element
  * Parameter `limit` :memo: The maximum count of returned elements. -> The maximum count of returned elements
* `GET` /api/v1/organizations/{organizationId}/users/{username}/roles Get user roles by username  
  * Parameter `offset` :memo: Start with the n-th element.  -> Start with the n-th element
  * Parameter `limit` :memo: The maximum count of returned elements. -> The maximum count of returned elements
* `GET` /api/v1/roles List roles  
  * Parameter `offset` :memo: Start with the n-th element.  -> Start with the n-th element
  * Parameter `limit` :memo: The maximum count of returned elements. -> The maximum count of returned elements
* `GET` /api/v1/search/guids Search for GUIDs by alias  
  * Parameter `offset` :memo: Start with the n-th element.  -> Start with the n-th element
  * Parameter `limit` :memo: The maximum count of returned elements. -> The maximum count of returned elements
* `GET` /api/v1/user/organizations Retrieve organizations of user  
  * Parameter `offset` :memo: Start with the n-th element.  -> Start with the n-th element
  * Parameter `limit` :memo: The maximum count of returned elements. -> The maximum count of returned elements
* `GET` /api/v1/users Find users  
  * Parameter `offset` :memo: Start with the n-th element.  -> Start with the n-th element
  * Parameter `limit` :memo: The maximum count of returned elements. -> The maximum count of returned elements

