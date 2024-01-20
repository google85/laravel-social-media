#### Changelog #
*************************************

- 2024-01-20
    - install Laravel with sail for linux:
    ```bash
    # x
    curl -s https://laravel.build/src | bash
    ```
    - install breeze with Vue support:
    ```bash
    composer require laravel/breeze --dev
    php artisan breeze:install
    # install
    php artisan migrate
    npm install
    ```
    - add models
    ```bash
    php artisan make:model Post -m
    php artisan make:model PostAttachment -m
    php artisan make:model PostReaction -m
    php artisan make:model Comment -m
    php artisan make:model Group -m
    php artisan make:model GroupUser -m
    php artisan make:model Follower -m
    php artisan make:model Notification -m
    ```
    - update post, group, group_users table migrations, move group, group_users creation before post
    - update migrations, add column to `users` table:
    ```bash
    php artisan make:migration add_columns_to_users_table
    php artisan migrate
    ```