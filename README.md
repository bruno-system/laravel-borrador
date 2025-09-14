<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400" alt="Laravel Logo"></a></p>

<p align="center">
<a href="https://github.com/laravel/framework/actions"><img src="https://github.com/laravel/framework/workflows/tests/badge.svg" alt="Build Status"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/dt/laravel/framework" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/v/laravel/framework" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/l/laravel/framework" alt="License"></a>
</p>

## alias sail
1. Ubique el archivo .bashrc (Dentro de Ubuntu > home > user).
Ábralo en un editor de texto y agregue la siguiente línea en la sección “some more ls
aliases”:
alias sail='sh $([ -f sail ] && echo sail || echo vendor/bin/sail)'


## Instalar dependencias:
Para instalar las dependencias de la aplicación, navega al directorio del proyecto y ejecuta
el siguiente comando desde la consola de ubuntu..
Este comando utiliza un contenedor Docker con PHP y Composer para instalar las
dependencias sin necesidad de tener PHP y Composer instalados en el sistema:
docker run --rm \
-u "$(id -u):$(id -g)" \
-v "$(pwd):/var/www/html" \
-w /var/www/html \
laravelsail/php84-composer:latest \
composer install --ignore-platform-reqs
Cuando utilice la imagen del compositor laravelsail/phpXX, debe utilizar la misma versión de
PHP que planea utilizar para su aplicación (80, 81, 82, 83 u 84).
