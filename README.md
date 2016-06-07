# User And Post

Repository ini adalah repository yang berisi model User dan Post, dimana user dapat melakukan banyak post.

## Method yang ada pada post

| Endpoint        | Fungsi           |
| ------------- |-------------|
| GET /posts      | Melakukan list semua post yang ada |

## Method yang ada pada user

| Endpoint        | Fungsi           |
| ------------- |-------------|
| GET /sosmedusers      | Melakukan list semua user yang terdaftar |
| POST /sosmedusers     | Membuat user baru |
| GET /sosmedusers/{id} | Mendapatkan user dengan {id} tertentu |
| PUT /sosmedusers/{id}      | Melakukan update suatu user berdasarkan {id} user |
| DELETE /sosmedusers/{id}    | Menghapus user dengan {id} tertentu |
| GET /sosmedusers/{id}/exists  | Mengecek apakah user dengan {id} tertentu ada di database |
| GET /sosmedusers/{id}/posts | Mendapatkan semua post dari user dengan {id} tertentu |
| POST /sosmedusers/{id}/posts | Membuat post untuk user dengan {id} tertentu |
| DELETE /sosmedusers/{id}/posts | Menghapus semua post dari user dengan {id} tertentu |
| GET /sosmedusers/{id}/posts/{fk} | Mendapatkan post dengan id = {fk} dari user dengan {id} tertentu |
| PUT /sosmedusers/{id}/posts/{fk} | Update post dengan id = {fk} dari user dengan {id} tertentu |
| DELETE /sosmedusers/{id}/posts/{fk} | Menghapus post dengan id = {fk} dari user dengan {id} tertentu |
| GET /sosmedusers/{id}/posts/count | Menghitung jumlah post dari user dengan {id} tertentu |
| GET /sosmedusers/count | Menghitung jumlah semua user |

## Testcase

### POST /sosmedusers
#### Request
```json
{
  "email": "akhfa@a.com",
  "password": "akhfa",
  "name": "akhfa",
  "address": "jalan X kel. Y",
  "telp": "08123456789"
}
```
#### Response
```json
{
  "email": "akhfa@a.com",
  "password": "akhfa",
  "name": "akhfa",
  "address": "jalan X kel. Y",
  "telp": "08123456789",
  "id": 1
}
```

### GET /sosmedusers
#### response
```json
[
  {
    "email": "akhfa@a.com",
    "password": "akhfa",
    "name": "akhfa",
    "address": "jalan X kel. Y",
    "telp": "08123456789",
    "id": 1
  }
]
```

### GET /sosmedusers/1
#### response
```json
{
  "email": "akhfa@a.com",
  "password": "akhfa",
  "name": "akhfa",
  "address": "jalan X kel. Y",
  "telp": "08123456789",
  "id": 1
}
```

### PUT /sosmedusers/1
#### request
```json
{
  "email": "akhfa@a.com",
  "password": "akhfa",
  "name": "akhfaBaru",
  "address": "jalan X kel. Y",
  "telp": "08123456789"
}
```
#### response
```json
{
  "email": "akhfa@a.com",
  "password": "akhfa",
  "name": "akhfaBaru",
  "address": "jalan X kel. Y",
  "telp": "08123456789",
  "id": 1
}
```

### GET /sosmedusers/1/exists
#### response
```json
{
  "exists": true
}
```

### GET /sosmedusers/2/exists
#### response
```json
{
  "exists": false
}
```

### GET /sosmedusers/count
#### response
```json
{
  "count": 1
}
```

### POST /sosmeduser/1/posts
#### request
```json
{
  "date": "2016-06-07",
  "text": "ini isi dari posting"
}
```
#### response
```json
{
  "date": "2016-06-07T00:00:00.000Z",
  "text": "ini isi dari posting",
  "id": 2,
  "sosmeduserId": 1
}
```

### GET /sosmedusers/1/posts/2 `1 adalah id user dan 2 adalah id post`
#### response
```json
{
  "date": "2016-06-07T00:00:00.000Z",
  "text": "ini isi dari posting",
  "id": 2,
  "sosmeduserId": 1
}
```

### PUT /sosmedusers/1/posts/2
#### request
```json
{
  "date": "2016-06-07",
  "text": "ini isi dari posting yang baru"
}
```
#### response
```json
{
  "date": "2016-06-07T00:00:00.000Z",
  "text": "ini isi dari posting yang baru",
  "id": 2,
  "sosmeduserId": 1
}
```

### GET /sosmedusers/1/posts/count
#### response
```json
{
  "count": 2
}
```

### GET /posts
#### response
```json
[
  {
    "date": "2016-06-07T00:00:00.000Z",
    "text": "string",
    "id": 1,
    "sosmeduserId": 1
  },
  {
    "date": "2016-06-07T00:00:00.000Z",
    "text": "ini isi dari posting yang baru",
    "id": 2,
    "sosmeduserId": 1
  }
]
```

### GET /posts/2
#### response
```json
{
  "date": "2016-06-07T00:00:00.000Z",
  "text": "ini isi dari posting yang baru",
  "id": 2,
  "sosmeduserId": 1
}
```
