
<p align="center">

   <img alt="License" src="https://img.shields.io/badge/license-MIT-%23F26C6C">


  <a href="https://www.linkedin.com/in/wilsonfranca-dev-engineer/">
    <img alt="Made by Wilson Franca" src="https://img.shields.io/badge/made%20by-Wilson%20Franca-%230AA186">
  </a>
</p>

<h1 align="center" style="height: 100px;">
    <img alt="Nodejs" title="#Nodejs" src="https://miro.medium.com/max/1200/1*fsseXIPGEhwmg6kfgXyIjA.jpeg" />
</h1>

<h4 align="center">
	Nodejs JWT Authorization Test Driven Development (TDD)  (Practice)
</h4>

<p align="center">
 <a href="#-about-the-project">About</a> •
 <a href="#-functionalities">Functionalities</a> •
 <a href="#-how-to-run-the-project">How to run</a> •
 <a href="#-technologies">Technologies</a> •
 <a href="#-author">Author</a> •
 <a href="#user-content--license">License</a>
</p>


## 💻 About the project

This project's goal was to practice Test Driven Development (TDD) with a NodeJS API RESTful built from scratch. This app contains both integration and unit tests for the JWT User Authentication functionality. 

---

## ⚙️ Functionalities

[X] Basic Nodejs API
- [X] POST -> /session
    - SessionController
- [X] GET -> /dashboard

[X] Environment Variables with `dotenv`
- .env (not included in this folder)
- .env.test

[X] Session Integration Test
- [X] It should authenticate with valid credentials
- [X] It should not authenticate with invalid email
- [X] It should not authenticate with invalid credentials
- [X] It should return jwt token when authenticated
- [X] It should be able to access private routes when authenticated
- [X] It should not be able to access private routes without a jwt token
- [X] It should not be able to access private routes with invalid token

[X] User Unit Test
- [X] It should encrypt user password

[X] Truncate tests' database to start with a fresh database even if tests fail

[X] Multiple user creation randomically using fake data
- Use `faker` and `factory-girl` 

[X] Test Coverage

---

## 🚀 How to run the project

This practice project contains:
1. Backend (authtdd directory)

💡 RESTful API.

### Requirements

Initial requirements:
[Git](https://git-scm.com), [Node.js](https://nodejs.org/en/), [Yarn](https://yarnpkg.com/), a relational database and a code editor of your choice.

#### Create your Environment Variables (.env)

Create a `.env` file at your root directory and include your development environment variables:

```

APP_SECRET=your_secret_key

DB_HOST=your_ip_address
DB_PORT=your_db_port
DB_USER=your_database_username
DB_PASS=your_database_passcode
DB_NAME=your_database_name

```

#### Creating a Database Container (Docker)

> Skip this step if you are not using docker or do not need to create a new container.

Start your docker quickstart terminal. Then, start a Postgres instance running:

```bash

docker run --name your_database_name -e POSTGRES_PASSWORD=your_database_passcode -p 5433:5432 -d postgres

```

💡 `5433:5432` (port_in_your_host_os:port_in_your_container)

I am using PORT 5433 because I already have Postgres installed on my Host OS, which is using PORT 5432 already. If you **do not** have Postgres installed on your machine, you could use `5432:5432`.

💡 Check if your PORT is open for Postgres:

- Linux/MacOS = `lsof -i:5432`
- Windows (port 5432) = `Get-Process -Id (Get-NetTCPConnection -LocalPort portnumber).OwningProcess`

💡 Use `:number` suffix for the Postgres image to define the version to be installed.

After creating your docker container with Postgres image, list your containers, copy the id, and start the container you just created:

```bash

# List all docker containers
$ docker ps -a

# Start the container using its ID
$ docker start container_id

```

#### Running Nodejs (Server)

```bash

# Clone this repository
$ git clone git@github.com:wilsonfsouza/nodeauthorization-tdd-jest.git

# Access the folder in your terminal/cmd
$ cd authtdd

# Install dependencies
$ yarn install

# Run tests
$ yarn test

```

---

## 🛠 Technologies

The following tools were used in this project:

#### [](https://github.com/wilsonfsouza/nodeauthorization-tdd-jest#server-nodejs)**Server**  ([NodeJS](https://nodejs.org/en/))

-   **[Express](https://expressjs.com/)**
-   **[Sequelize ORM](https://sequelize.org/)**
-   **[PostgreSQL](https://www.postgresql.org/)**
-   **[Sqlite 3](https://sqlite.org/index.html)** (tests)
-   **[Nodemon](https://nodemon.io/)**
-   **[Jest](https://jestjs.io/)**
-   **[Supertest](https://github.com/visionmedia/supertest)**
-   **[Dotenv](github.com/motdotla/dotenv#readme)**
-   **[Jsonwebtoken](https://www.jsonwebtoken.io/)**
-   **[Bcryptjs](https://github.com/dcodeIO/bcrypt.js/)**
-   **[Faker](https://github.com/marak/Faker.js/)**
-   **[Factory-girl](https://github.com/simonexmachina/factory-girl)**

> See the file  [package.json](https://github.com/wilsonfsouza/nodeauthorization-tdd-jest/blob/main/package.json)

#### [](https://github.com/wilsonfsouza/nodeauthorization-tdd-jest#utilities)**Utilities**

-   Container: **[Docker](https://www.docker.com/)**
-   Editor:  **[Visual Studio Code](https://code.visualstudio.com/)**  → Extensions:  **[SQLite](https://marketplace.visualstudio.com/items?itemName=alexcvzz.vscode-sqlite)**
-   Markdown:  **[StackEdit](https://stackedit.io/)**,  **[Markdown Emoji](https://gist.github.com/rxaviers/7360908)**

---

## 💪 How to contribute to this project

1. **Fork** the project.
2. Start a new branch with your changes: `git checkout -b my-new-feature`
3. Save it and create a commit message describing what you have done: `git commit -m "feature: My new feature"`
4. Send your alterations: `git push origin my-feature`

---

## 👨‍💻 Author

<br/>
<h3 style="display: flex; align-items: center; justify-content: flex-start;">
 <img style="border-radius: 50%; margin-right: 20px; width: 80px;" src="https://avatars0.githubusercontent.com/u/21347383?s=460&u=fdb399c92e369762d45d6495cbd2e87eef9e4d65&v=4" width="100px;" alt="Wilson Franca"/>
 <br />
 <sub>Wilson Franca</sub></h3>
 <br />

[![Linkedin Badge](https://img.shields.io/badge/-Wilson-blue?style=flat-square&logo=Linkedin&logoColor=white&link=https://www.linkedin.com/in/wilsonfranca-dev-engineer/)](https://www.linkedin.com/in/wilsonfranca-dev-engineer/)
[![Gmail Badge](https://img.shields.io/badge/-wilson.franca.92@gmail.com-c14438?style=flat-square&logo=Gmail&logoColor=white&link=mailto:wilson.franca.92@gmail.com)](mailto:wilson.franca.92@gmail.com)

---

## 📝 License

This project is being developed under [MIT License](./LICENSE).

Made with ❤️ by Wilson Franca 👋🏽

