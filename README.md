# Database scanner and automatic translator #
Translator package 
###### An elegant way to scan all text of blade files and send to database them. ##


## Installation ##

The preferred way to install this extension is through [composer](http://getcomposer.org/download/).

Either run

```injectablephp
 composer require teamprodev/laravel-translator
```

or add below line to the require section of composer.json file and then run `php composer.phar update -vv --prefer-dist --profile`

```injectablephp
"teamprodev/laravel-translator": "*"
```
Place it in config/app.php
```injectablephp
'providers' => [ 
   ...
   TeamPro\TranslateScanner\TranslateScannerServiceProvider::class
]
```
You should place it in config/app.php
```injectablephp
'providers' => [ 
   ...
   TeamPro\TranslateScanner\TranslateScannerServiceProvider::class
]
```
## How To Use ##

You should migrate tables once
```injectablephp
php artisan migrate --path=/database/migrations/translations
```
Scan it with in cmd once
```injectablephp
php artisan scan:translation
```

All formats of text must be used like this
###### my_view.blade.php
```html
 <p>{{trans("your any texts here")}}</p>
```
###### index.html
```html
 <p>{{trans("your any texts here")}}</p>
 
 <p> <?php trans("your any texts here"); ?> </p>
```
###### MyController.php or any php based file
```html
 trans("your any texts here");
```
## Changelog ##

### 1.0 ###
* First version


## Contributors ##

* [Bekzod Erkinov](https://github.com/iBekzod)
* [O'ktam](https://github.com/Uktam19980416)
