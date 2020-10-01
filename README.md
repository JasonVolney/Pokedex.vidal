---
description: Simple tutorial for aid the development of the documentation API Pokedéx
---

# API Pokédex

![https://pokeapi.co/](.gitbook/assets/pokeapi_256.888baca4.png)

The propose here is starting a new API and to do the API documentation for mockup our data at the application. Let's get started!

First of all, we made use of an API with HTTP methods, and to document this we used tools to facilitate the understanding of how to use the methods in the API, such a tool used in the previous example, the INSOMNIA DESIGNER, which has the purpose of making the interface designer API documentation using a [Swagger](https://github.com/swagger-api/swagger-ui) or [OpenAPI](https://github.com/OAI/OpenAPI-Specification) standard. Using a text language called YAML. The links for some that references are bellow:

{% embed url="https://github.com/OAI/OpenAPI-Specification/blob/master/versions/3.0.3.md\#parameterObject" caption="OpenAPI-Specification" %}

{% embed url="https://swagger.io/" caption="Swagger" %}

For now, we gonna look the website finished at this link: [https://pokedex-github-io.vercel.app/](https://pokedex-github-io.vercel.app/) that consuming API data of the mocking in an file in JSON format. 

But before we going to start downloading the application for understand better the code. Type this command on your prompt:

```text
git clone https://github.com/vidal987/Pokedex.vidal.git
cd Pokedex.vidal
```

Open up the code on your favorite IDE, in my case I use VSCode, and in your terminal type npm install for update dependencies for this project. Run `npm start` to see application in your browser. Or open with Live Server extension for VSCode.

![](.gitbook/assets/image%20%281%29.png)

After that we going to start with creating the new file and let's renaming like db.json and then copy and paste de code that is here [https://codeshare.io/5glXrw](https://codeshare.io/5glXrw)

We have two types of insomnia, the designer and the core. Basically the core is where you can work by examining the responses that the API will give, such as REST and [GraphQL](https://graphql.org/), whereas the designer is where you can debug your API, testing, managing specifications or editing documents as an OpenApi.

Now search for [https://insomnia.rest/](https://insomnia.rest/) and click em download button for install in your PC. This video shows the page for download insomnia app.

{% embed url="https://youtu.be/egcJa2W\_mHc" %}

Open up the Insomnia Designer.

![](.gitbook/assets/microsoftteams-image.png)

You can find the code in YAML format on codeshare.io [https://codeshare.io/senai115](https://codeshare.io/senai115), copy and paste this content in an new document.

![CRUD - CREATE, READ, UPDATE and DELETE methods](.gitbook/assets/microsoftteams-image-1-.png)

How can you see the methods GET, POST, PUT and DELETE are present. Go to GET method clicking in this button, and it's show us more informations like: parameters, and option like responses formats. Also, it's possible to copy the [Curl](https://curl.haxx.se/) commands and URL links.

![](.gitbook/assets/image%20%282%29.png)

Let's go back to the YAML file. This part of code is responsable for generate the GET method. Where we can declare the paths or endpoints that we want to include, and the waited responses in case of achieving the data in JSON format. It's return the status 200 OK when the answer is positive. Also, we can add a brief comments about this, like a instructions for the users on our summary.

```text
paths:
    /pokemons/{id}: 
      get:
        summary: Passe o id no corpo da requisição
        responses:
          '200':
            description: OK
```

