# RateLimit

A Zend Framework module that helps you to deal with rate limit.

# HOW TO USE

1. In your `composer.json` file, add:
```json
    "repositories": [
        {
            "url": "https://github.com/inmediam/zf-rate-limit.git",
            "type": "git"
        }
    ],
```

2. In the terminal, run:
```sh
composer require inmediam/zf-rate-limit
```

3. In your config file (eg. config/autoload/global.php), add:
```php
return [
    // ...
    'rate_limit' => [
        'routes' => ['*'],
        'storage' =>  [
            'adapter' => Zend\Cache\Storage\Adapter\Filesystem::class,
            'options' => [
                'cache_dir' => __DIR__ . '/../../data/cache',
            ],
        ],
        'limit' => 2,
        'period' => 15,
    ]
];
```


## License

RateLimit is licensed under [The MIT License (MIT)](LICENSE).
