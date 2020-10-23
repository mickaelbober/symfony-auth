Symfony Auth Application
============

The "Symfony Auth Application" is a simple application to show how to authentificate 
user following the [Symfony Best Practices][1].

Requirements
------------

Require the [usual Symfony application requirements][2].

  * PHP 7.2.9 or higher
  * Mysql 8.0.21 or higher
  * Some PHP extensions
  * Composer
  * Symfony CLI

Installation
------------

Clone the [repository][3] on your computer:

```bash
$ git clone https://github.com/mickaelbober/symfony-auth.git symfony-auth
```

Configuring your `.env` file:

```bash
DATABASE_URL=mysql://symfony_auth:Azerty12@127.0.0.1:3306/symfony_auth?serverVersion=8.0
```

Create the database:

```bash
$ cd symfony-auth/
$ php bin/console doctrine:database:create
```

Apply migrations:

```bash
$ cd symfony-auth/
$ php bin/console doctrine:migrations:migrate
```

Composer
------------

[Download Composer][4] to install the `composer` binary on your computer and install
dependencies to the `./vendor` directory.

```bash
$ cd symfony-auth/
$ composer install
```

Symfony CLI
------------

[Download Symfony][5] to install the `symfony` binary on your computer. 

```bash
$ wget https://get.symfony.com/cli/installer -O - | bash
```

Run this command and access the application in your
browser at the given URL (<https://localhost:8000> by default):

```bash
$ cd symfony-auth/
$ symfony server:start
```

If you don't have the Symfony binary installed, run `php -S localhost:8000 -t public/`
to use the built-in PHP web server or [configure a web server][6] like Nginx or
Apache to run the application.

References
------------

 * [Security][7]
 * [Guard][8]
 * [Security User Providers][9]
 * [The Symfony MakerBundle][10]
 * [Openclassrooms.com : Tutorial][11]

[1]: https://symfony.com/doc/current/best_practices.html
[2]: https://symfony.com/doc/current/setup.html
[3]: https://github.com/mickaelbober/symfony-auth
[4]: https://getcomposer.org/download/
[5]: https://symfony.com/download
[6]: https://symfony.com/doc/current/setup/web_server_configuration.html
[7]: https://symfony.com/doc/current/security.html
[8]: https://symfony.com/doc/current/security/guard_authentication.html
[9]: https://symfony.com/doc/current/security/user_provider.html
[10]: https://symfony.com/doc/current/bundles/SymfonyMakerBundle/index.html
[11]: https://openclassrooms.com/fr/courses/5489656-construisez-un-site-web-a-l-aide-du-framework-symfony-4/5654131-securisez-lacces-de-votre-site-web
