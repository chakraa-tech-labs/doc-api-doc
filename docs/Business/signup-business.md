# Sign Up Business
If the above error response is received, the client should prompt for completing the sign-up, asking for mandatory information, and then make the following request to complete the sign-up.

- **Method:** POST  
- **Endpoint:** `/setup/business`  
- **Body:** Business object.  
- **Response:** Business object.  
  
The currently logged-in user will be considered the super admin of the signing-up business.