## Version 0.7.2 to 0.8.0
---
### :sparkles: Added
---
* `GET` /api/v1/organizations/{organizationId}/partner - Get partners of an organization
* `PUT` /api/v1/organizations/{organizationId}/partner - Add partner
* `DELETE` /api/v1/organizations/{organizationId}/partner - Remove partner
* `GET` /api/v1/routingfiles/{id4n}/route/{type} - Retrieve current route of a GUID (or ID4N)

### :recycle: Removed
---
* `GET` ~~/api/v1/routingfiles/{id4n}/routes~~ - Retrieve all web routes

### :wrench: Changed
---
* `POST` /api/v1/history/{id4n} Add history item  
  * :heavy_plus_sign: Property `historyItem.additionalProperties` - History items custom additional properties
* `PATCH` /api/v1/history/{id4n}/{organizationId}/{sequenceId} Update history item  
  * :heavy_plus_sign: Property `additionalProperties` - History items custom additional properties
* `PUT` /api/v1/history/{id4n}/{organizationId}/{sequenceId}/visibility Set history item visibility  
  * :heavy_plus_sign: Property `additionalProperties` - History items custom additional properties
* `GET` /api/v1/public/routes/{id4n} Retrieve all public routes for a GUID  
  * :heavy_plus_sign: Parameter `type` - type
  * :heavy_plus_sign: Parameter `interpolate` - interpolate
* `GET` /api/v1/routingfiles/{id4n}/routes/{type} Retrieve all routes of a GUID (or ID4N)  
  * :heavy_plus_sign: Parameter `organizationId` - organizationId
  * :x: Parameter ~~`privateRoutes`~~ - privateRoutes
  * :x: Parameter ~~`publicRoutes`~~ - publicRoutes
* `GET` /api/v1/transfers/{id4n}/receiveInfo Show transfer information  
  * :heavy_plus_sign: Property `openForClaims` - Anyone who knows (or can scan) the ID4N can claim ownership of this object
  * :x: Property `nextScanOwnership` - Allow anyone which scans or knows the ID4N to obtain this object
* `PUT` /api/v1/transfers/{id4n}/receiveInfo Transfer a GUID or collection, obtaining it (i.e. becoming the holder) and if allowed also taking ownership  
  * :heavy_plus_sign: Property `request.openForClaims` - Anyone who knows (or can scan) the ID4N can claim ownership of this object
  * :x: Property `request.nextScanOwnership` - Allow anyone which scans or knows the ID4N to obtain this object
* `GET` /api/v1/transfers/{id4n}/sendInfo Show transfer preparation information  
  * :heavy_plus_sign: Property `openForClaims` - Allow anyone who knows (or can scan) the ID4N to claim ownership of this object
  * :x: Property `nextScanOwnership` - Allow anyone which scans or knows the ID4N to obtain this object
* `PUT` /api/v1/transfers/{id4n}/sendInfo Prepare an object for transfer  
  * :heavy_plus_sign: Property `request.openForClaims` - Allow anyone who knows (or can scan) the ID4N to claim ownership of this object
  * :x: Property `request.nextScanOwnership` - Allow anyone which scans or knows the ID4N to obtain this object
