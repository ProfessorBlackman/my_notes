1. User makes a request
2. Get access token from it
3. Validate token
4. Extract claims from it
5. Extract organizationId from requestURI
6. Compare with the one in the access token
7. If they match
8. access granted
9. else
10. access denied