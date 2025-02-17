---
id: get_business
title: Get Business
sidebar_label: Get Business
---
## Get Business
After the user signs up or logs in, the client should make this request to check if sign-up is proper.

- **Method:** GET  
- **Endpoint:** `/setup/business`  
- **Response:** Business object.

### Error Cases
- **When the sign-up is not complete** - 400
```json
{
  "status": "error",
  "code": "NOT_FOUND",
  "message": "No business found for user."
}
```