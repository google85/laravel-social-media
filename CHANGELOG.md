#### Changelog #
*************************************

- 2024-02-25
    - [bonus-by-me] convert `like`, `comment`, `document` SVG into their own SVG
    - [dashboard] implemented separate scroll
    - [dashboard] small screen optimizations
    - [dashboard] make `My Groups` a foldable (Disclosure) area on small screens, refactor into component
    - [dashboard] make `My Followings` foldable, refactor into component
    - [dashboard] wrap all into `AuthenticatedLayout`, fix the scroll area
    - added screenshot

- 2024-02-24
    - [video-part-4]
    - creating home page
    - `/` route works only logged in
    - added `HomeController`:
    ```bash
    php artisan make:controller HomeController
    chown 1000:1000 app/Http/Controllers/HomeController.php
    ```
    - created the dashboard page as simple html, convert parts of it to component
    - added `Following` list as components, like in `My Groups`
    - created `Create Post` component
    - created `Post List/Post Item` components
    - install headless-ui for using in 'show more..' components
    ```bash
    npm install @headlessui/vue@latest
    ```
    - implemented `Read more/less` on post
    - added second post, group name on post, hover effects on img, group images / other type of attachments, updated download buttons on them
    - add like/comment buttons on attachments of each post
    - small UI updates, added group-hover on images [pe rand]
    - responsive updates


- 2024-02-18
    - [video-part-3]
    - use sluggable package for username:
    ```bash
    composer require spatie/laravel-sluggable
    ```
    - add username generated from name into the database
    - add update username (slug) from Profile page, but prevent from re-creating slug when updating Name

- 2024-01-20
    - install Laravel with sail for linux:
    ```bash
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
    - [PENDING] add username from name