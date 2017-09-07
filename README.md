## Create New Event

### API Endpoint:
```
POST /v1/events
```

### Parameters
|           Name         |          Description           |   Required/Optional   |
|------------------------|--------------------------------|-----------------------|
|     event[name]        |          Name of Event         |     Optional
|     event[description] |       Description of Event     |     Optional   
|     event[location]    |        Location of Event       |     Optional     
|     event[start_date]  |Start Date of Event [yyyy-mm-dd]|     Optional     
|     event[end_date]    | End Date of Event [yyyy-mm-dd] |     Optional     



### Example Request

```shell
curl -X POST \
  http://localhost:3000/v1/events \
  -H 'auth_token: eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjoxLCJpYXQiOiIyMDE3LTA2LTE0IDA2OjU0OjM0IFVUQyJ9.M7pgzA4ktNVvuDFvKMqESJfHmLQCobp0WNjC6k2Kjac' \
  -H 'cache-control: no-cache' \
  -H 'content-type: multipart/form-data; boundary=----WebKitFormBoundary7MA4YWxkTrZu0gW' \
  -H 'postman-token: 92a3e27f-0d0c-7e8a-2e4a-b24f2ae47009' \
  -F 'event[name]=Punjab Event' \
  -F 'event[description]=This is .......' \
```

### Response
```json
{
    "success": true,
    "message": "Event created successfully",
    "data": {
        "id": 29,
        "name": "Punjab Event",
        "description": "This is .......",
        "location": null,
        "start_date": null,
        "end_date": null,
        "duration": "",
        "status": "draft",
        "deleted": false,
        "created_at": "2017-09-07T11:55:04.000Z",
        "updated_at": "2017-09-07T11:55:04.000Z"
    }
}
```



## Update Specific Event

### API Endpoint:
```
PUT /v1/events/<event-id>
```

### Parameters
|           Name         |          Description           |   Required/Optional   |
|------------------------|--------------------------------|-----------------------|
|     event[name]        |          Name of Event         |     Optional
|     event[description] |       Description of Event     |     Optional   
|     event[location]    |        Location of Event       |     Optional     
|     event[start_date]  |Start Date of Event [yyyy-mm-dd]|     Optional     
|     event[end_date]    | End Date of Event [yyyy-mm-dd] |     Optional     



### Example Request

```shell
curl -X PUT \
  http://localhost:3000/v1/events/1 \
  -H 'auth_token: eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjoxLCJpYXQiOiIyMDE3LTA2LTE0IDA2OjU0OjM0IFVUQyJ9.M7pgzA4ktNVvuDFvKMqESJfHmLQCobp0WNjC6k2Kjac' \
  -H 'cache-control: no-cache' \
  -H 'content-type: multipart/form-data; boundary=----WebKitFormBoundary7MA4YWxkTrZu0gW' \
  -H 'postman-token: 92a3e27f-0d0c-7e8a-2e4a-b24f2ae47009' \
  -F 'event[name]=Punjab Event' \
  -F 'event[description]=This is .......' \
```

### Response
```json
{
    "success": true,
    "message": "Event updated successfully",
    "data": {
        "id": 29,
        "name": "Punjab Event",
        "description": "This is .......",
        "location": null,
        "start_date": null,
        "end_date": null,
        "duration": "",
        "status": "draft",
        "deleted": false,
        "created_at": "2017-09-07T11:55:04.000Z",
        "updated_at": "2017-09-07T11:55:04.000Z"
    }
}
```


## Update Status of Event

### API Endpoint:
```
PUT /v1/events/<event-id>/status
```

### Parameters
|           Name         |            Description             |   Required/Optional   |
|------------------------|------------------------------------|-----------------------|
|     event[status]      | Status of Event (draft, published) |     Required
    
### Example Request

```shell
curl -X PUT \
  http://localhost:3000/v1/events/1/status \
  -H 'auth_token: eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjoxLCJpYXQiOiIyMDE3LTA2LTE0IDA2OjU0OjM0IFVUQyJ9.M7pgzA4ktNVvuDFvKMqESJfHmLQCobp0WNjC6k2Kjac' \
  -H 'cache-control: no-cache' \
  -H 'content-type: multipart/form-data; boundary=----WebKitFormBoundary7MA4YWxkTrZu0gW' \
  -H 'postman-token: 92a3e27f-0d0c-7e8a-2e4a-b24f2ae47009' \
  -F 'event[status]=published' \
```

### Response
```json
{
    "success": true,
    "message": "Event Status updated successfully",
    "data": {
        "id": 29,
        "name": "Punjab Event",
        "description": "This is .......",
        "location": null,
        "start_date": null,
        "end_date": null,
        "duration": "",
        "status": "published",
        "deleted": false,
        "created_at": "2017-09-07T11:55:04.000Z",
        "updated_at": "2017-09-07T11:55:04.000Z"
    }
}
```


## Delete Specific Event

### API Endpoint:
```
DELETE /v1/events/<event-id>
```

### Example Request

```shell
curl -X DELETE \
  http://localhost:3000/v1/events/1 \
  -H 'auth_token: eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjoxLCJpYXQiOiIyMDE3LTA2LTE0IDA2OjU0OjM0IFVUQyJ9.M7pgzA4ktNVvuDFvKMqESJfHmLQCobp0WNjC6k2Kjac' \
  -H 'cache-control: no-cache' \
  -H 'content-type: multipart/form-data; boundary=----WebKitFormBoundary7MA4YWxkTrZu0gW' \
  -H 'postman-token: 92a3e27f-0d0c-7e8a-2e4a-b24f2ae47009' \
```

### Response
```json
{
    "success": true,
    "message": "Event deleted successfully",
    "data": {
        "id": 29,
        "name": "Punjab Event",
        "description": "This is .......",
        "location": null,
        "start_date": null,
        "end_date": null,
        "duration": "",
        "status": "published",
        "deleted": true,
        "created_at": "2017-09-07T11:55:04.000Z",
        "updated_at": "2017-09-07T11:55:04.000Z"
    }
}
```

