## Version 0.9.6 to 0.9.7
---
### :sparkles: Added
---
* `GET` /api/v1/id4ns/{id4n}/properties - Retrieve ID4n properties
* `DELETE` /api/v1/id4ns/{id4n}/properties - Delete ID4n properties
* `PATCH` /api/v1/id4ns/{id4n}/properties - Patch ID4n properties
* `POST` /api/v1/documents/{id4n}/{organizationId} - Create an document for an id4n

### :recycle: Removed
---

### :wrench: Changed
---
* `GET` /api/v1/organizations/{organizationId}/collections Get collections of organization  
  * :heavy_plus_sign: Parameter `property` - List of i4dn property filter. e.g. "com.myorga.state:IN:waiting|processing" or "com.myorga.orderId:EQ:SAP001"
