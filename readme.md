This repository will get you quickly up and running with the following:

- PHP5
- MySQL
- Laravel

Instructions:
- Install [VirtualBox](https://www.virtualbox.org/wiki/Downloads)
- Install [Vagrant](https://www.vagrantup.com/downloads.html)
- Clone the repository
- Copy `.env.example` to `.env`
- Run the command `vagrant up`
- Rename `test.conf` to the subdomain you want, ending with `.conf`
- Change the lines following `# CHANGE THIS LINE #` in: `test.conf`, `privileged.sh`, `unprivileged.sh`, `Vagrantfile` to the same subdomain as your `.conf`
- Add `<subdomain>.localhost.com` to your host file with the ip `127.0.0.1`
- Access your site at `<subdomain>.localhost.com:8080`

You will need to modify the file, `provisioners/privileged.sh` to use your own desired password for the MySQL server.

You will want to update `.env` with the password above, as well as with the default database that you setup. I recommend using MySQL Workbench as your DBMS.

MySql Workbench settings for the server are as follows:
Connection Method: Standard TCP/IP over SSH
SSH Hostname: `192.168.33.10:22` (from config.vm.network in Vagrantfile)

SSH Username: `vagrant`

SSH Keyfile: `/path/to/project/.vagrant/machines/default/virtualbox/private_key`

MySQL Hostname: `127.0.0.1`

MySQL Server Port: `3306`

Username: `root`

Password: `not_safe_password` (or whatever you changed it to)

Note: Testing the database connection may fail the first time. Try again.

This repository is dependent on....

# Laravel PHP Framework

[![Build Status](https://travis-ci.org/laravel/framework.svg)](https://travis-ci.org/laravel/framework)
[![Total Downloads](https://poser.pugx.org/laravel/framework/d/total.svg)](https://packagist.org/packages/laravel/framework)
[![Latest Stable Version](https://poser.pugx.org/laravel/framework/v/stable.svg)](https://packagist.org/packages/laravel/framework)
[![Latest Unstable Version](https://poser.pugx.org/laravel/framework/v/unstable.svg)](https://packagist.org/packages/laravel/framework)
[![License](https://poser.pugx.org/laravel/framework/license.svg)](https://packagist.org/packages/laravel/framework)

Laravel is a web application framework with expressive, elegant syntax. We believe development must be an enjoyable, creative experience to be truly fulfilling. Laravel attempts to take the pain out of development by easing common tasks used in the majority of web projects, such as authentication, routing, sessions, queueing, and caching.

Laravel is accessible, yet powerful, providing tools needed for large, robust applications. A superb inversion of control container, expressive migration system, and tightly integrated unit testing support give you the tools you need to build any application with which you are tasked.

## Official Documentation

Documentation for the framework can be found on the [Laravel website](http://laravel.com/docs).

## Contributing

Thank you for considering contributing to the Laravel framework! The contribution guide can be found in the [Laravel documentation](http://laravel.com/docs/contributions).

## Security Vulnerabilities

If you discover a security vulnerability within Laravel, please send an e-mail to Taylor Otwell at taylor@laravel.com. All security vulnerabilities will be promptly addressed.

## License

The Laravel framework is open-sourced software licensed under the [MIT license](http://opensource.org/licenses/MIT).
