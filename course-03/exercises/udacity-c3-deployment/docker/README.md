# Udagram Image Filtering Microservice

Udagram is a simple cloud application developed alongside the Udacity Cloud Engineering Nanodegree. It allows users to register and log into a web client, post photos to the feed, and process photos using an image filtering microservice.



## Tasks

### Setup Docker Environment
You'll need to install docker https://docs.docker.com/install/. Open a new terminal within the project directory and run:

1. Build the images: `docker-compose -f docker-compose-build.yaml build --parallel`
2. Push the images: `docker-compose -f docker-compose-build.yaml push`
3. Add .env files: see below 
4. Run the container: `docker-compose up`

### Add .env files
To simplify the environment variables for the two backend services, the variables have been extracted into 3 files:

* `aws.env` : contains `AWS_REGION`, `AWS_PROFILE`, `AWS_BUCKET`
* `postgres.env` : contains `POSTGRESS_USERNAME`, `POSTGRESS_PASSWORD`, `POSTGRESS_DB`, `POSTGRESS_HOST`
* `jwt.env` : contains `JWT_SECRET`

These need to be created before running `docker-compose up`.