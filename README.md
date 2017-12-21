# auth-server
Authentication server implementation serving various grant types

## Getting started
### 1) Clone the repository
```html
git clone https://github.com/dmcloughlin/auth-server.git
```

### 2) Start spring boot
``` ./mvnw spring-boot:run ``` on Mac/Linux

``` mvn spring-boot:run ``` on Windows

### 3) Configure Postman
Enter HTTP Basic Authentication credentials: (These represent client and secret)
```html
username: live-test
password: bG12ZS10ZXN0
```

### 4) Issue request for Token
Enter the following in the URL in Postman
```html
http://localhost:8080/oauth/token?grant_type=password&client_id=live-test&username=user&password=password
```

You should see something like the following:

```html
{
    "access_token": "00c7ccf6-85a8-47cf-9bdd-e9e08dc3609a",
    "token_type": "bearer",
    "expires_in": 3599,
    "scope": "webapp"
}
```








