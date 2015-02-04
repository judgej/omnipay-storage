# Omnipay: Transaction Storage

**Storage interface for cross-session transactions in the Omnipay PHP payment processing library**

[Omnipay](https://github.com/thephpleague/omnipay) is a framework agnostic, multi-gateway payment
processing library for PHP 5.3+. This package implements Authorize.Net support for Omnipay.

## Installation

Omnipay is installed via [Composer](http://getcomposer.org/). To install, simply add it
to your `composer.json` file:

```json
{
    "require": {
        "omnipay/storage": "~2.0"
    }
}
```

And run composer to update your dependencies:

    $ curl -s http://getcomposer.org/installer | php
    $ php composer.phar update

## Basic Usage

Many OmniPay drivers support a callback from the remote payment gateway to communicate
the results of the authorisation. This callback will not be sharing the same session as
the user making the payment. This package provides a consistent way to access the
storage that will work across multiple gateways and drivers.

