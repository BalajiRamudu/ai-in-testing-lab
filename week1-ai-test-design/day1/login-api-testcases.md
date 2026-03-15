Login API Test Cases using AI

## Prompt Used

Generate all positive, negative, boundary and security test cases for a swagger API with id, title, dueDate and completed fields.
Request Body:
{
  "id": 5,
  "title": "Test",
  "dueDate": "2026-06-15T06:43:37.169Z",
  "completed": true
}
Source: https://fakerestapi.azurewebsites.net/index.html

---

## AI Generated Test Cases (Summary)

Positive:
- Valid request with all fields
- completed true/false
- future dueDate

Negative:
- Missing id
- Invalid dueDate format
- completed as string
- empty title

Boundary:
- id = 0
- very long title
- past dueDate

Security:
- SQL injection in title
- script injection
- large payload

---

## My Identified Missing Scenarios

- id as string ("five")
- id as null
- id with special characters
- mixed case title
- default date like 0001-01-01T00:00:01
- past due date validation

---

## Senior Added Scenarios

- duplicate id
- max integer id
- decimal id
- unicode title
- invalid date like 2026-02-30
- timezone issues
- completed = 1
