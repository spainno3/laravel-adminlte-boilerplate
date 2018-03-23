# Laravel 5.6+ AdminLTE
> [Laravel 5.6+](https://laravel.com/docs/) and [AdminLTE 2.4+](https://github.com/almasaeed2010/AdminLTE)

## Included

- Frontend: Login, Registration
- Backend: User Management, Simple Role, Profile
- [Laravel Breadcrumbs](https://github.com/davejamesmiller/laravel-breadcrumbs)
- [Easy flash notifications](https://github.com/laracasts/flash)
- Tests

## How to use

- Clone: __git clone https://github.com/rrpadilla/laravel-adminlte-boilerplate.git my-new-project__
- cd my-new-project
- Copy __.env.example__ file to __.env__ and edit database credentials and APP_URL
- Run __composer install__
- Run __php artisan key:generate__
- Run __php artisan migrate --seed__
- Testing: Run __phpunit__
- See [UsersControllerTest](https://github.com/rrpadilla/laravel-adminlte-boilerplate/blob/master/tests/Feature/Controllers/Admin/UsersControllerTest.php)
- Login with:
    - Admin: __admin@admin.com__ - __secret__
    - Member: __member@example.com__ - __secret__

## Compatibility Chart

| Laravel | PHP  | Breadcrumbs | AdminLTE  
|---------|------|-------------|----------|
| 5.6+    | 7.1+ | **5.x**     | 2.4+ 

## Production

$ composer install --optimize-autoloader
$ php artisan config:cache
$ php artisan route:cache
$ php artisan view:clear
$ composer install --optimize-autoloader && php artisan config:cache && php artisan route:cache && php artisan view:clear

## Production (Configuring Trusted Proxies)

[See] https://laravel.com/docs/5.6/requests#configuring-trusted-proxies
Change your .env if:
- you're using AWS ELB:
    - TRUSTEDPROXY_PROXIES='*'
    - TRUSTEDPROXY_HEADERS='HEADER_X_FORWARDED_AWS_ELB'
- IP address (or range) of your proxy
    - TRUSTEDPROXY_PROXIES='192.168.1.1,192.168.1.2'
    - TRUSTEDPROXY_PROXIES='192.168.1.0/8'
    - TRUSTEDPROXY_HEADERS='HEADER_X_FORWARDED_ALL'

## Interface

![laravel-adminlte](https://user-images.githubusercontent.com/6921286/36182902-aed39d64-10e0-11e8-9442-4d036fa47d12.gif)
