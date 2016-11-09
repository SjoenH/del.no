# API

## Requests

### **GET** - /api/auth/confirm_account/:confirmation_string

#### CURL

```sh
curl -X GET "http://it2810-02.idi.ntnu.no:2000/api/auth/confirm_account/:confirmation_string" \
    -H "Content-Type: application/x-www-form-urlencoded" \
    --data-raw "email"="mariusomoe@gmail.com" \
    --data-raw "password"="test" \
    --data-raw "firstName"="Lars" \
    --data-raw "lastName"="skaugvoll"
```

#### Header Parameters

- **Content-Type** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "application/x-www-form-urlencoded"
  ],
  "default": "application/x-www-form-urlencoded"
}
```

#### Body Parameters

- **email** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "mariusomoe@gmail.com"
  ],
  "default": "mariusomoe@gmail.com"
}
```
- **password** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "test"
  ],
  "default": "test"
}
```
- **firstName** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "Lars"
  ],
  "default": "Lars"
}
```
- **lastName** should respect the following schema:

```
{
  "type": "string",
  "enum": [
    "skaugvoll"
  ],
  "default": "skaugvoll"
}
```

## References

