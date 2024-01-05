# Dr-Broker-Backend

#### Introduction

# Backend Project Created Using Node.js with TypeScript, Express.js and MongoDB as Database Server

A few things to note in the project:
* **TypeScript** - It uses TypeScript.
* **JWT** - It uses JWT Token for Authentication.
* **Mongo Connection Helper** - A helper class to connect to MongoDB reliably.
* **Middleware for easier async/await** - Catches errors from routes and throws them to express error handler to prevent app crash due to uncaught errors.
* **.env file for configuration** - Change server config like app port, mongo url etc
* **Winston Logger** - Uses winston as the logger for the application.

#### Install dependencies

```
$ npm i
```

## Development

### Start dev server
```
$ npm run dev
```
Running the above commands results in 
* 🌏**API Server** running at `http://localhost:8000`
* 🛢️**MongoDB** running at `mongodb://localhost:27017`


## Environment
To edit environment variables, create a file with name `.env` and copy the contents from `.env.sample` to start with.

| Var Name  | Type  | Default | Description  |
|---|---|---|---|
|  PORT | number  | `8000` | Port to run the API server on |
|  DB_URL | string  | `mongodb://localhost:27017/library` | URL for MongoDB |

## Logging
The application uses [winston](https://github.com/winstonjs/winston) as the default logger. The configuration file is at `src/logger.ts`.
* All logs are saved in `./logs` directory.
* Console messages are prettified
* Each line in error log file is a stringified JSON.


## License
Copyright (c) ZAPTA Technologies. All rights reserved.
Licensed under the [MIT](LICENSE) License.
