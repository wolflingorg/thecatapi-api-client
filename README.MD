# Task

Create a PHP API Client for ``https://docs.thecatapi.com/``

*implement at least ``search``, ``breed``, ``category`` methods

#### Example of API usage:
```php
$api = new TheCatAPI($apiKey);

/** @var Category[] $categories */
$categories = $api->categories()->all();

$request = (new SearchByBreedRequestBuilder($breedId))
            ->page(1)
            ->limit(10)
            ->create();

/** @var SearchResult[] $results */
$results = $api->images()->search($request);
```

#### Please ensure that:
 - You use ``http://docs.guzzlephp.org/en/stable/`` as HTTP client
 - You can switch your APP to offline mode and get stubbed results
 - You can turn on logging of all requests/responses
 - You can turn on response caching
 - You follow SOLID principles

#### Consider using
 - Adapter Design Pattern for Guzzle HTTP Client
 - Smart Proxy / Decorator Design Pattern for logging / caching
 - Builder Design Pattern for building requests / results
