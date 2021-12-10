# JWT

## Desc

- JWT is generate by HCAC algorithm
- JWT is create by three things :
  - JOSE Header: contains metadata about the type of token and
  - JWS Payload: user information
  - JWS Signature: signature to verify that the sender of the JWT

## JWT parts
- Identifies which algorithm is used to generate the signature

### Header
- The header consits of two part
  - alg: HS256
  - typ: JWT 


```
base64urlEncoding({
  "alg": "HS256",
  "typ": "JWT"
})
```

### Payload
- User information

```
base64urlEncoding({
  "loggedInAs": "admin",
  "iat": 1422779638
})
```

### Signature
- The signature is calculated by 
  - encoding the header using Base64url Encoding RFC 4648 
  - payload using Base64url Encoding RFC 4648 
  - concatenating the two together with a period separator
  
```
HMAC_SHA256(
  secret,
  base64urlEncoding(header) + '.' +
  base64urlEncoding(payload)
)
```


### Token is created 
- const token = base64urlEncoding(header) + '.' + base64urlEncoding(payload) + '.' + base64urlEncoding(signature)

## Workflow

- Backend generate JWT

## Questions

- Can you verfiy a token without storing into the database ? 
