# Technical 1

Remove key that have null or undefined value

## Input
```json
[
  {
    "session_name": "first test",
    "classes": [
      {
        "class_name": undefined,
        "students": [
          {
            "name": "Jhon"
          }
        ]
      }
    ]
  },
  {
    "session_name": null,
    "classes": [
      {
        "class_name": "second class", 
        "students": [
          {
            "student_name": "Doe"
          }
        ]
      }
    ]
  }
]
```

## Output

```json
[
  {
    "session_name": "first test",
    "classes": [
      {
        "students": [
          {
            "student_name": "John"
          }
        ]
      }
    ]
  },
  {
    "classes": [
      {
        "class_name": "second class",
        "students": [
          {
            "student_name": "Doe"
          }
        ]
      }
    ]
  }
]
```