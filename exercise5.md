1. GET ​/api​/v1​/Activities

https://fakerestapi.azurewebsites.net/api/v1/Activities

accept: text/plain; v=1.0

Code: 200
 
  {
    "id": 1,
    "title": "Activity 1",
    "dueDate": "2023-07-02T05:35:49.9627911+00:00",
    "completed": false
  },
  {
    "id": 2,
    "title": "Activity 2",
    "dueDate": "2023-07-02T06:35:49.9627933+00:00",
    "completed": true
  },
  {
    "id": 3,
    "title": "Activity 3",
    "dueDate": "2023-07-02T07:35:49.9627936+00:00",
    "completed": false

2. POST ​/api​/v1​/Activities

https://fakerestapi.azurewebsites.net/api/v1/Activities

"Content-Type: application/json; v=1.0"

Code: 200

{
  "id": 0,
  "title": "string",
  "dueDate": "2023-07-02T18:18:30.014Z",
  "completed": true
}

3. GET ​/api​/v1​/Activities​/1

https://fakerestapi.azurewebsites.net/api/v1/Activities/1

"accept: text/plain; v=1.0"

Code: 200

{
  "id": 1,
  "title": "Activity 1",
  "dueDate": "2023-07-02T19:20:44.3032649+00:00",
  "completed": false
}

4. GET ​/api​/v1​/Activities​/152

https://fakerestapi.azurewebsites.net/api/v1/Activities/152

"accept: text/plain; v=1.0"

Code: 404

{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
  "title": "Not Found",
  "status": 404,
  "traceId": "00-711937e91ffc4144b494254c234b5b45-b3bea7624ecf974d-00"
}

5. PUT ​/api​/v1​/Activities​/{id}

https://fakerestapi.azurewebsites.net/api/v1/Activities/1

"Content-Type: application/json; v=1.0"

{
  "id": 0,
  "title": "string",
  "dueDate": "2023-07-02T18:28:27.468Z",
  "completed": true
}

Code: 200

{
  "id": 0,
  "title": "string",
  "dueDate": "2023-07-02T18:28:27.468Z",
  "completed": true
}

6. PUT ​/api​/v1​/Activities​/{id}

https://fakerestapi.azurewebsites.net/api/v1/Activities/15324632463264236

"Content-Type: application/json; v=1.0"

{
  "id": 0,
  "title": "string",
  "dueDate": "2023-07-02T18:28:27.468Z",
  "completed": true
}

Code: 400

{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-0058a5f0c1d43c42bae7ff3527b32d64-1ffccea4480a5e45-00",
  "errors": {
    "id": [
      "The value '15324632463264236' is not valid."
    ]
  }
}

7. DELETE ​/api​/v1​/Activities​/{id}

https://fakerestapi.azurewebsites.net/api/v1/Activities/1

"accept: */*"

Code: 200
	
Success

8. DELETE ​/api​/v1​/Activities​/{id}

https://fakerestapi.azurewebsites.net/api/v1/Activities/5346236346326

"accept: */*"

Code: 400
	
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-ca3be8042f64944f9aebf03aec5ae364-17d6021235e85243-00",
  "errors": {
    "id": [
      "The value '5346236346326' is not valid."
    ]
  }
}

9. GET ​/api​/v1​/Authors

https://fakerestapi.azurewebsites.net/api/v1/Authors

"accept: text/plain; v=1.0"

Code: 200

[
  {
    "id": 1,
    "idBook": 1,
    "firstName": "First Name 1",
    "lastName": "Last Name 1"
  },
  {
    "id": 2,
    "idBook": 1,
    "firstName": "First Name 2",
    "lastName": "Last Name 2"
  },
  {
    "id": 3,
    "idBook": 1,
    "firstName": "First Name 3",
    "lastName": "Last Name 3"
  },
  {
    "id": 4,
    "idBook": 1,
    "firstName": "First Name 4",
    "lastName": "Last Name 4"
  },

10. POST ​/api​/v1​/Authors

https://fakerestapi.azurewebsites.net/api/v1/Authors

"Content-Type: application/json; v=1.0"

{
  "id": 0,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}

Code: 200

{
  "id": 0,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}

11. GET ​/api​/v1​/Authors​/authors​/books​/{idBook}

https://fakerestapi.azurewebsites.net/api/v1/Authors/authors/books/1

"accept: text/plain; v=1.0"

Code: 200

[
  {
    "id": 1,
    "idBook": 1,
    "firstName": "First Name 1",
    "lastName": "Last Name 1"
  },
  {
    "id": 2,
    "idBook": 1,
    "firstName": "First Name 2",
    "lastName": "Last Name 2"
  },
  {
    "id": 3,
    "idBook": 1,
    "firstName": "First Name 3",
    "lastName": "Last Name 3"
  },
  {
    "id": 4,
    "idBook": 1,
    "firstName": "First Name 4",
    "lastName": "Last Name 4"
  }
]

12. GET ​/api​/v1​/Authors​/authors​/books​/{idBook}

https://fakerestapi.azurewebsites.net/api/v1/Authors/authors/books/600456756325324

"accept: text/plain; v=1.0"

Code: 400

{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-221cb31a3b8b704fa36d039233a76bac-7caf8a925b3c9046-00",
  "errors": {
    "idBook": [
      "The value '600456756325324' is not valid."
    ]
  }
}

13. GET ​/api​/v1​/Authors​/{id}

https://fakerestapi.azurewebsites.net/api/v1/Authors/1

"accept: text/plain; v=1.0"

Code: 200

{
  "id": 1,
  "idBook": 1,
  "firstName": "First Name 1",
  "lastName": "Last Name 1"
}

14. GET ​/api​/v1​/Authors​/{id}

https://fakerestapi.azurewebsites.net/api/v1/Authors/76868686

"accept: text/plain; v=1.0"

Code: 404

{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
  "title": "Not Found",
  "status": 404,
  "traceId": "00-b0fddf5c0f5b9c4d9257f8872fd8ac63-eec5703b332e6a4c-00"
}

15. PUT ​/api​/v1​/Authors​/{id}

https://fakerestapi.azurewebsites.net/api/v1/Authors/1

"Content-Type: application/json; v=1.0"

{
  "id": 0,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}

Code: 200

{
  "id": 0,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}

16. PUT ​/api​/v1​/Authors​/{id}

https://fakerestapi.azurewebsites.net/api/v1/Authors/1645747457574

"Content-Type: application/json; v=1.0"

{
  "id": 0,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}

Code: 400

{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-ada033404558524db5d7987a41f7f485-26894fd912c5c443-00",
  "errors": {
    "id": [
      "The value '1645747457574' is not valid."
    ]
  }
}

17. DELETE ​/api​/v1​/Authors​/{id}

https://fakerestapi.azurewebsites.net/api/v1/Authors/1

"accept: */*"

Code: 200

Success

18. DELETE ​/api​/v1​/Authors​/{id}

https://fakerestapi.azurewebsites.net/api/v1/Authors/15437447457

"accept: */*"

Code: 400

{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-fd2fb13868a6bd4693d4a6b6c7c70074-9b5f2cd2f2cb8a46-00",
  "errors": {
    "id": [
      "The value '15437447457' is not valid."
    ]
  }
}

19. GET ​/api​/v1​/Books

https://fakerestapi.azurewebsites.net/api/v1/Books

"accept: text/plain; v=1.0"

Code: 200

[
  {
    "id": 1,
    "title": "Book 1",
    "description": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
    "pageCount": 100,
    "excerpt": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
    "publishDate": "2023-07-01T19:03:12.3138709+00:00"
  },
  {
    "id": 2,
    "title": "Book 2",
    "description": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
    "pageCount": 200,
    "excerpt": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
    "publishDate": "2023-06-30T19:03:12.3138845+00:00"
  },

20. POST ​/api​/v1​/Books

https://fakerestapi.azurewebsites.net/api/v1/Books

"Content-Type: application/json; v=1.0"

{
  "id": 0,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-07-02T19:11:46.178Z"
}

Code: 200

{
  "id": 0,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-07-02T19:11:46.178Z"
}

21. GET ​/api​/v1​/Books​/{id}

https://fakerestapi.azurewebsites.net/api/v1/Books/1

"accept: text/plain; v=1.0"

Code: 200

{
  "id": 1,
  "title": "Book 1",
  "description": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
  "pageCount": 100,
  "excerpt": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
  "publishDate": "2023-07-01T19:12:54.7765397+00:00"
}

22. GET ​/api​/v1​/Books​/{id}

https://fakerestapi.azurewebsites.net/api/v1/Books/1421342341

"accept: text/plain; v=1.0"

Code: 404

{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
  "title": "Not Found",
  "status": 404,
  "traceId": "00-65e77d6f55bcb94ab39c8c9aac3b51d9-41d6a65bc90bfc43-00"
}

23. PUT ​/api​/v1​/Books​/{id}

https://fakerestapi.azurewebsites.net/api/v1/Books/1

"Content-Type: application/json; v=1.0"

{
  "id": 0,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-07-02T19:14:26.245Z"
}

Code: 200

{
  "id": 0,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-07-02T19:14:26.245Z"
}

24. PUT ​/api​/v1​/Books​/{id}

https://fakerestapi.azurewebsites.net/api/v1/Books/153245234542345

"Content-Type: application/json; v=1.0"

{
  "id": 0,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-07-02T19:14:26.245Z"
}

Code: 400

{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-ae9039605f3dc54ebd84b9bd6c3320ad-1c0e37cbccf6194d-00",
  "errors": {
    "id": [
      "The value '153245234542345' is not valid."
    ]
  }
}

25. DELETE ​/api​/v1​/Books​/{id}

https://fakerestapi.azurewebsites.net/api/v1/Books/1

"accept: */*"

Code: 200

Success

26. DELETE ​/api​/v1​/Books​/{id}

https://fakerestapi.azurewebsites.net/api/v1/Books/1235235235235

"accept: */*"

Code: 400

{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-bdec97021a605345b3dfe4a7732d0330-c080861d37b92542-00",
  "errors": {
    "id": [
      "The value '1235235235235' is not valid."
    ]
  }
}

27. GET ​/api​/v1​/CoverPhotos

https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos

"accept: text/plain; v=1.0"

Code: 200

[
  {
    "id": 1,
    "idBook": 1,
    "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 1&w=250&h=350"
  },
  {
    "id": 2,
    "idBook": 2,
    "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 2&w=250&h=350"
  },
  {
    "id": 3,
    "idBook": 3,
    "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 3&w=250&h=350"
  },
  {
    "id": 4,
    "idBook": 4,
    "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 4&w=250&h=350"
  },

28. POST ​/api​/v1​/CoverPhotos

https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos

"Content-Type: application/json; v=1.0" 

{
  "id": 0,
  "idBook": 0,
  "url": "string"
}

Code: 200

{
  "id": 0,
  "idBook": 0,
  "url": "string"
}

29. GET ​/api​/v1​/CoverPhotos​/books​/covers​/{idBook}

https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/books/covers/1

"accept: text/plain; v=1.0"

Code: 200

[
  {
    "id": 1,
    "idBook": 1,
    "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 1&w=250&h=350"
  }
]

30. GET ​/api​/v1​/CoverPhotos​/books​/covers​/{idBook}

https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/books/covers/15346345745

"accept: text/plain; v=1.0"

Code: 400

{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-50a731a09f6ab640915d2393a5c1e5df-6d26be7f5813af4b-00",
  "errors": {
    "idBook": [
      "The value '15346345745' is not valid."
    ]
  }
}

31. GET ​/api​/v1​/CoverPhotos​/{id}

https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/1

"accept: text/plain; v=1.0"

Code: 200

{
  "id": 1,
  "idBook": 1,
  "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 1&w=250&h=350"
}

32. GET ​/api​/v1​/CoverPhotos​/{id}

https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/14563463463

"accept: text/plain; v=1.0"

Code: 400

  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-741d802bf6127444beebda4616bca080-d7488548e22cf84d-00",
  "errors": {
    "id": [
      "The value '14563463463' is not valid."
    ]
  }
}

33. PUT ​/api​/v1​/CoverPhotos​/{id}

https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/1

"Content-Type: application/json; v=1.0"

{
  "id": 0,
  "idBook": 0,
  "url": "string"
}

Code: 200

{
  "id": 0,
  "idBook": 0,
  "url": "string"
}

34. PUT ​/api​/v1​/CoverPhotos​/{id}

https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/14124124124

"Content-Type: application/json; v=1.0"

{
  "id": 0,
  "idBook": 0,
  "url": "string"
}

Code: 400

{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-cd4bf53e85529640b31ebcadb52cfabd-7b2e6482c62efe4c-00",
  "errors": {
    "id": [
      "The value '14124124124' is not valid."
    ]
  }
}

35. DELETE ​/api​/v1​/CoverPhotos​/{id}

https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/1

"accept: */*"

Code: 200

Success

36. DELETE ​/api​/v1​/CoverPhotos​/{id}

https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/143643636434634

"accept: */*"

Code: 400

{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-553fec7b0f47cf4c93d1a9f66c2db34a-27153b1191120e4d-00",
  "errors": {
    "id": [
      "The value '143643636434634' is not valid."
    ]
  }
}

37. GET ​/api​/v1​/Users

https://fakerestapi.azurewebsites.net/api/v1/Users

"accept: text/plain; v=1.0"

Code: 200

[
  {
    "id": 1,
    "userName": "User 1",
    "password": "Password1"
  },
  {
    "id": 2,
    "userName": "User 2",
    "password": "Password2"
  },
  {
    "id": 3,
    "userName": "User 3",
    "password": "Password3"
  },
  {
    "id": 4,
    "userName": "User 4",
    "password": "Password4"
  },

38. POST ​/api​/v1​/Users

https://fakerestapi.azurewebsites.net/api/v1/Users

"accept: */*"
"Content-Type: application/json; v=1.0" -d "

{
  "id": 0,
  "userName": "string",
  "password": "string"
}

Code: 200 

{
  "id": 0,
  "userName": "string",
  "password": "string"
}

39. GET ​/api​/v1​/Users​/{id}

https://fakerestapi.azurewebsites.net/api/v1/Users/1

"accept: */*"

Code: 200 

{
  "id": 1,
  "userName": "User 1",
  "password": "Password1"
}

40. GET ​/api​/v1​/Users​/{id}

https://fakerestapi.azurewebsites.net/api/v1/Users/1124124124124

"accept: */*"

Code: 400 

{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-b63bc917e7a7a349866fab6a6f5b7e37-79c7ebd0f0d12642-00",
  "errors": {
    "id": [
      "The value '1124124124124' is not valid."
    ]
  }
}

41. PUT ​/api​/v1​/Users​/{id}

https://fakerestapi.azurewebsites.net/api/v1/Users/1

"accept: */*"
"Content-Type: application/json; v=1.0"

{
  "id": 0,
  "userName": "string",
  "password": "string"
}

Code: 200 

{
  "id": 0,
  "userName": "string",
  "password": "string"
}

42. PUT ​/api​/v1​/Users​/{id}

https://fakerestapi.azurewebsites.net/api/v1/Users/16364363463

"accept: */*"
"Content-Type: application/json; v=1.0"

{
  "id": 0,
  "userName": "string",
  "password": "string"
}

Code: 400 

{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-5c8da202ac442a4d9bf78959fba09396-894445d9cec2c743-00",
  "errors": {
    "id": [
      "The value '16364363463' is not valid."
    ]
  }
}

43. DELETE ​/api​/v1​/Users​/{id}

https://fakerestapi.azurewebsites.net/api/v1/Users/1

"accept: */*"

Code: 200 

Success

44. DELETE ​/api​/v1​/Users​/{id}

https://fakerestapi.azurewebsites.net/api/v1/Users/13252523523

"accept: */*"

Code: 400 

{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-25bce0ba6841c54e9a2c1a7726653788-e3e6d0528edd9540-00",
  "errors": {
    "id": [
      "The value '13252523523' is not valid."
    ]
  }
}
