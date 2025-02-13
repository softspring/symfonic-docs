# Symfonic standalone

## Description

[Symfonic Standalone](https://github.com/softspring/symfonic-standalone) is a great way to dive into the world of [Symfonic](https://github.com/softspring/symfonic). With a
quick and easy setup, you can have a fully functional local development environment in minutes.

## Installation

**1. Clone this repository:**

```bash
    git clone https://github.com/softspring/symfonic-standalone
```

**2. Install dependencies**

1. [Symfony CLI](https://symfony.com/download):

```bash
curl -1sLf 'https://dl.cloudsmith.io/public/symfony/stable/setup.deb.sh' | sudo -E bash
sudo apt install symfony-cli
```
***macOS:***
```bash
brew install symfony-cli/tap/symfony-cli
```

2. [Docker](https://docs.docker.com/get-docker/):
   Choose one option.

3. PHP

```bash
sudo apt install php-cli 
sudo apt in
```
***macOS:***

First you need Xcode Command ine tools:
```bash
xcode-select --install
```

```bash
brew install php
brew install mysql
```



4. Composer

```bash
sudo apt install composer
```
***macOS:***
```bash
brew install composer
```

5. NPM
   (Node >= 18)

```bash
sudo apt install npm
```

6. Lift the containers

in the folder where you downloaded symfonic-standalone run:
```bash
  docker compose up -d --force-recreate
```

7. Start the Symfony server

```bash
  symfony server:ca:install
  symfony server:start -d
```

8. Composer install

```bash
  composer install
```

9. Execute migrations

```bash
  php bin/console doctrine:migrations:migrate -n
```

10. Install front-end dependencies

```bash
  npm install
  npm run dev
```

11. Create a test user. In this case, the user is “admin”, the email is “email@example.com” and the password is “admin”.

```bash
  php bin/console sfs:user:create admin email@example.com admin
  php bin/console sfs:user:promote email@example.com 
```

12. (Optional) If you want an example page, you have to load fixture:

```bash
  php bin/console doctrine:fixtures:load -n --append --group=test
```
  
## Usage

Open your browser and go to https://127.0.0.1:8000/app/en/login.

1. Log in with the email and password you created in the previous step.
![login.png](.files/login.png)

2. You are done! You can now start working with Symfonic Standalone at https://127.0.0.1:8000/admin/en/.
![dashboard.png](.files/dashboard.png)

3. If you have executed point 8 of the installation and you wish to see the example page, you can consult the page at https://127.0.0.1:8000/admin/en/cms/pages/ , its name is 'Home'.
![example.png](.files/example.png)
   You can see the page information and edit it in https://127.0.0.1:8000/admin/en/cms/pages/0194cfc9-bbfa-79e7-baf7-0a300514f3cf 
![example-edit.png](.files/example-edit.png)
   If you publish it, you can see it at https://127.0.0.1:8000/en/home.
![example-page.png](.files/example-page.png)
    

