# jmeter-azure-authentication
The article helps to generate an OAuth 2.0 token in Java using a Client ID, Client Secret, and Tenant ID, you can use the Microsoft Identity Platform (Azure AD) to authenticate your application and obtain a token and work with API

# barier token generation
A bearer token helps to get access to app when it's configured in APP. The official documentation is https://learn.microsoft.com/en-us/azure/active-directory/develop/v2-oauth2-client-creds-grant-flow#first-case-access-token-request-with-a-shared-secret
The example of the curl 
```
curl -X POST -H "Content-Type: application/x-www-form-urlencoded" -d 'client_id={your_id}&scope=https%3A%2F%2Fgraph.microsoft.com%2F.default&client_secret={your_secret}&grant_type=client_credentials' 'https://login.microsoftonline.com/{your_tenant}/oauth2/v2.0/token'
```
So there is no sense in creating some libs, you can get access using the post above.
