# 🛠 wiz-develop/php-cs-fixer-config
wiz-develop 用 php-cs-fixer 設定

## ✨ Features
- **Strict**: コードベースを厳格に保護します。
- **Modern**: 最新のPHP ver.に最適化されます。

## 📦 Installation
```shell
composer require --dev wiz-develop/php-cs-fixer-config
```

設定を有効にするためには `.php-cs-fixer.php` をプロジェクトに追加してください。

```php
<?php

declare(strict_types=1);

use PhpCsFixer\Finder;
use WizDevelop\PhpCsFixerConfig\Config;

return (new Config())
    ->setFinder(
        (new Finder())
            ->in(__DIR__),
    );
```

リスクの高いルールを許可したい場合は、コンストラクタで `$allowRisky` を true に設定してください。

```php
new Config(allowRisky: true)
```

## ✅ Versioning
このパッケージのバージョン x.y.z は PHP x.y で動作します (例: 8.3.x は PHP 8.3 で動作します)。
ルールセットが変更されると、z の数値が増加します。

| Package Version | PHP Version | Maintained? |
|-----------------|-------------|-------------|
| 8.4.x           | ^8.4        | Yes         |
| 8.3.x           | ^8.3        | Yes         |

