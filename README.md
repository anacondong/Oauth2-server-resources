
#### Oauth2-server-resources  ####

```
**** Init program ****
$cd identity-server
$mvn spring-boot:run

$cd resource-provider
$mvn spring-boot:run

```



```
***** how to run test ***
** Get access token from Auth server
### curl -XPOST -k client:secret@localhost:9000/sample/oauth/token -d grant_type=password -d client_id=client -d client_secret=abc123 -d username=user -d password=secret

*** access resources server by using access token
### curl -H "Authorization: Bearer 5bc788e4-6bee-42d2-ba85-446b847210f2" http://localhost:9001/resource/

*** refresh token for Auth server
### curl -XPOST -k client:secret@localhost:9000/sample/oauth/token -d grant_type=refresh_token -d refresh_token=6deda518-e523-4bc4-b307-ace507619c0c

```