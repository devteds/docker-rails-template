# README

Template for creating Rails application using docker. Create a new directory on your machine, copy the files from this repo and follow the instructions below.

## Tested on

* macOS - 10.12
* Docker - 1.12.6, 1.13.0
* Docker compose - 1.9.0, 1.10.0

## Instructions / commands

```
# Go to your projects or work directory and,
git clone git@github.com:ec-codecasts/docker-rails-template.git myapp
cd myapp
rm -rf .git
docker-compose run app rails new . --force --database=mysql --skip-bundle
mv database.yml config/database.yml
docker-compose build
docker-compose up
# http://localhost:3001/
```

## Build your application

Now that you have the rails application setup, start adding features - controllers, views, models, resources, migrations etc.

## Some useful commands

```
bin/d_rails g scaffold post title body:text
# or
# docker-compose run --rm app rails g scaffold post title body:text
bin/d_rails db:migrate
bin/d_rails c
```

## Rails API-only 

If you are creating an API-only application, with no UI or web-ui components, you may change the above "rails new ..." command as,

```
docker-compose run app rails new . --force --database=mysql --skip-bundle --api
```


