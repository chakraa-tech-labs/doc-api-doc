---
sidebar_position: 3
---
# Update Business
- **Method:** PUT  
- **Endpoint:** `/setup/business`  
- **Body:** Business object with only edit-supported fields. Any other field will be ignored.  
- **Response:** Result object for success & failure cases.

### Error Cases
- **Only an admin can update the properties of a business.** For others, an `UNAUTHORIZED` error will be thrown.
- **Only the current super admin can change the super admin of a business.** For others, an `UNAUTHORIZED` error will be thrown.