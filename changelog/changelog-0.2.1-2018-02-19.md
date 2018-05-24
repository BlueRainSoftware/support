## Version 0.1.4 to 0.2.1
---
### :sparkles: Added
---
* `GET` /api/v1/documents/{id4n} - List documents
* `GET` /api/v1/documents/{id4n}/{organizationId} - List organization specific documents
* `PUT` /api/v1/documents/{id4n}/{organizationId} - Create an empty document for an id4n
* `GET` /api/v1/documents/{id4n}/{organizationId}/{fileName} - Retrieve a document (meta-data only, no content)
* `DELETE` /api/v1/documents/{id4n}/{organizationId}/{fileName} - Delete a document
* `PATCH` /api/v1/documents/{id4n}/{organizationId}/{fileName} - Update a document
* `GET` /api/v1/documents/{id4n}/{organizationId}/{fileName}/content - Read document contents
* `PUT` /api/v1/documents/{id4n}/{organizationId}/{fileName}/content - Write document contents
* `GET` /api/v1/microstorage/{id4n}/{organization} - Read data from microstorage
* `PUT` /api/v1/microstorage/{id4n}/{organization} - Write data to microstorage
* `GET` /api/v1/public/documents/{id4n} - List organization specific documents
* `GET` /api/v1/public/documents/{id4n}/{organizationId} - List organization specific documents
* `GET` /api/v1/public/documents/{id4n}/{organizationId}/{fileName} - Retrieve a document (meta-data only, no content)
* `GET` /api/v1/public/documents/{id4n}/{organizationId}/{fileName}/content - Read document contents

### :recycle: Removed
---
* `GET` ~~/api/v1/collections/{id4n}/documents~~ - List documents
* `GET` ~~/api/v1/collections/{id4n}/documents/{organizationId}~~ - List organization specific documents
* `PUT` ~~/api/v1/collections/{id4n}/documents/{organizationId}~~ - Create an empty document for an id4n
* `GET` ~~/api/v1/collections/{id4n}/documents/{organizationId}/{fileName}~~ - Retrieve a document (meta-data only, no content)
* `DELETE` ~~/api/v1/collections/{id4n}/documents/{organizationId}/{fileName}~~ - Delete a document
* `PATCH` ~~/api/v1/collections/{id4n}/documents/{organizationId}/{fileName}~~ - Update a document
* `GET` ~~/api/v1/collections/{id4n}/documents/{organizationId}/{fileName}/content~~ - Read document contents
* `PUT` ~~/api/v1/collections/{id4n}/documents/{organizationId}/{fileName}/content~~ - Write document contents
* `GET` ~~/api/v1/collections/{id4n}/micro/{organization}~~ - Read data from microstorage
* `PUT` ~~/api/v1/collections/{id4n}/micro/{organization}~~ - Write data to microstorage
* `GET` ~~/api/v1/guids/{id4n}/documents~~ - List documents
* `GET` ~~/api/v1/guids/{id4n}/documents/{organizationId}~~ - List organization specific documents
* `PUT` ~~/api/v1/guids/{id4n}/documents/{organizationId}~~ - Create an empty document for an id4n
* `GET` ~~/api/v1/guids/{id4n}/documents/{organizationId}/{fileName}~~ - Retrieve a document (meta-data only, no content)
* `DELETE` ~~/api/v1/guids/{id4n}/documents/{organizationId}/{fileName}~~ - Delete a document
* `PATCH` ~~/api/v1/guids/{id4n}/documents/{organizationId}/{fileName}~~ - Update a document
* `GET` ~~/api/v1/guids/{id4n}/documents/{organizationId}/{fileName}/content~~ - Read document contents
* `PUT` ~~/api/v1/guids/{id4n}/documents/{organizationId}/{fileName}/content~~ - Write document contents
* `GET` ~~/api/v1/guids/{id4n}/micro/{organization}~~ - Read data from microstorage
* `PUT` ~~/api/v1/guids/{id4n}/micro/{organization}~~ - Write data to microstorage
* `GET` ~~/api/v1/public/collections/{id4n}/documents~~ - List organization specific documents
* `GET` ~~/api/v1/public/collections/{id4n}/documents/{organizationId}~~ - List organization specific documents
* `GET` ~~/api/v1/public/collections/{id4n}/documents/{organizationId}/{fileName}~~ - Retrieve a document (meta-data only, no content)
* `GET` ~~/api/v1/public/collections/{id4n}/documents/{organizationId}/{fileName}/content~~ - Read document contents
* `GET` ~~/api/v1/public/guids/{id4n}/documents~~ - List organization specific documents
* `GET` ~~/api/v1/public/guids/{id4n}/documents/{organizationId}~~ - List organization specific documents
* `GET` ~~/api/v1/public/guids/{id4n}/documents/{organizationId}/{fileName}~~ - Retrieve a document (meta-data only, no content)
* `GET` ~~/api/v1/public/guids/{id4n}/documents/{organizationId}/{fileName}/content~~ - Read document contents

### :wrench: Changed
---
* `POST` /account/password Request password reset  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `PUT` /account/password Verify password reset  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `POST` /account/registration Register user  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `PUT` /account/registration Complete registration  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `POST` /account/verification Verify registration  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `POST` /api/v1/apikeys Create API key  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `GET` /api/v1/apikeys Find API key by organization  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `GET` /api/v1/apikeys/privileges List all privileges  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `GET` /api/v1/apikeys/{key} Show API key  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `DELETE` /api/v1/apikeys/{key} Delete API key  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `PUT` /api/v1/apikeys/{key} Update API keys  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `POST` /api/v1/apikeys/{key}/privileges Add privilege  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `GET` /api/v1/apikeys/{key}/privileges List privileges  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `DELETE` /api/v1/apikeys/{key}/privileges Remove privilege  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `POST` /api/v1/apikeys/{key}/privileges/{privilege}/id4ns Add ID4ns of a privilege  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `GET` /api/v1/apikeys/{key}/privileges/{privilege}/id4ns ID4ns of a privilege  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `DELETE` /api/v1/apikeys/{key}/privileges/{privilege}/id4ns Remove id4ns of a privilege  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `GET` /api/v1/billing/{organizationId} Get billing amount of services for a given organization  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `POST` /api/v1/collections/labelled Create labelled collection  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `POST` /api/v1/collections/labelled/{collectionId4n}/elements Add elements to labelled collection  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `DELETE` /api/v1/collections/labelled/{collectionId4n}/elements Remove elements from labelled collection  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `GET` /api/v1/collections/labelled/{id4n} Find labelled collection  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `DELETE` /api/v1/collections/labelled/{id4n} Delete labelled collection  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `PATCH` /api/v1/collections/labelled/{id4n} Update labelled collection  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `PUT` /api/v1/collections/labelled/{id4n} Set labelled collection values  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `GET` /api/v1/collections/labelled/{id4n}/elements List contents of the collection  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `POST` /api/v1/collections/logistic Create logistic collection  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `POST` /api/v1/collections/logistic/{collectionId4n}/elements Add elements to logistic collection  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `DELETE` /api/v1/collections/logistic/{collectionId4n}/elements Remove elements from logistic collection  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `GET` /api/v1/collections/logistic/{id4n} Find logistic collection  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `DELETE` /api/v1/collections/logistic/{id4n} Delete logistic collection  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `PATCH` /api/v1/collections/logistic/{id4n} Update logistic collection  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `PUT` /api/v1/collections/logistic/{id4n} Replace logistic collection  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `GET` /api/v1/collections/logistic/{id4n}/elements List contents of the collection  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `POST` /api/v1/collections/routing Create routing collecton  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `POST` /api/v1/collections/routing/{collectionId4n}/elements Add element to routing collection  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `DELETE` /api/v1/collections/routing/{collectionId4n}/elements Remove elements from routing collection  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `GET` /api/v1/collections/routing/{id4n} Find routing collection  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `DELETE` /api/v1/collections/routing/{id4n} Delete routing collection  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `PATCH` /api/v1/collections/routing/{id4n} Update routing collection  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `PUT` /api/v1/collections/routing/{id4n} Update routing collection  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `GET` /api/v1/collections/routing/{id4n}/elements List contents of the collection  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `GET` /api/v1/collections/{id4n} Find collection  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `DELETE` /api/v1/collections/{id4n} Delete collection  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `PATCH` /api/v1/collections/{id4n} Update collection  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `PUT` /api/v1/collections/{id4n} Set collection  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `POST` /api/v1/collections/{id4n}/elements Add elements to collection  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `GET` /api/v1/collections/{id4n}/elements List contents of the collection  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `DELETE` /api/v1/collections/{id4n}/elements Remove elements from collection  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `GET` /api/v1/countries List countries  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `POST` /api/v1/guids Create GUID(s)  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `GET` /api/v1/guids/withoutCollection Retrieve GUIDs not in any collection  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `GET` /api/v1/guids/{id4n} Retrieve GUID information  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `PATCH` /api/v1/guids/{id4n} Change GUID information.  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `PUT` /api/v1/guids/{id4n} Change GUID information.  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `GET` /api/v1/guids/{id4n}/alias Get all aliases for the given GUID  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `POST` /api/v1/guids/{id4n}/alias/{aliasType} Add alias for GUIDs  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `DELETE` /api/v1/guids/{id4n}/alias/{aliasType} Remove aliases from GUIDs  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `GET` /api/v1/id4ns/{id4n} Retrieve ID4n information  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `GET` /api/v1/info Retrieve version information about ID4i  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `POST` /api/v1/organizations Create organization  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `GET` /api/v1/organizations/{organizationId} Find organization by id  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `DELETE` /api/v1/organizations/{organizationId} Delete organization  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `PUT` /api/v1/organizations/{organizationId} Update organization  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `GET` /api/v1/organizations/{organizationId}/addresses/billing Retrieve billing address  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `DELETE` /api/v1/organizations/{organizationId}/addresses/billing Remove billing address  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `PUT` /api/v1/organizations/{organizationId}/addresses/billing Store billing address  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `GET` /api/v1/organizations/{organizationId}/addresses/default Retrieve address  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `PUT` /api/v1/organizations/{organizationId}/addresses/default Store address  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `GET` /api/v1/organizations/{organizationId}/collections Get collections of organization  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `POST` /api/v1/organizations/{organizationId}/logo Update organization logo  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `DELETE` /api/v1/organizations/{organizationId}/logo Delete organization logo  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `GET` /api/v1/organizations/{organizationId}/roles List users and their roles  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `GET` /api/v1/organizations/{organizationId}/users Find users in organization  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `POST` /api/v1/organizations/{organizationId}/users/invite Invite Users  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `POST` /api/v1/organizations/{organizationId}/users/{username}/roles Add role(s) to user  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `GET` /api/v1/organizations/{organizationId}/users/{username}/roles Get user roles by username  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `DELETE` /api/v1/organizations/{organizationId}/users/{username}/roles Remove role(s) from user  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `GET` /api/v1/public/image/{imageID} Resolve image  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `GET` /api/v1/roles List roles  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `GET` /api/v1/routingfiles/{id4n} Retrieve routing file  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `PUT` /api/v1/routingfiles/{id4n} Store routing file  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `GET` /api/v1/routingfiles/{id4n}/route/{type} Retrieve current route of a GUID (or ID4N)  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `GET` /api/v1/search/guids Search for GUIDs by alias  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `GET` /api/v1/search/guids/aliases/types List all supported alias types  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `GET` /api/v1/user/organizations Retrieve organizations of user  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `GET` /api/v1/users Find users  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `GET` /api/v1/users/{username} Find by username  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `GET` /go/{guid} Forward  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language
* `GET` /whois/{id4n} Resolve owner of id4n  
  * :x: Parameter ~~`Authorization`~~ - Authorization JWT Bearer Token
  * :x: Parameter ~~`Accept-Language`~~ - Requested language

