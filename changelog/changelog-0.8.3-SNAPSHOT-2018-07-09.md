## Version 0.8.1 to 0.8.3-SNAPSHOT
---
### :sparkles: Added
---
* `GET` /api/v1/id4ns/{id4n}/alias - Get all aliases for the given GUID or Collection.
* `POST` /api/v1/id4ns/{id4n}/alias/{aliasType} - Add alias for GUID or Collection
* `DELETE` /api/v1/id4ns/{id4n}/alias/{aliasType} - Remove aliases from GUID or Collection

### :recycle: Removed
---
* `GET` ~~/api/v1/guids/{id4n}/alias~~ - Get all aliases for the given GUID.
* `POST` ~~/api/v1/guids/{id4n}/alias/{aliasType}~~ - Add alias for GUIDs
* `DELETE` ~~/api/v1/guids/{id4n}/alias/{aliasType}~~ - Remove aliases from GUIDs

### :wrench: Changed
---
