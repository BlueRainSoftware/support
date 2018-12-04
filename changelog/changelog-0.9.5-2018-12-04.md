## Version 0.9.3 to 0.9.5
---
### :sparkles: Added
---

### :recycle: Removed
---
* `GET` ~~/api/v1/transfers/{id4n}/receiveInfo~~ - Show transfer information

### :wrench: Changed
---
* `DELETE` /api/v1/documents/{id4n}/{organizationId}/{fileName} Delete a document  
  * :x: Property `body`
  * :x: Property `statusCode`
  * :x: Property `statusCodeValue`
* `POST` /api/v1/history/{id4n} Add history item  
  * :heavy_plus_sign: Property `historyItem.ownerOrganizationId` - Owner of the history item
* `GET` /api/v1/history/{id4n}/{organizationId}/{sequenceId} Get history item  
  * :heavy_plus_sign: Property `additionalProperties` - History items custom additional properties
  * :heavy_plus_sign: Property `organizationId` - Originator of the history item
  * :heavy_plus_sign: Property `ownerOrganizationId` - Owner of the history item
  * :heavy_plus_sign: Property `sequenceId` - Forms the primary key of the history item together with the GUID and the organizationId
  * :heavy_plus_sign: Property `timestamp` - History item timestamp
  * :heavy_plus_sign: Property `type` - Type of the history item
  * :heavy_plus_sign: Property `visibility.public` - Document is publicly readable (if ID4N is owned by the same organization)
  * :heavy_plus_sign: Property `visibility.sharedOrganizationIds` - Document is readable by these organizations (independend of ID4N ownership)
  * :x: Property `elements`
  * :x: Property `limit` - The number of returned elements
  * :x: Property `offset` - Starting with the n-th element
  * :x: Property `total` - The total number of elements
* `PATCH` /api/v1/history/{id4n}/{organizationId}/{sequenceId} Update history item  
  * :heavy_plus_sign: Property `ownerOrganizationId` - Owner of the history item
* `PUT` /api/v1/history/{id4n}/{organizationId}/{sequenceId}/visibility Set history item visibility  
  * :heavy_plus_sign: Property `ownerOrganizationId` - Owner of the history item
* `PUT` /api/v1/transfers/{id4n}/receiveInfo Transfer a GUID or collection, obtaining it (i.e. becoming the holder) and if allowed also taking ownership  
  * :heavy_plus_sign: Property `request.organizationId` - Organization to take the ownership of the ID. If the sender chose to keep the ownership, this organization becomes the holder. Otherwise, it becomes the new owner.
  * :x: Property `request.holderOrganizationId` - The current holder of the object
  * :x: Property `request.keepOwnership` - Keep the public ownership while transferring the object
  * :x: Property `request.openForClaims` - Anyone who knows (or can scan) the ID4N can claim ownership of this object
  * :x: Property `request.ownerOrganizationId` - The current publicly visible owner of the object
  * :x: Property `request.recipientOrganizationIds` - Allow only these organizations to obtain this object
