## Version 0.9.3 to 0.9.4-SNAPSHOT
---
### :sparkles: Added
---

### :recycle: Removed
---
* `GET` ~~/api/v1/transfers/{id4n}/receiveInfo~~ - Show transfer information

### :wrench: Changed
---
* `PUT` /api/v1/transfers/{id4n}/receiveInfo Transfer a GUID or collection, obtaining it (i.e. becoming the holder) and if allowed also taking ownership  
  * :heavy_plus_sign: Property `request.organizationId` - Organization to take the ownership of the ID. If the sender chose to keep the ownership, this organization becomes the holder. Otherwise, it becomes the new owner.
  * :x: Property `request.holderOrganizationId` - The current holder of the object
  * :x: Property `request.keepOwnership` - Keep the public ownership while transferring the object
  * :x: Property `request.openForClaims` - Anyone who knows (or can scan) the ID4N can claim ownership of this object
  * :x: Property `request.ownerOrganizationId` - The current publicly visible owner of the object
  * :x: Property `request.recipientOrganizationIds` - Allow only these organizations to obtain this object
