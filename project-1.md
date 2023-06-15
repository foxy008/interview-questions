# Project 1

## Release 1

Make CRUD (Create, Read, Update, Delete) REST API with format Application/JSON using Express & MongoDB/Postgress Database for patient data in hospital.

patient fields:
- id
- name
- sex
- religion
- phone
- address
- nik

Response

```json
{
  "status" : "code", : 200, // berdasarkan http status yg di inginkan  https://en.wikipedia.org/wiki/List_of_HTTP_status_codes
  "response": "success", // fill this with success/ failed/error
  "message": "Exampe of success update data",
  "result" : {
// fill this with data if not showin. the data .lease let this bla,
}
```

## Release 2
Make form input / CRUD (front end) using **Vue.JS or React.JS:**

- List patient
- Detail patient
- Update patient
- Delete patient
- Add patient

## Notes
- Pay attention to clean code
- Make a good design
