## Table of Contents

- [Quick Start](#quick-start)
  - [Installation](#installation)
  - [Configuration](#configuration)
  - [Sequelize Migration](#sequelize-migration)
- [Fixing Error](#fixing-error)

## Quick Start

## Installation

```sh
git clone https://github.com/homurin/binar-challenge-07.git
npm install

// run for develop
npm run dev

// run for testing
npm run test
```

## Configuration

You got error when run

```sh
npm run dev
// or
npm run start
// or
npm run test
```

You need to configure environment on `.env` file.
Copy `.env.example` file and name it `.env` or run this simple command on your terminal.

```sh
cp .env.example .env
```

Finally fill necessary environment variables to configure server and database. Then you can run the application

```sh
#  database configuration

DB_USER=postgres
DB_PASSWORD=
DB_NAME=challenge-chapter8
DB_HOST=localhost
DB_PORT=5432

#  jwt configuration

JWT_SIGNATURE_KEY=Rahasia

```

## Sequelize Migration

After download all dependencis and configure .env file, Last step is do postgresql migration with simply run this command.

```sh
# note : using npx sequelize instead when you not download globaly sequelize-cli on your local machine

sequelize db:create
sequelize db:migrate
sequelize db:seed:all
```

## Fixing Error

If you using linux and got database failed to connect then you can check postgresql server status.

```sh
systemctl status postgresql
```

If the postgresql server is inactive then start the service

```sh
sudo systemctl start postgresql
```
