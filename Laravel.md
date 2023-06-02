# Laravel

## Some useful resource links

- [Top Laravel Packages Which You Can Use to Optimize App in 2022](https://www.cloudways.com/blog/best-laravel-packages/)
- [10 Laravel Packages you must use in 2022 - Jahid Anowar](https://jahid.dev/blog/top-laravel-packages/)
- Carbon DOCs: [Carbon - A simple PHP API extension for DateTime.](https://carbon.nesbot.com/docs/)
- [Laravel Artisan Cache Commands Explained - DEV Community](https://dev.to/kenfai/laravel-artisan-cache-commands-explained-41e1)

## Laravel VS code extensions

1. Very nice tutorial for Laravel 9 with a lot of good info on how to setup the entire enviroment - [Laravel Tutorial for Beginners | How to Learn Laravel | Complete Laravel Tutorial in 2023 - YouTube](https://www.youtube.com/watch?v=2mqsVzgsV_c)
   - Laravel Artisan by Ryan Naddy
   - Laravel Blade Snippets by Winnie Lin
   - Laravel Blade Spacer by Austen Cameron
   - Laravel Extra Intellisense by amir
   - PHP Intelephense by Ben Mewburn
   - Laravel goto view by codingyu
   - Laravel-goto-controler by stef-k
   - Laravel-goto-components by naoray
   - Laravel Snippets by Winnie Lin
   - PHP DocBlocker by Neil Brayfield
   - PHP Namespace Resolver by Mehedi Hassan
   - DotENV by mikestead

## How to fix common problems

### Page expired 419 after logout

[CSRF and expired logout forms - TALL Stack Tips](https://talltips.novate.co.uk/laravel/csrf-and-expired-logout-forms)

## Laravel artisan commands

`php artisan optimize:clear` :: pobriše ves cache naenkrat

`php artsian queue:work` :: zaženi queue workerja lokalno

`php artisan schedule:work` 

## cPanel cron jobs to run laravel scheduler

`/usr/local/bin/php /home/trgovine/subdomains/malica-staging.trgovine-mass.com/artisan schedule:run` - tole pošlje še mejl za vsakič ko se cron job izvede

`/usr/local/bin/php /home/trgovine/subdomains/malica.trgovine-mass.com/artisan schedule:run >/dev/null 2>&1` tole pa ne pošlje mejla ... 

Na shared hsotingu ne gre da bi imel zagnan queue workerja zato se periodično zažene scheduler in znotraj schedulerja se potem zaganja queue workerja na ta način:

```php
// app\Console\Kernel.php

$schedule->command('queue:work --stop-when-empty')
    ->everyMinute()
     ->withoutOverlapping();
```
