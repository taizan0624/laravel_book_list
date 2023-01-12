# laravel_book_list

1. Install php and composer to your local
2. Execute commands<br>
`% composer create-project laravel/laravel example-app`<br>
`% cd example-app`<br>
`% php artisan serve // run development server`<br>
`% php artisan key:generate`
`% composer install --ignore-platform-req=ext-fileinfo // when seeing error with above command`<br>

3. Install MySQL to local
- Install using installer ref. https://prog-8.com/docs/mysql-env-win
- Add C:\Program Files\MySQL\MySQL Server 8.0\bin to environment variable

4. Execute migration (laravel will create tables on local MySQL)
- Edit .env, update DB_DATABASE and DB_PASSWORD
- php artisan migrate
- If seeing `Illuminate\Database\QueryException could not find driver error` -> Remove comment out of `extension=pdo_mysql` on php.ini(C:\Program Files\php-8.1.0-Win32-vs16-x64)

5. user authentication set up
`composer require laravel/breeze --dev
Your requirements could not be resolved to an installable set of packages.

  Problem 1
    - league/mime-type-detection 1.11.0 requires ext-fileinfo * -> it is missing from your system. Install or enable PHP's fileinfo extension.
    - laravel/framework v9.47.0 requires league/flysystem ^3.8.0 -> satisfiable by league/flysystem[3.12.1].
    - league/flysystem 3.12.1 requires league/mime-type-detection ^1.0.0 -> satisfiable by league/mime-type-detection[1.11.0].
    - laravel/framework is locked to version v9.47.0 and an update of this package was not requested.
edit php.ini extension=fileinfo, extension=gd
`php artisan breeze:install`
`npm install`
`npm run dev` -> In case of error, update node version. Just intall latest (https://nodejs.org/ja/), check by node -v
`php artisan migrate`

check laravel version
`php artisan --version`

update node.js to latest (https://nodejs.org/ja/)

# function
- create user (DONE)
- login (DONE)
- view user book list
- add book
  - call rakuten books api
- delete book
- follow user
- unfollow user
- logout (DONE)
