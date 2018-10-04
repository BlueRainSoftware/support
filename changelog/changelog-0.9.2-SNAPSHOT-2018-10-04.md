## Version 0.9.1 to 0.9.2-SNAPSHOT
---
### :sparkles: Added
---

### :recycle: Removed
---

### :wrench: Changed
---
* `GET` /api/v1/history/{id4n} List history  
  * :heavy_plus_sign: Parameter `organization` - Show only entries created by the given organization
  * :heavy_plus_sign: Parameter `type` - Show only entries matching the given history item type
  * :heavy_plus_sign: Parameter `qualifier` - Show only entries matching the given history item qualifier (additional property de.id4i.history.item.qualifier)
  * :heavy_plus_sign: Parameter `fromDate` - From date time as UTC Date-Time format
  * :heavy_plus_sign: Parameter `toDate` - To date time as UTC Date-Time format
