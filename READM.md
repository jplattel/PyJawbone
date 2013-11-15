# PyJawbone

A simple wrapper for the Jawbone UP API.

## Usage

Import the library:

	from jawbone import JawboneAPI

Assign it to an object:

	j = JawboneAPI()

Generated an authentication URL with the scope:

	auth_url = j.getAuth(scope) 
	
Open auth URL and sign it, you will be redirected and given a auth code.

	access_token = j.getAccessToken(code)

Use the access token 

	j.apiCall(accesspoint, endpoint, other_params_as_a_dict)

If the response is succesfull, JSON will be return, otherwise it will return the error.


## Dependencies

This library has one dependency:

	requests