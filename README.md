# Gatsby and Drupal 10 Proof of Concept Project

This project demonstrates the integration of Gatsby, a modern front-end framework, with Drupal 10, a powerful CMS. It's designed to showcase how these technologies can work together effectively.

## Getting Started
These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

## Prerequisites
Before setting up the project, ensure you have the following installed:

- Docker
- Lando

## CMS Setup
- Start Docker and Lando:
Make sure Docker and Lando are running on your machine.
- Navigate to the CMS Directory:
```
cd cms
```
- Start Lando:
```bash
lando start
```
- Install Dependencies with Composer:

```
lando composer install
```

- Import Database:
Place your drupal10_db.sql.gz database file in the db directory and execute:

```
lando db-import db/drupal10_db.sql.gz
```

- Move Files to CMS:

Extract and move the contents from assets/files.tar.gz to web/sites/default/files.

## Frontend Setup
- Install Dependencies:

```
yarn install
```

- Setup Environment:

```
yarn setup
```

	Drupal Credentials:

```
Host: http://drupal10.lndo.site:8000/user/1
Username: admin
Password: admin
```

- Start the Frontend Server:

```
yarn start

```
