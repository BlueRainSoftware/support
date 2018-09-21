## Version 0.9.0 to 0.9.1
---
### :sparkles: Added
---

### :recycle: Removed
---
* `GET` ~~/api/v1/public/documents/{id4n}/{organizationId}~~ - List organization specific documents

### :wrench: Changed
---
* `GET` /api/v1/documents/{id4n} List documents  
  * :heavy_plus_sign: Parameter `owner` - Filter by owner organization
* `GET` /api/v1/documents/{id4n}/{organizationId} List organization specific documents  
  * :heavy_plus_sign: Parameter `owner` - Filter by owner organization
* `PUT` /api/v1/documents/{id4n}/{organizationId} Create an empty document for an id4n  
  * :heavy_plus_sign: Property `ownerOrganizationId` - The organization's namespace which owns the document
* `PATCH` /api/v1/documents/{id4n}/{organizationId}/{fileName}/metadata Update a document  
  * :heavy_plus_sign: Property `ownerOrganizationId` - The organization's namespace which owns the document
* `GET` /api/v1/documents/{id4n}/{organizationId}/{fileName}/metadata Retrieve a document (meta-data only, no content)  
  * :heavy_plus_sign: Property `ownerOrganizationId` - The organization's namespace which owns the document
* `GET` /api/v1/public/documents/{id4n} List public documents  
  * :heavy_plus_sign: Parameter `owner` - Filter by owner organization
* `GET` /api/v1/public/documents/{id4n}/{organizationId}/{fileName}/metadata Retrieve a public document (meta-data only, no content)  
  * :heavy_plus_sign: Property `ownerOrganizationId` - The organization's namespace which owns the document
