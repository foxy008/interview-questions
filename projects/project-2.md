# Project 2

## Requirement
- NodeJs/Express
- Database PostgreSQL
- API Token menggunakan Bearer atau OAuth2
- Password encryption harus menggunakan bcrypt

## Soal
Membuat aplikasi RESTFUL API dengan fitur: 
- Login
- Insert Data
- Approve Data
- Get Data

## Keterangan
- Buatlah aplikasi RESTFUL API yang dapat melakukan Insert dan Get Data dalam format json.

- Disaat user melakukan insert ataupun get data, API harus melakukan validasi token terlebih
dahulu.

- Token didapatkan setelah user melakukan Login.

- Data user hanya boleh di-approve oleh supervisor nya sendiri.

- Data yang akan di-insert adalah data absensi.

- Setiap hari user melakukan 2 kali absensi (masuk dan pulang, menjadi 2 baris di database).

## Database

### Tabel users

| id          | name        | email         |npp             | npp_supervisor | password |
| ----------- | ----------- | ------------  | -------------- | -------------- | -------- |
| 1           | Udin        | udin@mail.com | 1234           | 1111           | password |
| 2           | Kosasih     | udin@mail.com | 5678           | 0000           | password |

### Table epresences

| id          | id_users    | type          |is_approve      | waktu          |
| ----------- | ----------- | ------------  | -------------- | -------------- |
| 1           | 1           | IN            | TRUE           | 16/10/20 08:00 |
| 2           | 1           | OUT           | FALSE          | 16/10/20 17:00 |


## Insert Data
```json
{
	"type": "IN",
	"waktu": "2020-16-10 08:00:00"
}
```

## Get Data Response
```json
{
  "message": "success get data",
  "data": [
    {
      "id_user": 1,
      "nama_user": "Udin",
      "tanggal": "2020-10-16",
      "waktu_masuk": "08:00:00",
      "waktu_pulang": "17:00:00",
      "status_masuk": "APPROVED",
      "status_pulang": "REJECTED"
    },
    {
      "id_user": 2,
      "nama_user": "Kosasih",
      "tanggal": "2020-10-16",
      "waktu_masuk": "08:00:00",
      "waktu_pulang": "17:00:00",
      "status_masuk": "APPROVED",
      "status_pulang": "APPROVED"
    }
  ]
}
```
### Keterangan
1. data absensi dibuat menjadi satu baris dari dua baris data di database
2. nama_user diambil dari tabel users
3. tanggal diambil dari field type = IN
4. waktu_masuk diambil dari field waktu dengan type = IN
5. waktu_pulang diambil dari field wakttu dengan type = OUT
6. status_masuk diambil dari field is_approve, true = APPROVE || false REJECT
7. status_pulang diambil dari field is_approve