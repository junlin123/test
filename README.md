# push

## Introduction

Third party message push

## Install

```
$ composer require yanlongma/push
```
## junlin2 测试3
## Demo

```php
<?php

require __DIR__ . '/vendor/autoload.php';

$appKey = 'your-app-key';
$masterSecret = 'your-master-secret';

$alert = 'Hi JPush!';
$extras = [
    'type' => 1,
    'url' => 'http://www.junlin.com'
];
$platform = ['android', 'ios'];
$audience = [
    'alias' => ['13888888888']
];

$push = new YanlongMa\Push\JPush($appKey, $masterSecret);
$push->push($alert, $extras, $platform, $audience);
```