PayumPayzen
===========

PayZen Payum Gateway (Systempay, Scellius)

[![Build](https://github.com/ekyna/PayumPayzen/actions/workflows/build.yml/badge.svg?branch=master)](https://github.com/ekyna/PayumPayzen/actions/workflows/build.yml)

## Installation / Configuration

```bash
composer require ekyna/payum-payzen
```

```php
use Ekyna\Component\Payum\Payzen\Api\Api;
use Ekyna\Component\Payum\Payzen\PayzenGatewayFactory;

$factory = new PayzenGatewayFactory();

$gateway = $factory->create([
    'site_id'     => '132456',
    'certificate' => '132456',
    'ctx_mode'    => Api::MODE_PRODUCTION,
    'directory'   => __DIR__ . '/payzen-cache',
]);

// Register your convert payment action
// $gateway->addAction(new \Acme\ConvertPaymentAction());
```
