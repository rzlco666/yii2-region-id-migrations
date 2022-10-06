# yii2-region-id-migration

**Indonesia regional & postcode database as Yii2 Migrations**

Database based on Minister of Home Affairs Regulation [(Kepmendagri No. 050-145 Tahun 2022)](https://www.kemendagri.go.id/arsip/detail/10857/keputusan-menteri-dalam-negeri-nomor-050145-tahun-2022-tentang-pemberian-kode-data-wilayah-administrasi-pemerintahan-dan-pulau-tahun-2021).

This repository will be updated when there is a new regulation.

Installation
---------

    composer require rzlco666/yii2-region-id-migrations:"@dev"

Config
-----------

in web.php or common.php for **(yii2-basic)** and main.php for **(yii2-advanced)** to activate module
```php
    'modules' => [
        'region' => [
            'class' => 'rzlco666\region\Module',
        ],
    ],
```

in console.php for **(yii2-basic)** and console/config/main.php for **(yii2-advanced)**
```php
    'controllerMap' => [
        'migrate' => [
            'class' => 'yii\console\controllers\MigrateController',
            'migrationNamespaces' => [
                'rzlco666\region\migrations',
            ],
        ],
    ],
```

Migration
----------

```
yii migrate
```

Or

```
php yii migrate
```

if you config console.php properly in latest yii, it will detect migration inside vendor folder


Thanks
----------
[database wilayah by cahyadsn](https://github.com/cahyadsn/wilayah)
[kodepos by edwinkun](https://github.com/edwinkun/database-kodepos-seluruh-indonesia)


created by [fredyns](http://fredyns.net)
