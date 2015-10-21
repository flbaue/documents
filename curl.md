# curl

### 1) Request oAuth Token
``` bash
curl --data "grant_type=password&client_id=acme&username=user&password=password" https://acme:acmesecret@192.168.99.100:9999/uaa/oauth/token -k
```
Hint: Replace the IP address


The Response will look like this:
``` bash
{"access_token":"3e96698e-fc1e-4942-b355-7dacb05a8808",...
```
copy the access_token to use it for a request



### 2.1) Send a GET Request to a REST-URL
``` bash
curl --header "Authorization: Bearer {token}" https://192.168.99.100:8080/api/1
```
Hint: Replace {token} with the access_token and check the IP address


### 2.2) Send a POST Request to the REST-URL
``` bash
curl -H "Authorization: Bearer {token}" -H "Content-Type: application/json" -X POST -d '{"username":"xyz","password":"xyz"}' http://localhost:3000/api/login
```
Hint: use your access_token and modify the JSON string at the end
