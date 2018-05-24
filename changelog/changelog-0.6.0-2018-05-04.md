## Version 0.5.1 to 0.6.0
May the fo(rce|ourth) be with you :rocket:
---
### :sparkles: Added
---
* `POST` /api/v1/collections - Create collection

### :recycle: Removed
---
* `POST` ~~/api/v1/collections/labelled~~ - Create labelled collection
* `POST` ~~/api/v1/collections/labelled/{collectionId4n}/elements~~ - Add elements to labelled collection
* `DELETE` ~~/api/v1/collections/labelled/{collectionId4n}/elements~~ - Remove elements from labelled collection
* `GET` ~~/api/v1/collections/labelled/{id4n}~~ - Find labelled collection
* `DELETE` ~~/api/v1/collections/labelled/{id4n}~~ - Delete labelled collection
* `PATCH` ~~/api/v1/collections/labelled/{id4n}~~ - Update labelled collection
* `GET` ~~/api/v1/collections/labelled/{id4n}/elements~~ - List contents of the collection
* `POST` ~~/api/v1/collections/logistic~~ - Create logistic collection
* `POST` ~~/api/v1/collections/logistic/{collectionId4n}/elements~~ - Add elements to logistic collection
* `DELETE` ~~/api/v1/collections/logistic/{collectionId4n}/elements~~ - Remove elements from logistic collection
* `GET` ~~/api/v1/collections/logistic/{id4n}~~ - Find logistic collection
* `DELETE` ~~/api/v1/collections/logistic/{id4n}~~ - Delete logistic collection
* `PATCH` ~~/api/v1/collections/logistic/{id4n}~~ - Update logistic collection
* `GET` ~~/api/v1/collections/logistic/{id4n}/elements~~ - List contents of the collection
* `POST` ~~/api/v1/collections/routing~~ - Create routing collecton
* `POST` ~~/api/v1/collections/routing/{collectionId4n}/elements~~ - Add element to routing collection
* `DELETE` ~~/api/v1/collections/routing/{collectionId4n}/elements~~ - Remove elements from routing collection
* `GET` ~~/api/v1/collections/routing/{id4n}~~ - Find routing collection
* `DELETE` ~~/api/v1/collections/routing/{id4n}~~ - Delete routing collection
* `PATCH` ~~/api/v1/collections/routing/{id4n}~~ - Update routing collection
* `GET` ~~/api/v1/collections/routing/{id4n}/elements~~ - List contents of the collection

### :wrench: Changed
---
* `GET` /api/v1/apikeys Find API key by organization  
  * Parameter `organizationId`not required :memo: The id of the organization to search in. -> The namespace of the organization to search in.
* `GET` /api/v1/changelog/organization/{organizationId}/ List change log entries of an organization  
  * Parameter `organizationId` :memo: Organization-ID of change log entries to be listed -> The namespace identifying the organization whose change log entries are to be listed
* `POST` /api/v1/guids Create GUID(s)  
  * Parameter `createGUIDInfo` :memo: createGUIDInfo -> GUID creation model
* `GET` /api/v1/guids/withoutCollection Retrieve GUIDs not in any collection  
  * Parameter `organizationId` :memo: Organization to search GUIDs for (required). -> The namespace of the organization to search GUIDs for
* `POST` /api/v1/organizations Create organization  
  * :heavy_plus_sign: Property `organization.namespace` - The namespace of the organization
  * :heavy_plus_sign: Property `namespace` - The namespace of the organization
* `PUT` /api/v1/organizations/{organizationId} Update organization  
  * :heavy_plus_sign: Parameter `organizationUpdate` - Updated organization object
  * Parameter `organizationId` :memo: The id of the organization to be updated. -> The namespace of the organization to be updated.
  * :x: Parameter ~~`organization`~~ - Updated organization object
  * :heavy_plus_sign: Property `namespace` - The namespace of the organization
* `DELETE` /api/v1/organizations/{organizationId} Delete organization  
  * Parameter `organizationId` :memo: The id of the organization to be deleted. -> The namespace of the organization to be deleted.
* `GET` /api/v1/organizations/{organizationId} Find organization by id/namespace  
  * Parameter `organizationId` :memo: The id of the organization to be retrieved. -> The namespace of the organization to be retrieved.
  * :heavy_plus_sign: Property `namespace` - The namespace of the organization
* `GET` /api/v1/organizations/{organizationId}/collections Get collections of organization  
  * Parameter `organizationId` :memo: organizationId -> The namespace of the organization
* `DELETE` /api/v1/organizations/{organizationId}/logo Delete organization logo  
  * Parameter `organizationId` :memo: The id of the organization where the logo should be deleted. -> The namespace of the organization where the logo should be deleted.
* `POST` /api/v1/organizations/{organizationId}/logo Update organization logo  
  * Parameter `organizationId` :memo: The id of the organization where the logo should be updated. -> The namespace of the organization where the logo should be updated.
* `POST` /api/v1/organizations/{organizationId}/users/invite Invite Users  
  * Parameter `organizationId` :memo: organizationId -> The namespace of the organization where users should be invited
* `DELETE` /api/v1/organizations/{organizationId}/users/{username}/roles Remove role(s) from user  
  * Parameter `organizationId` :memo: organizationId -> The namespace of the organization
* `POST` /api/v1/organizations/{organizationId}/users/{username}/roles Add role(s) to user  
  * Parameter `organizationId` :memo: organizationId -> The namespace of the organization
* `GET` /api/v1/organizations/{organizationId}/users/{username}/roles Get user roles by username  
  * Parameter `organizationId` :memo: organizationId -> The namespace of the organization
* `GET` /api/v1/public/organizations/{organizationId} Read public organization information  
  * :heavy_plus_sign: Property `namespace` - The namespace of the organization
* `GET` /whois/{id4n} Resolve owner of id4n  
  * :heavy_plus_sign: Property `organization.namespace` - The namespace of the organization

