# Evolve IP Project

## Goals

### Enhance IDP Project with Passport script for SAML Authentication

We need to redirect user to IDP (Where user is coming from) before user is authenticated.

Required flow of request from user:
- User requested to SP
- SP redirect user to gluu for login with request IDP encoded in base64 in state param
- Gluu extract state param and prepare request and endpoint to send request to IDP 
	- Get required info(if required) from state
        - extract endpoint of IDP
	- Prepare request to send user on IDP
	- Redirect User to IDP
- After validating user from IDP its redirected back to SP.

The Image below show the Flow of Passport SAML Authentication

![alt text](screen.png "IDP SAML Authentication Flow")
