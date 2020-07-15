This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

My part of job here is Docker stuff.

Dockerfile -> should be used in production. First step, build application using npm. Second step, copy build output from first step to default nginx folder and using nginx start production server.

Dockerfile.dev -> used for development. Simply loads node:alpine image and gets dependencies from package.json. Then copies all files to container and runs 'npm run start'.

docker-compose.yml -> constructed for development purposes. First service maps ports 3000:3000 and volumes: node_modules unmapped and everything else is mapped to container in order to have fast reload.
Second service created for automatic tests.
