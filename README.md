# JwtAuth

A simple program to make a **Api** requests using **Asp.Net core** and **Jwt** authentication.

## Build instructions

* Install [.Net core](https://dotnet.microsoft.com/download)
* Navigate to your project path with **terminal or cmd** and launch the following command **dotnet run**, the localhost should be on the **5000 port**, otherwise check the terminal/cmd output.

## Http requests

* Request type **POST**, **http://localhost:5000/api/token** generate the token to authenticate through Get request, the json body has the following format:

```json
{
	"username":"mario",
	"password":"secret"
}
```

* Request type **GET**, after you have logged in, set the authentication as Bearer and use the token that has been generated with the previous request to generate a result from the following Get response **http://localhost:5000/api/books**

Example of Get request result:

```json
[
    {
        "author": "Ray Bradbury",
        "title": "Fahrenheit 451",
        "ageRestriction": false
    },
    {
        "author": "Gabriel García Márquez",
        "title": "One Hundred years of Solitude",
        "ageRestriction": false
    },
    {
        "author": "George Orwell",
        "title": "1984",
        "ageRestriction": false
    },
    {
        "author": "Anais Nin",
        "title": "Delta of Venus",
        "ageRestriction": true
    }
]
```

## Built with

* [Asp.Net core](https://docs.microsoft.com/en-us/aspnet/?view=aspnetcore-2.2#pivot=core)
* [Visual studio](https://visualstudio.microsoft.com/)
* [C#](https://docs.microsoft.com/en-us/dotnet/csharp/)
* [Jwt](https://jwt.io/)
