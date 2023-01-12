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

check laravel version
`php artisan --version`

update node.js to latest (https://nodejs.org/ja/)

# function
- create user
- login
- view user book list
- add book
- delete book
- follow user
- unfollow user
- logout

# todo
- mysql とつなぐ
- rakuten books api を呼ぶ
