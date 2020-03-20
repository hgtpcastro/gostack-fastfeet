<h1 align="center">
  <img alt="Fastfeet" title="Fastfeet" src="https://github.com/Rocketseat/bootcamp-gostack-desafio-02/raw/master/.github/logo.png" width="300px" />
</h1>

<h3 align="center">
  GoStack Final Challenge: FastFeet
</h3>

## Instructions

Clone the project
```
git clone --recursive https://github.com/lucasbittar/gostack-fastfeet.git
```
We're using a different clone approach because this repository contains submodules for each piece of the application (back-end, front-end and mobile)

### Setup back-end
Change directory to the backend folder `cd backend` and run `yarn install`.

All of the following commands that has [] wrapped around it are related to the `.env` file. Just duplicate from `.env.example` and update the values.

- PostgreSQL
```
docker run --name database -e POSTGRES_PASSWORD=[DB_PASS] -p 5432:5432 -d [DB_USER]
```

- Redis
```
docker run --name redisfastfeet -p 6379:[REDIS_PORT] -d -t redis:alpine
```

- Seed database with admin user
```
yarn sequelize db:seed:all
```
This command generates the admin user with the following credentials:
```
Email: fastfeet@admin.com
Password: 123456
```

- Update the .env variables for Mailtrap and Sentry

At this point you shoud have the back-end all set up and good to go.

- Start server
```
yarn dev
```

- Start queue (open a new terminal)
```
yarn queue
```

### Setup front-end
Change directory to the front-end folder `cd frontend` and run `yarn install`.

- Start server
```
yarn start
```

### Setup mobile
Change directory to the mobile folder `cd mobile` and run `yarn install`.
The mobile app was tested on the **iOS Simulator* and on an *actual Android device*.

- Build app for Android
```
npx react-native run-android
```

- Build app for iOS
```
npx react-native run-ios
```

- Start server
```
yarn start
```
