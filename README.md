# User And Post

Repository ini adalah repository yang berisi model User dan Post, dimana user dapat melakukan banyak post.

# Method yang ada pada post

| Endpoint        | Fungsi           |
| ------------- |-------------|
| GET /posts      | Melakukan list semua post yang ada |
| POST /posts     | Membuat post baru |
| GET /posts/{id} | Mendapatkan post dengan {id} tertentu |
| PUT /posts/{id}      | Melakukan update suatu post berdasarkan {id} post |
| DELETE /posts/{id}    | Menghapus post dengan {id} tertentu |
| GET /posts/{id}/exists  | Mengecek apakah post dengan {id} tertentu ada di database |
| GET /posts/count | Menghitung jumlah semua posts |

# Method yang ada pada user

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


