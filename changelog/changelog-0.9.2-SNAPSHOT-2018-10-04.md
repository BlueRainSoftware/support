## Version 0.9.1 to 0.9.2-SNAPSHOT
---
### :sparkles: Added
---

### :recycle: Removed
---

### :wrench: Changed
---
* `GET` /api/v1/history/{id4n} List history  
  * :heavy_plus_sign: Parameter `organization` - Show only entries created by one of the given organizations. This parameter can be used multiple times.
  * :heavy_plus_sign: Parameter `type` - Show only entries matching one of the given history item types. This parameter can be used multiple times.
  * :heavy_plus_sign: Parameter `qualifier` - Show only entries matching one of the given history item qualifiers (additional property de.id4i.history.item.qualifier). This parameter can be used multiple times.
  * :heavy_plus_sign: Parameter `fromDate` - From date time as UTC Date-Time format
  * :heavy_plus_sign: Parameter `toDate` - To date time as UTC Date-Time format
