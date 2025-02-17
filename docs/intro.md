---
sidebar_position: 1
id: intro
title: Introduction to Chatzeal
sidebar_label: Overview
---
# Chatzeal API Documentation

## Introduction
Chatzeal is an omni-channel chat platform for businesses to connect with customers across chatting channels like WhatsApp, Instagram, website, mobile app, etc.

## Request URL
All URL endpoints are of Catalyst functions, and hence all the below endpoints should be prefixed with `/server`.

For example, to get contacts, the URL will be:
```
https://chatrail-839016960.development.catalystserverless.com/server/contacts/
```

## Common Properties
All objects will have the following properties, even if not explicitly mentioned in the respective Object Models.

```json
{
  "id": "20923000000050314", // ID of the record
  "created_by": {
    "id": "2092300000000500" // User ID
  },
  "created_time": "2024-03-31 10:25:10:810",
  "modified_by": {
    "id": "2092300000000500" // User ID
  },
  "modified_time": "2024-03-31 10:25:10:810"
}
```

## Common Errors
Below are the errors that can occur in any of the APIs, in addition to specific error cases mentioned for individual APIs.

### Internal Server Error
- **Status Code:** 500
```json
{
  "status": "error",
  "code": "INTERNAL_ERROR",
  "message": "Internal error."
}
```

### Unauthorized
Occurs when the user is not permitted to perform an operation.
- **Status Code:** 400
```json
{
  "status": "error",
  "code": "UNAUTHORIZED",
  "message": "This user is not permitted to do this operation."
}
```

## Create/Update API Common Errors

### Body Missing
Occurs when the request body is missing.
- **Status Code:** 400
```json
{
  "status": "error",
  "message": "Missing data.",
  "code": "MISSING_DATA"
}
```

### Mandatory Field Missing
Occurs when a required field is missing or set to null in create or edit APIs.
- **Status Code:** 400
```json
{
  "status": "error",
  "message": "Mandatory field missing.",
  "code": "MISSING_MANDATORY_FIELD",
  "key": "name"
}
```

### Invalid Field Value
Occurs when some field value is invalid.
- **Status Code:** 400
```json
{
  "status": "error",
  "code": "INVALID_DATA",
  "message": "Invalid value",
  "key": "field_name"
}
```

If multiple levels of properties are present, the `key` value will represent the field from the root property. Example:
```
"content.buttons.0.params.0.name"
```
where the numbers indicate the index of the array value set for those properties.

## Get List of Records Common Errors

### No Records Found
Occurs when no records are found.
- **Status Code:** 204
- Response Body: Empty

## Update/Delete/Get Single Record Common Errors

### Invalid ID
Occurs when the provided ID is invalid.
- **Status Code:** 400
```json
{
  "status": "error",
  "code": "INVALID_ID",
  "message": "{module_name} id is invalid."
}
```

## File API Common Errors

### File Size Limit Exceeded
Occurs when the uploaded file exceeds the size limit.
- **Status Code:** 400
```json
{
  "status": "error",
  "code": "LIMIT_FILE_SIZE",
  "message": "File too large."
}
```

### Invalid File
Occurs when the uploaded file is invalid.
- **Status Code:** 400
```json
{
  "status": "error",
  "code": "INVALID_DATA",
  "message": "Invalid file.",
  "key": "file"
}
