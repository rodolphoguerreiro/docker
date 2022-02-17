# Hosts and file structure

As stated before, we included a few different webroots. These webroots can be used with different hostnames:
 
 - `htdocs`
 - `httpdocs`
 - `public`
 - `pub`

## Magento 1
Magento 1 projects in both PHP7 and PHP5 are supported. 

All webroots supported.

E.g.: `http://iwant.coffee.magento.locahost`.
You can also identify a MAGE_RUN_CODE, `customer.project.MAGE_RUN_CODE.magento.locahost`.

## Magento 2
Magento 2 projects are only supported in PHP7. 

Hostname `customer.project.magento2.locahost` => PHP7
Only supports `pub` as webroot.

E.g.: `http://iwant.coffee.magento2.locahost`.

## Symfony 2 / 3
Symfony projects in both PHP7 and PHP5 are supported.

Hostname `*.symfony.locahost` => PHP7.
Hostname `*.symfony.php5.locahost` => PHP5.
All webroots + `web` are supported.

E.g.: `http://iwant.coffee.symfony.locahost`.

## Silex
Silex projects in both PHP7 and PHP5 are supported.

Hostname `*.symfony.locahost` => PHP7.
Hostname `*.symfony.php5.locahost` => PHP5.
All webroots + `web` are supported.

E.g.: `http://iwant.coffee.silex.locahost`.
