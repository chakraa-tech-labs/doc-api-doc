
# Common Errors
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
```
