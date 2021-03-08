# show-dot-php-in-htaccess
mostrar ext .php no fim do ficheiro index.php - config .htaccess

## show .php
```
# Turn on url rewriting
RewriteEngine on

# Remove the need for .php extention
RewriteCond %{REQUEST_FILENAME} !-f
RewriteCond %{REQUEST_FILENAME} !-d
RewriteRule ^(.*)$ $1.php
```

## dont show .php
```
RewriteEngine On

RewriteCond %{REQUEST_FILENAME} !-f
RewriteCond %{REQUEST_FILENAME} !-d
RewriteRule ^(.*)$ index.php/$1 [L]
```
