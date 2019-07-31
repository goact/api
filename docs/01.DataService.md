# SAIL DATASERVICE API

## Auth
### **POST** emotion POST Research Auth
[https://saildata.goact.co/api/research/authenticate]()

#### Headers
x-access-token

Content-Type
application/x-www-form-urlencoded

#### Body
**urlencoded**

username

password

```
curl --location --request POST "https://saildata.goact.co/api/research/authenticate" \
  --header "Content-Type: application/x-www-form-urlencoded" \
  --data "username=[username]&password=[password]"
```

## User Tokens
### **GET** user tokens
[https://saildata.goact.co/api/tokens]()

#### Headers
x-access-token

Content-Type
application/x-www-form-urlencoded

```
curl --location --request GET "https://saildata.goact.co/api/tokens" \
  --header "x-access-token: [insert token here] \
  --header "Content-Type: application/x-www-form-urlencoded" \
```

### **Get** user tokens by date range
[https://saildata.goact.co/api/tokens/active?start=2019-05-14&end=2019-06-30]()

#### Headers
x-access-token

Content-Type
application/x-www-form-urlencoded

#### Params
start - eg 2019-05-14

end	- eg 2019-06-30

```
curl --location --request GET "https://saildata.goact.co/api/tokens/active?start=2019-05-14&end=2019-06-30" \
  --header "x-access-token: [insert token here]" \
  --header "Content-Type: application/x-www-form-urlencoded"
```

## Data
### GET emotion GET data
[https://saildata.goact.co/api/data?start=2019-05-8&end=2019-05-11]()

#### Headers
x-access-token

Content-Type
application/x-www-form-urlencoded

#### Params
start - eg 2019-05-14

end	- eg 2019-06-30

```
curl --location --request GET "https://saildata.goact.co/api/data?start=2019-05-8&end=2019-05-11" \
  --header "x-access-token: [insert token here]" \
  --header "Content-Type: application/x-www-form-urlencoded" \
```

### GET emotion GET data by app_tokens
[https://saildata.goact.co/api/data/app_tokens]()

#### Headers
x-access-token

#### Body
**raw (application/json)**
````
{
    "app_tokens": [
        "1YotnFZsEjr1zCsicMWpAAFSa",
        "ZY2taFvsEjr1zCsicAlcTSEUs"
    ]
}
````

```
curl --location --request GET "https://saildata.goact.co/api/data/app_tokens" \
  --header "x-access-token: [insert token here]" \
  --header "Content-Type: application/json" \
  --data "{
    \"app_tokens\": [
        \"1YotnFZsEjr1zCsicMWpAAFSa\",
        \"ZY2taFvsEjr1zCsicAlcTSEUs\"
    ]
}"
```

### GET emotion GET data by user
[https://saildata.goact.co/api/data/user/f0626324-c0bb-4f1a-b20e-983e6b6fc808?start=2019-03-26&end=2019-03-27]()

#### Headers
x-access-token

#### Params
start - eg 2019-05-14

end	- eg 2019-06-30

```
curl --location --request GET "https://saildata.goact.co/api/data/user/f0626324-c0bb-4f1a-b20e-983e6b6fc808?start=2019-03-26&end=2019-03-27" \
  --header "x-access-token: [insert token here]" \
  --header "Content-Type: application/json" \
```
