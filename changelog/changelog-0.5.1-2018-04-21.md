## Version 0.4.0 to 0.5.1
---
### :sparkles: Added
---
* `GET` /account/contractRequired - Tells you whether your company needs to have a contract with BlueRain to be able to sign up
* `GET` /api/v1/history/{id4n} - List history
* `POST` /api/v1/history/{id4n} - Add history item
* `GET` /api/v1/history/{id4n}/{organizationId} - List history
* `GET` /api/v1/history/{id4n}/{organizationId}/{sequenceId} - List history
* `PATCH` /api/v1/history/{id4n}/{organizationId}/{sequenceId} - Update history item
* `PUT` /api/v1/history/{id4n}/{organizationId}/{sequenceId}/visibility - Set history item visibility
* `GET` /api/v1/public/history/{id4n} - Shows the public history of the given GUID
* `GET` /api/v1/public/organizations/{organizationId} - Read public organization information

### :recycle: Removed
---
* `PUT` ~~/api/v1/guids/{id4n}~~ - Change GUID information.

### :wrench: Changed
---
* `PATCH` /api/v1/collections/labelled/{id4n} Update labelled collection  
  * :heavy_plus_sign: Property `request.physicalState` - Physical attachment state of the collection
* `GET` /api/v1/collections/labelled/{id4n} Find labelled collection  
  * :heavy_plus_sign: Property `physicalState` - Physical attachment state of the collection
* `PATCH` /api/v1/collections/logistic/{id4n} Update logistic collection  
  * :heavy_plus_sign: Property `request.physicalState` - Physical attachment state of the collection
* `GET` /api/v1/collections/logistic/{id4n} Find logistic collection  
  * :heavy_plus_sign: Property `physicalState` - Physical attachment state of the collection
* `PATCH` /api/v1/collections/routing/{id4n} Update routing collection  
  * :heavy_plus_sign: Property `request.physicalState` - Physical attachment state of the collection
* `GET` /api/v1/collections/routing/{id4n} Find routing collection  
  * :heavy_plus_sign: Property `physicalState` - Physical attachment state of the collection
* `PATCH` /api/v1/collections/{id4n} Update collection  
  * :heavy_plus_sign: Property `request.physicalState` - Physical attachment state of the collection
* `GET` /api/v1/collections/{id4n} Find collection  
  * :heavy_plus_sign: Property `physicalState` - Physical attachment state of the collection
* `PATCH` /api/v1/guids/{id4n} Change GUID information.  
  * :heavy_plus_sign: Property `request.physicalState` - Physical attachment state of the GUID
* `GET` /api/v1/guids/{id4n} Retrieve GUID information  
  * :heavy_plus_sign: Property `physicalState` - Physical attachment state of the GUID
* `GET` /api/v1/info Retrieve version information about ID4i  
  * :heavy_plus_sign: Property `productionMode`
* `GET` /api/v1/users Find users  
  * Parameter `usernamePrefix`not required :memo: Find users starting with this prefix. -> null

