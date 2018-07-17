# LUMENT SIMPLE REST API
made with :heart: by b0nz
> RestAPI with Lumen 5.5

## Features
* Login & Register
* JWT-Auth
* ... *in the development process*


## Requirements
* PHP 7.0
* OpenSSL PHP Extension
* PDO PHP Extension
* Mbstring PHP Extension


## Installations
```
$ git clone 
$ cd lumenRestAPI
$ cp .env.example .env
$ nano .env
```

To generate `APP_KEY`, run this command.
```
$ php -S localhost:8000 -t public
```
Open `http://localhost:8000/key`, copy the key, and fill in `APP_KEY`.
> *make sure after generate Key, delete the following code* in `routes/web.php`
```
    $router->get('/key', function() {
        return str_random(32);
    });
```

```
$ php artisan migrate
```

## Rest API Design
```
    POST    /login                          login *{"email":"USER_EMAIL", "password":"USER_PASSWORD"}*
    POST    /register                       register new user *{"username":"USERNAME", "email":"USER_EMAIL", "password":"USER_PASSWORD"}*
    GET     /user?api_token={API_TOKEN}     list user
```

