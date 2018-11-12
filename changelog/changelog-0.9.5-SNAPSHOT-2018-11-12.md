## Version 0.9.3 to 0.9.5-SNAPSHOT
---
### :sparkles: Added
---

### :recycle: Removed
---
* `GET` ~~/api/v1/transfers/{id4n}/receiveInfo~~ - Show transfer information

### :wrench: Changed
---
* `PUT` /account/password Verify password reset  
* `POST` /account/password Request password reset  
* `PUT` /account/registration Complete registration  
* `POST` /account/registration Register user  
* `POST` /account/verification Verify registration  
* `GET` /api/v1/apikeys Find API key by organization  
* `POST` /api/v1/apikeys Create API key  
* `GET` /api/v1/apikeys/privileges List all privileges  
* `PUT` /api/v1/apikeys/{key} Update API keys  
* `DELETE` /api/v1/apikeys/{key} Delete API key  
* `GET` /api/v1/apikeys/{key} Show API key  
* `DELETE` /api/v1/apikeys/{key}/privileges Remove privilege  
* `GET` /api/v1/apikeys/{key}/privileges List privileges  
* `POST` /api/v1/apikeys/{key}/privileges Add privilege  
* `DELETE` /api/v1/apikeys/{key}/privileges/{privilege}/id4ns Remove id4ns of a privilege  
* `GET` /api/v1/apikeys/{key}/privileges/{privilege}/id4ns ID4ns of a privilege  
* `POST` /api/v1/apikeys/{key}/privileges/{privilege}/id4ns Add ID4ns of a privilege  
* `GET` /api/v1/billing/{organizationId} Get billing amount of services for a given organization  
* `GET` /api/v1/billing/{organizationId}/positions Get billing positions for a given organization  
* `GET` /api/v1/changelog/organization/{organizationId}/ List change log entries of an organization  
* `POST` /api/v1/collections Create collection  
* `DELETE` /api/v1/collections/{id4n} Delete collection  
* `GET` /api/v1/collections/{id4n} Find collection  
* `PATCH` /api/v1/collections/{id4n} Update collection  
* `DELETE` /api/v1/collections/{id4n}/elements Remove elements from collection  
* `GET` /api/v1/collections/{id4n}/elements List contents of the collection  
* `POST` /api/v1/collections/{id4n}/elements Add elements to collection  
* `GET` /api/v1/countries List countries  
* `GET` /api/v1/documents/{id4n} List documents  
* `PUT` /api/v1/documents/{id4n}/{organizationId} Create an empty document for an id4n  
* `GET` /api/v1/documents/{id4n}/{organizationId} List organization specific documents  
* `DELETE` /api/v1/documents/{id4n}/{organizationId}/{fileName} Delete a document  
* `GET` /api/v1/documents/{id4n}/{organizationId}/{fileName} Read document contents  
* `GET` /api/v1/documents/{id4n}/{organizationId}/{fileName}/metadata Retrieve a document (meta-data only, no content)  
* `PATCH` /api/v1/documents/{id4n}/{organizationId}/{fileName}/metadata Update a document  
* `POST` /api/v1/guids Create GUID(s)  
* `GET` /api/v1/guids/withoutCollection Retrieve GUIDs not in any collection  
* `GET` /api/v1/guids/{id4n} Retrieve GUID information  
* `PATCH` /api/v1/guids/{id4n} Change GUID information.  
* `GET` /api/v1/history/{id4n} List history  
* `POST` /api/v1/history/{id4n} Add history item  
* `GET` /api/v1/history/{id4n}/{organizationId}/{sequenceId} Get history item  
* `PATCH` /api/v1/history/{id4n}/{organizationId}/{sequenceId} Update history item  
* `PUT` /api/v1/history/{id4n}/{organizationId}/{sequenceId}/visibility Set history item visibility  
* `GET` /api/v1/id4ns/{id4n} Retrieve ID4n information  
* `GET` /api/v1/id4ns/{id4n}/alias Get all aliases for the given GUID or Collection.  
* `DELETE` /api/v1/id4ns/{id4n}/alias/{aliasType} Remove aliases from GUID or Collection  
* `POST` /api/v1/id4ns/{id4n}/alias/{aliasType} Add alias for GUID or Collection  
* `GET` /api/v1/id4ns/{id4n}/collections Retrieve collections of an ID  
* `GET` /api/v1/info Retrieve version information about ID4i  
* `PUT` /api/v1/microstorage/{id4n}/{organization} Write data to microstorage  
* `GET` /api/v1/microstorage/{id4n}/{organization} Read data from microstorage  
* `POST` /api/v1/organizations Create organization  
* `PUT` /api/v1/organizations/{organizationId} Update organization  
* `DELETE` /api/v1/organizations/{organizationId} Delete organization  
* `GET` /api/v1/organizations/{organizationId} Find organization by id/namespace  
* `PUT` /api/v1/organizations/{organizationId}/addresses/billing Store billing address  
* `DELETE` /api/v1/organizations/{organizationId}/addresses/billing Remove billing address  
* `GET` /api/v1/organizations/{organizationId}/addresses/billing Retrieve billing address  
* `PUT` /api/v1/organizations/{organizationId}/addresses/default Store address  
* `GET` /api/v1/organizations/{organizationId}/addresses/default Retrieve address  
* `GET` /api/v1/organizations/{organizationId}/collections Get collections of organization  
* `DELETE` /api/v1/organizations/{organizationId}/logo Delete organization logo  
* `POST` /api/v1/organizations/{organizationId}/logo Update organization logo  
* `PUT` /api/v1/organizations/{organizationId}/partner Add partner  
* `DELETE` /api/v1/organizations/{organizationId}/partner Remove partner  
* `GET` /api/v1/organizations/{organizationId}/partner Get partners of an organization  
* `GET` /api/v1/organizations/{organizationId}/privileges List my privileges  
* `GET` /api/v1/organizations/{organizationId}/roles List users and their roles  
* `GET` /api/v1/organizations/{organizationId}/users Find users in organization  
* `POST` /api/v1/organizations/{organizationId}/users/invite Invite Users  
* `DELETE` /api/v1/organizations/{organizationId}/users/{username}/roles Remove role(s) from user  
* `GET` /api/v1/organizations/{organizationId}/users/{username}/roles Get user roles by username  
* `POST` /api/v1/organizations/{organizationId}/users/{username}/roles Add role(s) to user  
* `GET` /api/v1/public/documents/{id4n} List public documents  
* `GET` /api/v1/public/documents/{id4n}/{organizationId}/{fileName} Read public document contents  
* `GET` /api/v1/public/documents/{id4n}/{organizationId}/{fileName}/metadata Retrieve a public document (meta-data only, no content)  
* `GET` /api/v1/public/history/{id4n} Shows the public history of the given GUID  
* `GET` /api/v1/public/image/{imageID} Resolve image  
* `GET` /api/v1/public/organizations/{organizationId} Read public organization information  
* `GET` /api/v1/public/routes/{id4n} Retrieve all public routes for a GUID  
* `GET` /api/v1/roles List roles  
* `PUT` /api/v1/routingfiles/{id4n} Store routing file  
* `GET` /api/v1/routingfiles/{id4n} Retrieve routing file  
* `GET` /api/v1/routingfiles/{id4n}/route/{type} Retrieve current route of a GUID (or ID4N)  
* `GET` /api/v1/routingfiles/{id4n}/routes/{type} Retrieve all routes of a GUID (or ID4N)  
* `GET` /api/v1/search/guids Search for GUIDs by alias  
* `GET` /api/v1/search/guids/aliases/types List all supported alias types  
* `PUT` /api/v1/transfers/{id4n}/receiveInfo Transfer a GUID or collection, obtaining it (i.e. becoming the holder) and if allowed also taking ownership  
  * :heavy_plus_sign: Property `request.organizationId` - Organization to take the ownership of the ID. If the sender chose to keep the ownership, this organization becomes the holder. Otherwise, it becomes the new owner.
  * :x: Property `request.holderOrganizationId` - The current holder of the object
  * :x: Property `request.keepOwnership` - Keep the public ownership while transferring the object
  * :x: Property `request.openForClaims` - Anyone who knows (or can scan) the ID4N can claim ownership of this object
  * :x: Property `request.ownerOrganizationId` - The current publicly visible owner of the object
  * :x: Property `request.recipientOrganizationIds` - Allow only these organizations to obtain this object
* `PUT` /api/v1/transfers/{id4n}/sendInfo Prepare an object for transfer  
* `GET` /api/v1/transfers/{id4n}/sendInfo Show transfer preparation information  
* `GET` /api/v1/user/organizations Retrieve organizations of user  
* `GET` /api/v1/users Find users  
  * Parameter `usernamePrefix`required :memo: null -> Find users starting with this prefix.
* `GET` /api/v1/users/{username} Find by username  
* `GET` /go/{guid} Forward  
* `GET` /whois/{id4n} Resolve owner of id4n  
