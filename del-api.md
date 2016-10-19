# GET /api/articles/all

+ Request (application/x-www-form-urlencoded)

    + Headers

            Authorization: JWT eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJfaWQiOiI1N2ZlM2E1M2NjOGFiNTExZGY4NzRkY2UiLCJmaXJzdE5hbWUiOiJNYXJpdXMiLCJsYXN0TmFtZSI6Ik1vZSIsImVtYWlsIjoibWFyaXVzb21vZUBnbWFpbC5jb20iLCJyb2xlIjoiTWVtYmVyIiwiaWF0IjoxNDc2Mjc5MDk3LCJleHAiOjE0NzYyODkxNzd9.PotadTqhhwSjh5zpZFrwZ6m8yFvlyPCvFGZJ9qHTT30

    + Body

            email=mariusomoe%40gmail.com&password=test&firstName=Lars&lastName=skaugvoll

+ Response 200 (application/json; charset=utf-8)

    + Headers

            Access-Control-Allow-Credentials: true
            X-Powered-By: Express
            Access-Control-Allow-Methods: PUT, GET, POST, DELETE, OPTIONS
            Access-Control-Allow-Headers: Origin, X-Requested-With, Content-Type, Accept, Authorization, Access-Control-Allow-Credentials
            Etag: W/"781-9WfAzT4ihxqUObeNsKS+dQ"

    + Body

            {
                "articles": [
                    {
                        "_id": "57fe3a54cc8ab511df874dd0",
                        "name": "Kaffetrakter",
                        "intro": "knallsterk kaffe",
                        "txt": "Kaffetrakter som er to eller tre år gammel. sort kaffe",
                        "price": 50,
                        "fromDate": "2016-10-12T13:27:48.552Z",
                        "toDate": "2016-10-12T13:27:48.552Z",
                        "__v": 0,
                        "active": true,
                        "tags": [
                            "iamatag",
                            "inventionfuel",
                            "styrkedrikk"
                        ],
                        "imgLink": [
                            "some/file/dir/yada/yada",
                            "super/img.img"
                        ]
                    },
                    {
                        "_id": "57fe3a54cc8ab511df874dd1",
                        "name": "støvsuger",
                        "intro": "Suger skikkelig",
                        "txt": "Støvsuger som er to eller tre år gammel. Liker ikke sokker",
                        "price": 50,
                        "fromDate": "2016-10-12T13:27:48.563Z",
                        "toDate": "2016-10-12T13:27:48.563Z",
                        "__v": 0,
                        "active": true,
                        "tags": [
                            "iamatag",
                            "støv",
                            "støvsuger"
                        ],
                        "imgLink": [
                            "some/file/dir",
                            "anoter/image.img"
                        ]
                    },
                    {
                        "_id": "57fe3a54cc8ab511df874dd2",
                        "name": "støvsuger",
                        "intro": "Suger skikkelig",
                        "txt": "Støvsuger som er to eller tre år gammel. Liker ikke sokker",
                        "price": 50,
                        "fromDate": "2016-10-12T13:27:48.565Z",
                        "toDate": "2016-10-12T13:27:48.565Z",
                        "__v": 0,
                        "active": true,
                        "tags": [
                            "iamatag",
                            "støv",
                            "støvsuger"
                        ],
                        "imgLink": [
                            "some/file/dir",
                            "anoter/image.img"
                        ]
                    }
                ]
            }


# POST /api/auth/register

+ Request (application/x-www-form-urlencoded)

        email=mariusomoe%40gmail.com&password=test&firstName=Lars&lastName=skaugvoll



# POST /api/auth/login

+ Request (application/x-www-form-urlencoded)

        email=mariusomoe%40gmail.com&password=test

+ Response 200 (application/json; charset=utf-8)

    + Headers

            Access-Control-Allow-Credentials: true
            X-Powered-By: Express
            Access-Control-Allow-Methods: PUT, GET, POST, DELETE, OPTIONS
            Access-Control-Allow-Headers: Origin, X-Requested-With, Content-Type, Accept, Authorization, Access-Control-Allow-Credentials
            Etag: W/"1f0-99TkJzM2P9363T0r5t6plQ"

    + Body

            {
                "token": "JWT eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJfaWQiOiI1N2ZlM2E1M2NjOGFiNTExZGY4NzRkY2UiLCJmaXJzdE5hbWUiOiJNYXJpdXMiLCJsYXN0TmFtZSI6Ik1vZSIsImVtYWlsIjoibWFyaXVzb21vZUBnbWFpbC5jb20iLCJyb2xlIjoiTWVtYmVyIiwiaWF0IjoxNDc2MjgwNDU5LCJleHAiOjE0NzYyOTA1Mzl9.BjaehLEonlVDXCKF1O_LqxBVY39mkenlyznuhlha5yo",
                "user": {
                    "_id": "57fe3a53cc8ab511df874dce",
                    "firstName": "Marius",
                    "lastName": "Moe",
                    "email": "mariusomoe@gmail.com",
                    "role": "Member"
                }
            }


# GET /api/auth/test_auth_route

+ Request (application/x-www-form-urlencoded)

        email=mariusomoe%40gmail.com&password=test&firstName=Lars&lastName=skaugvoll

+ Response 401

    + Headers

            Access-Control-Allow-Credentials: true
            X-Powered-By: Express
            Access-Control-Allow-Methods: PUT, GET, POST, DELETE, OPTIONS
            Access-Control-Allow-Headers: Origin, X-Requested-With, Content-Type, Accept, Authorization, Access-Control-Allow-Credentials

    + Body

            Unauthorized


# GET /api/auth/confirm_account/:confirmation_string

+ Request (application/x-www-form-urlencoded)

        email=mariusomoe%40gmail.com&password=test&firstName=Lars&lastName=skaugvoll

+ Response 400 (application/json; charset=utf-8)

    + Headers

            Access-Control-Allow-Credentials: true
            X-Powered-By: Express
            Access-Control-Allow-Methods: PUT, GET, POST, DELETE, OPTIONS
            Access-Control-Allow-Headers: Origin, X-Requested-With, Content-Type, Accept, Authorization, Access-Control-Allow-Credentials
            Etag: W/"3c-ZN12Yo9EDKhT2RrGMhNEaw"

    + Body

            {
                "message": "Could not find user",
                "status": 2011
            }


# POST /api/auth//request_new_email_confirmation

+ Request (application/x-www-form-urlencoded)

        mariusomoe@gmail.com



